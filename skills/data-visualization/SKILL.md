---
name: Data visualization
slug: data-visualization
description: Guidance for picking the right chart for your data and making it easy to read, honest, and accessible to everyone.
---

# Data visualization

Use this when deciding how to chart a dataset or reviewing a chart someone else made. Use available data/chart tools (spreadsheet charts, plotting libraries, or whatever's on hand) to build it — this skill is about which chart to pick and how to make it trustworthy and readable.

## Chart selection

| What you're showing | Best chart | Alternatives |
|---|---|---|
| Trend over time | Line chart | Area chart (for cumulative or composition) |
| Comparing categories | Vertical bar chart | Horizontal bar (many categories) |
| Ranking | Horizontal bar chart | Dot plot, slope chart (two periods) |
| Part-to-whole | Stacked bar chart | Treemap (hierarchical) |
| Composition over time | Stacked area chart | 100% stacked bar |
| Distribution of values | Histogram | Box plot (comparing groups), violin plot |
| Relationship between two numbers | Scatter plot | Bubble chart (add a third variable as size) |
| Relationship among many variables | Correlation heatmap | Pair plot |
| Geographic pattern | Map with shaded regions | Bubble map |
| Sequential process / drop-off | Funnel chart | Sankey diagram (for flow) |
| Performance vs. target | Bullet chart | Gauge (single number only) |
| Several KPIs at once | Small multiples (grid of mini charts) | Dashboard |

### Charts to avoid or use carefully

- **Pie charts** — only for fewer than 6 categories where rough comparison is enough; people are bad at judging angles. Bar charts are usually clearer.
- **3D charts** — avoid entirely; they distort the data and add nothing.
- **Dual-axis charts** — use cautiously, they can imply a false correlation between two unrelated scales; label both axes clearly.
- **Stacked bars with many categories** — hard to compare the middle segments; use small multiples or grouped bars instead.
- **Donut charts** — same issue as pie charts; fine only for a single headline number.

## Design principles

**Color**
- Color should carry meaning, not decorate. Highlight the one thing that matters with a bright color and grey out the rest.
- Use a single-hue gradient (light to dark) for ordered/sequential data.
- Use a two-hue gradient with a neutral midpoint for data with a meaningful center point (e.g., above/below zero).
- Cap categorical color palettes at 6-8 distinct colors — more becomes unreadable.
- Never rely on red/green alone — a meaningful share of people can't distinguish them; pair with blue/orange or add shape/pattern.

**Wording**
- Title the chart with the insight, not the topic: "Revenue grew 23% year over year" beats "Revenue by month."
- Add a subtitle with context: date range, filters, data source.
- Label axes with units; never make the reader guess what a number means.
- Add data labels only on the points that matter, not every single bar.

**Layout**
- Remove gridlines, borders, and backgrounds that don't carry information.
- Sort by value, not alphabetically — unless there's a natural order (months, funnel stages).
- Give charts room; don't cram several together with no space.

**Accuracy — do not mislead**
- Bar charts must start at zero. A bar cut off partway exaggerates small differences.
- Line charts can use a non-zero baseline when the variation itself is the point.
- When comparing several charts side by side, keep the same axis scale across all of them.
- Show uncertainty (error bars, ranges) when the data has meaningful uncertainty.

## Accessibility checklist

Before sharing any chart, confirm:
- [ ] It's still readable without color — series are distinguished by pattern, line style, or direct labels too
- [ ] Text is legible at normal zoom (10pt minimum for labels, 12pt for titles)
- [ ] The title states the insight, not just the data category
- [ ] Axes are labeled with units
- [ ] The legend is clear and doesn't sit on top of the data
- [ ] Data source and date range are noted somewhere on the chart
- [ ] It still works printed in black and white
