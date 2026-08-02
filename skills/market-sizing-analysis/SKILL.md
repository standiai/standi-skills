---
name: Market sizing analysis
slug: market-sizing-analysis
description: Estimate how big a market opportunity really is — total market, the slice you can realistically sell into, and the slice you can realistically win — using simple, defensible math.
---

# Market sizing analysis

Estimate market opportunity using three standard measures: TAM, SAM, and
SOM. Use whichever calculation method fits the data you have, and
cross-check with a second method when possible — a single-method estimate
is much less credible.

## The three-tier framework

- **TAM (Total Addressable Market)** — total revenue opportunity if you captured 100% of the market. Example: all email marketing software revenue globally.
- **SAM (Serviceable Available Market)** — the portion of TAM you could realistically target given your product, geography, and segment focus. Example: AI-powered email marketing for e-commerce in North America.
- **SOM (Serviceable Obtainable Market)** — the realistic share you could win in 3-5 years, accounting for competition and resources. Example: 2-5% of SAM.

## Three methods to calculate TAM

**1. Top-down** — start from total market size (industry reports) and
narrow down with filters.
```
TAM = total market category size
SAM = TAM × geographic % × segment %
SOM = SAM × realistic capture rate (2-5%)
```
Use when solid market research already exists. Quick, but less credible
alone — always pair with bottom-up if possible.

**2. Bottom-up** — build up from customer segment data.
```
TAM = sum of (segment size × annual revenue per customer)
SAM = TAM × (segments you can serve / total segments)
SOM = SAM × realistic penetration rate (year 3-5)
```
Use when targeting specific, well-understood customer segments. This is
the most credible method for investors — build from real customer/pricing
data where possible.

**3. Value theory** — estimate based on the value your solution creates.
```
Value per customer = cost of the problem × % solved by your solution
Price per customer = value × willingness-to-pay % (typically 10-30%)
TAM = total potential customers × price per customer
SAM = TAM × % meeting buy criteria
SOM = SAM × realistic adoption rate
```
Use for new categories or disruptive ideas where no existing market data
applies.

## Step-by-step process

1. **Define the market**: what problem, which customers, what category, what geography, what time horizon?
2. **Gather data**: industry reports and public filings for top-down; customer interviews, CRM/sales data, or industry databases for bottom-up; problem-cost studies and pricing research for value theory.
3. **Calculate TAM** using the chosen method(s); document sources and assumptions.
4. **Narrow to SAM** by applying geographic, product, and customer-fit filters. Example: TAM $10B × 40% (region) × 30% (segment) × 60% (feature fit) = SAM $720M.
5. **Estimate SOM** conservatively — 2% at year 3, 5% at year 5 of SAM is a reasonable default for a new entrant.
6. **Validate**: compare top-down and bottom-up results (should land within about 30% of each other); sanity-check against public company revenues in the space; flag a TAM under $1B (too small for most VC-backed plans) or a SOM over 10% in 5 years (too aggressive).

## Formulas by business model

- **SaaS**: TAM = total target companies × average contract value × (1 + expansion rate)
- **Marketplace**: TAM = total category GMV × expected take rate
- **Consumer**: TAM = total users × average revenue per user × purchase frequency per year
- **B2B services**: TAM = total target companies × average deal size × deals per year

## Presenting the numbers

For investors: lead with the bottom-up number (most credible), show it
triangulates with top-down, state your assumptions plainly, and connect it
to revenue projections.

For internal strategy: focus on SAM and SOM rather than TAM, break it down
by segment, and connect it directly to the go-to-market plan.

## Common mistakes to avoid

- Confusing TAM with SAM — don't claim the whole market is addressable.
- An overly aggressive SOM — new entrants rarely capture more than 5% within 5 years.
- Relying on top-down alone — always try to triangulate with a second method.
- Cherry-picking data or mixing inconsistent sources.
- Ignoring market growth/decline, competitive intensity, and switching costs.
