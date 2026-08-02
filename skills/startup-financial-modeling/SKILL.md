---
name: Startup financial modeling
slug: startup-financial-modeling
description: Build a realistic multi-year financial forecast for a small business or startup — revenue, costs, cash runway, and hiring plan — using simple, standard formulas.
---

# Startup financial modeling

Build a 3-5 year financial model covering revenue, costs, cash flow, and
headcount, with scenario planning for decision-making and investor or
board presentations.

## Revenue model

Build revenue bottom-up from customer cohorts, not a flat growth-rate
guess:

```
MRR = sum across cohorts of (cohort size × retention rate × average revenue per user)
ARR = MRR × 12
```

Key inputs: new customers acquired per month, retention by month, average
revenue per user, pricing/packaging, and any expansion revenue (upsells).

Typical SaaS retention curve to sanity-check against: ~100% at month 1,
~90% at month 3, ~85% at month 6, ~75% at month 12, ~70% at month 24.

## Cost structure

Group costs into four standard categories:

1. **COGS** — hosting/infrastructure, payment processing, variable support cost, per-customer third-party fees.
2. **Sales & Marketing** — CAC, ad spend, sales compensation, marketing tools.
3. **R&D** — engineering, product, design, dev tools.
4. **G&A** — executive, finance/legal/HR, office, insurance/compliance.

Split each into fixed (salaries, software, rent) versus variable (hosting,
processing, support) so the model scales correctly with growth.

Typical early-stage SaaS headcount split: Engineering 40-50%, Sales &
Marketing 25-35%, G&A 10-15%, Customer Success 5-10%.

## Cash flow and runway

```
Monthly burn = monthly revenue − monthly expenses
Runway (months) = current cash balance / monthly burn rate
```

Track beginning cash, inflows (revenue, fundraising), outflows (opex,
capex), and ending cash each month. Remember revenue collected is not the
same as revenue booked — model payment terms and collection timing, not
just the invoice date.

## Headcount planning

Track fully-loaded cost per role (salary × ~1.3-1.4 for benefits/taxes),
hiring velocity (roles typically take 3-6 months to fill), and ramp time
(3-6 months to full productivity). Account for 10-15% annual attrition.

## Scenario framework

Build three scenarios by varying the same core assumptions:

- **Conservative (P10)**: slower acquisition, lower pricing/conversion, higher churn, longer sales cycles. Use for cash management.
- **Base (P50)**: most likely assumptions. Use for board reporting.
- **Optimistic (P90)**: faster growth, better unit economics, lower churn. Use for upside planning.

Vary customer acquisition rate (±30%), churn (±20%), average contract
value (±15%), and CAC (±25%) across scenarios. Keep pricing structure and
the shape of the hiring plan fixed — only shift timing.

## Time horizon

Monthly detail for years 1-2, quarterly detail for year 3, annual
high-level projections for years 4-5.

## Key metrics to compute

- **Revenue**: MRR/ARR, month-over-month and year-over-year growth.
- **Unit economics**: CAC, LTV, CAC payback period, LTV:CAC ratio.
- **Efficiency**: burn multiple (net burn / net new ARR), magic number (net new ARR / S&M spend), Rule of 40 (growth % + profit margin %).
- **Cash**: monthly burn, runway in months.

## Fundraising integration

```
Post-money valuation = pre-money valuation + investment
Dilution % = investment / post-money valuation
```

Allocate the raise across product, sales & marketing, G&A, and working
capital, sized to reach the next milestone plus a 6-month buffer. Identify
milestones concretely (product launch, first $1M ARR, CAC break-even,
next raise) rather than modeling funding as an open-ended cushion.

## Common pitfalls

- Overly optimistic revenue — new companies rarely hit aggressive projections; model conservative acquisition and realistic churn.
- Underestimating costs — add a buffer (~20%) to expense estimates and use fully-loaded compensation.
- Ignoring cash-flow timing — revenue booked is not cash collected.
- Static headcount assumptions that ignore hiring lead time and ramp.
- Only modeling one scenario — always build the conservative case too, and know what you'd cut if it happens.

## Before presenting a model, sanity-check

- Is the revenue growth rate achievable (roughly 3x in year 2, 2x in year 3 for early-stage SaaS)?
- Are unit economics realistic (LTV:CAC > 3, payback < 18 months)?
- Is the burn multiple reasonable (< 2.0 in years 2-3)?
- Does headcount scale sensibly with revenue?
- Is gross margin appropriate for the business model?
- Does S&M spend align with the CAC and growth targets you're claiming?
