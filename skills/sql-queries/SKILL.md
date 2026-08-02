---
name: SQL queries
slug: sql-queries
description: Write correct, efficient database queries — including comparisons, running totals, trends over time, and cleaning up duplicate records.
---

# SQL queries

Use this when writing or reviewing SQL against a business database or data warehouse (PostgreSQL, Snowflake, BigQuery, Redshift, Databricks, or similar). Write queries that are correct, readable, and efficient — not just queries that happen to return an answer.

## Before writing a query

- Confirm what table and columns actually exist rather than guessing names.
- Prefer readable, structured queries (see CTEs below) over deeply nested subqueries.
- Always qualify column names with a table alias when joining more than one table, to avoid ambiguous-column errors.
- Filter dates/times explicitly rather than relying on default sort order.

## Structure complex queries with CTEs (WITH clauses)

Break a query into named, readable steps instead of one giant nested query:

```sql
WITH
base_users AS (
    SELECT user_id, created_at, plan_type
    FROM users
    WHERE created_at >= DATE '2024-01-01' AND status = 'active'
),
user_metrics AS (
    SELECT u.user_id, u.plan_type,
           COUNT(DISTINCT e.session_id) AS session_count,
           SUM(e.revenue) AS total_revenue
    FROM base_users u
    LEFT JOIN events e ON u.user_id = e.user_id
    GROUP BY u.user_id, u.plan_type
)
SELECT plan_type, COUNT(*) AS user_count, AVG(session_count) AS avg_sessions
FROM user_metrics
GROUP BY plan_type
ORDER BY user_count DESC;
```

## Common analytical patterns

**Ranking / "top N per group"** — use a window function, then filter:
```sql
ROW_NUMBER() OVER (PARTITION BY category ORDER BY revenue DESC) AS rnk
```

**Running totals / moving averages:**
```sql
SUM(revenue) OVER (ORDER BY date_col ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) AS running_total
AVG(revenue) OVER (ORDER BY date_col ROWS BETWEEN 6 PRECEDING AND CURRENT ROW) AS moving_avg_7d
```

**Comparing to a prior row (e.g. week-over-week):**
```sql
LAG(value, 1) OVER (PARTITION BY entity ORDER BY date_col) AS prev_value
```

**Deduplication — keep the most recent row per key:**
```sql
WITH ranked AS (
    SELECT *, ROW_NUMBER() OVER (PARTITION BY entity_id ORDER BY updated_at DESC) AS rn
    FROM source_table
)
SELECT * FROM ranked WHERE rn = 1;
```

**Funnel / conversion analysis** — flag each step per user, then sum and divide:
```sql
WITH funnel AS (
    SELECT user_id,
           MAX(CASE WHEN event = 'viewed' THEN 1 ELSE 0 END) AS step_1,
           MAX(CASE WHEN event = 'started' THEN 1 ELSE 0 END) AS step_2,
           MAX(CASE WHEN event = 'completed' THEN 1 ELSE 0 END) AS step_3
    FROM events
    GROUP BY user_id
)
SELECT COUNT(*) AS total,
       SUM(step_1) AS viewed, SUM(step_2) AS started, SUM(step_3) AS completed,
       ROUND(100.0 * SUM(step_2) / NULLIF(SUM(step_1), 0), 1) AS view_to_start_pct
FROM funnel;
```

**Cohort retention** — group users by their start month, then check activity in later months:
```sql
WITH cohorts AS (
    SELECT user_id, DATE_TRUNC('month', first_activity_date) AS cohort_month FROM users
)
SELECT cohort_month, COUNT(DISTINCT user_id) AS cohort_size
FROM cohorts GROUP BY cohort_month ORDER BY cohort_month;
```

## Performance basics (apply across most databases)

- Filter as early as possible; avoid `SELECT *` on wide tables.
- Use `EXISTS` instead of `IN` for correlated subqueries.
- Index or otherwise optimize columns that are frequently filtered or joined on (exact mechanism varies by database — ask or check what's available).
- Filter on date/partition columns explicitly when the table is time-partitioned; this is often the single biggest performance factor on a warehouse.
- Avoid mixing dialect-specific syntax (e.g. `ILIKE` is not universal — some databases only support `LOWER(col) LIKE ...`).

## Debugging a failing or wrong query

1. **Syntax error** — check for functions or operators that aren't supported in this specific database; they vary more than people expect.
2. **Column not found** — check exact name, spelling, and case sensitivity.
3. **Type mismatch** — cast explicitly when comparing different types.
4. **Division by zero** — guard with `NULLIF(denominator, 0)`.
5. **Ambiguous column** — qualify every column with its table alias once more than one table is involved.
6. **"Column must appear in GROUP BY"** — every selected column that isn't aggregated must be listed in the GROUP BY clause.
