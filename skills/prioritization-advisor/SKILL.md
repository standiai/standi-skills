---
name: Prioritization advisor
slug: prioritization-advisor
description: Helps you pick the right way to decide what to work on first, based on how big your team is, how much data you have, and what's causing disagreement.
---

# Prioritization advisor

Help the user choose a prioritization approach that fits their situation, instead of defaulting to whatever framework they've heard of. Different situations call for different approaches — there is no single "best" one.

Ask questions one at a time, offer a few plain-language choices, and let the user pick or describe their own answer in their own words.

## Step 1: Ask about company stage

"What stage is the business in?"
1. Just starting out — still figuring out what customers actually want, moving fast, experimenting
2. Early traction — found something that works, growing, adding to keep customers happy
3. Established — steady market, making things incrementally better, competing on quality
4. Multiple products or teams — need to coordinate priorities across more than one thing

## Step 2: Ask about team and stakeholders

"What's the team and decision-making environment like?"
1. Small team, limited people — need to focus ruthlessly, no time for heavy process
2. Aligned team — everyone agrees on goals, can use more rigorous methods
3. Disagreement among stakeholders — different people want different things, need a fair and transparent process
4. Large organization — many teams, shared roadmaps, dependencies across groups

## Step 3: Ask what problem they're actually trying to solve

"What's the main challenge?"
1. Too many ideas, need to narrow down
2. People disagree and need a way to reach agreement
3. Decisions are being made by gut feel and they want something more grounded in evidence
4. Hard tradeoffs between big bets and quick wins

## Step 4: Ask about available data

"How much data do you have to work with?"
1. Very little — new idea, no usage numbers, few customers to ask
2. Some — basic numbers and feedback, nothing rigorous
3. A lot — solid usage data, experiments, clear metrics

## Step 5: Recommend an approach

Based on the answers, recommend ONE of these approaches and explain briefly why it fits:

- **Quick score (Impact / Confidence / Ease):** lightweight, gut-check scoring. Best for early-stage, small teams, little data. Score each idea 1-10 on each dimension; multiply or average; rank.
- **Reach / Impact / Confidence / Effort score:** more rigorous, needs usage numbers. Best for growing companies with some data and aligned teams. Formula: (Reach × Impact × Confidence) ÷ Effort — higher score = higher priority.
- **Value vs. effort grid:** a simple 2x2 (high value / low effort = do first). Best for fast, visual, low-overhead decisions or building consensus in a meeting.
- **Weighted criteria with stakeholder input:** custom criteria voted or weighted by multiple people. Best when stakeholders disagree and need to feel heard.
- **Must / Should / Could / Won't:** a forcing function for hard yes/no calls, good for scoping a release under a deadline.
- **Cost of delay / urgency-based:** best when some items are time-sensitive and waiting has a real cost.

Then give 3-4 concrete implementation steps for the recommended approach, and note when to reconsider (team grows, stage changes, current approach isn't working, stakeholders keep re-litigating decisions).

## Common pitfalls to warn about

- **Wrong framework for the stage** — heavy scoring processes slow down early-stage teams who need to experiment, not calculate.
- **Switching approaches too often** — pick one and stick with it for months; only change when the situation actually changes.
- **Treating scores as absolute truth** — a framework is an input to judgment, not a replacement for it. Close scores should be broken by judgment, not decimal points.
- **One person scoring alone** — when multiple people are affected by the decision, score together so everyone buys into the result.
- **No process at all** — the loudest voice in the room wins by default. Any consistent process beats none.

Reassess the chosen approach when the business stage changes, the team grows or reorganizes, stakeholder dynamics shift, or the current approach is clearly not working (too slow, ignoring what actually matters).
