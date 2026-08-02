---
name: Roadmap management
slug: roadmap-management
description: Plan and explain what your team is building next, decide what matters most, and communicate roadmap changes clearly to stakeholders.
---

# Roadmap management

Use this to build a roadmap, decide what to prioritize, map out
dependencies, plan capacity, or explain a roadmap change to stakeholders.

## Roadmap formats

**Now / Next / Later** — the simplest and usually best default:
- *Now*: committed, actively being built, high confidence
- *Next* (1-3 months out): scoped and prioritized, but timing may shift
- *Later* (3-6+ months out): directional bets, scope and timing flexible

Good for most teams and for communicating outward, since it avoids false
precision about exact dates.

**Quarterly themes** — organize around 2-3 strategic themes per quarter,
each mapped to a business goal, with specific initiatives listed underneath.
Good for showing WHY something is being built, e.g. in planning meetings.

**Goal-aligned roadmap** — start from the team's goals/targets for the
period, and under each one list the initiatives expected to move it,
including the expected impact. Creates clear accountability between what's
built and what's measured.

**Timeline/calendar view** — shows start/end dates and sequencing. Useful
for execution planning with engineering and spotting scheduling conflicts.
Avoid using this format for external communication — it creates false
precision.

## Deciding what to prioritize

**RICE score** = (Reach x Impact x Confidence) / Effort
- Reach: how many people/customers, in a given period (use real numbers)
- Impact: 3 = massive, 2 = high, 1 = medium, 0.5 = low, 0.25 = minimal
- Confidence: 100% = backed by data, 80% = some evidence, 50% = gut feel
- Effort: person-months of work across all functions involved

Good for comparing a large backlog with hard numbers; less good for
strategic bets where impact is genuinely hard to estimate.

**MoSCoW** — Must have / Should have / Could have / Won't have (this time).
Good for scoping a release or negotiating what fits in a period.

**ICE score** (1-10 each) = Impact x Confidence x Ease. Simpler than RICE;
useful when you don't have enough data for RICE, or need a quick pass.

**Value vs. effort matrix** — plot items on a 2x2:
- High value / low effort: do first (quick wins)
- High value / high effort: plan carefully (big bets)
- Low value / low effort: fill in when there's spare time
- Low value / high effort: don't do these — remove from the backlog

## Mapping dependencies

Look for dependencies in five places: technical (one feature needs
infrastructure from another), team (needs another team's work), external
(vendor/partner/third party), knowledge (needs research first), and
sequential (must ship A before starting B).

For each dependency: name an owner responsible for resolving it, set a
"need by" date, build in buffer time (dependencies are usually the riskiest
part of any roadmap), flag cross-team dependencies early, and have a backup
plan if it slips.

To reduce dependencies: build a simpler version that avoids it, use a mock
or interface contract to work in parallel, resequence work to surface the
dependency earlier, or absorb the work into your own team.

## Planning capacity

Start from headcount and time period, subtract known overhead (meetings,
on-call, interviews, holidays, PTO). A common rule of thumb: people spend
roughly 60-70% of their time on planned feature work.

A healthy default allocation: 70% planned features, 20% technical
health/reliability, 10% unplanned buffer for urgent issues. Adjust based on
context — a new product skews toward features, a mature product skews
toward reliability, post-incident periods skew toward reliability.

If commitments exceed capacity, something has to give — cut scope, don't
assume people can just do more. Every time something is added, ask "what
comes off?"

## Communicating roadmap changes

When something changes: say plainly what changed and why, explain what new
information drove the decision, show the tradeoff (what got cut or delayed
to make room), share the updated plan, and tell affected people directly —
don't let them find out from the roadmap doc alone.

Avoid roadmap whiplash: don't rework the roadmap for every small piece of
new information — set a threshold for what counts as a real change. Batch
routine updates on a regular cadence (e.g. monthly) unless something is
genuinely urgent. If the roadmap is changing very often, that's usually a
sign of unclear strategy, not responsiveness.
