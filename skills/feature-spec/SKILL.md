---
name: Feature spec
slug: feature-spec
description: Write a clear, complete description of a new feature — the problem it solves, who it's for, exactly what to build, and how you'll know it worked.
---

# Feature spec

Use this to write a feature specification (also called a PRD) that defines
what to build, why, and how success will be measured — for a specific
feature request, not a whole roadmap.

## Structure

### 1. Problem statement
2-3 sentences: who experiences this problem, how often, and what it costs
(user frustration, lost time, lost business, competitive risk). Ground it in
real evidence — user feedback, support tickets, or usage numbers — not
assumptions.

### 2. Goals
3-5 specific, measurable outcomes. Each should answer "how will we know this
worked?" Separate what users get from what the business gets. State outcomes
("reduce time-to-value by 50%"), not outputs ("build a wizard").

### 3. Non-goals
3-5 things this feature will explicitly NOT do, with a short reason for each
(not enough impact, too complex for now, belongs to a different effort).
Writing these down prevents the feature quietly growing bigger than planned.

### 4. User stories
Format: "As a [specific type of user], I want [capability], so that
[benefit]." Be specific about the user type ("team admin", not just "user").
Describe what they're trying to accomplish, not the UI mechanism. Include
error/edge cases and different user types where relevant. List them in
priority order.

Common mistakes: too vague ("I want it to be faster" — faster how?),
describing a UI widget instead of a need, missing the "why", or being too
big to build as one item.

### 5. Requirements
Group into three tiers:
- **Must-have**: the feature isn't viable without these — ask "if we cut
  this, does it still solve the core problem?"
- **Nice-to-have**: meaningfully better, but the core case works without it
  — often a fast follow-up
- **Future considerations**: explicitly out of scope now, but worth keeping
  in mind so today's design doesn't accidentally block them later

For each requirement: describe the expected behavior clearly, list
acceptance criteria, and flag any dependency on another team or system.

Be strict about must-haves — if everything is must-have, nothing really is.

### 6. Success metrics
- **Leading indicators** (visible within days-weeks): adoption rate,
  activation rate, task completion rate, time to complete, error rate, usage
  frequency
- **Lagging indicators** (visible over weeks-months): retention, revenue
  impact, satisfaction change, support ticket volume, competitive win rate
- Set a specific target ("50% adoption within 30 days", not "high
  adoption"), a success threshold and a stretch target, and say when you'll
  check it

### 7. Open questions
List unanswered questions, who needs to answer each one, and whether it
blocks starting work or can be resolved along the way.

### 8. Timeline considerations
Hard deadlines, dependencies on other teams' work, and a suggested phasing
if the feature is too big for one release.

## Writing acceptance criteria

Given/When/Then format, or a plain checklist:

```
Given [context/precondition]
When [the user does something]
Then [expected outcome]
```

Cover the normal case, error cases, and edge cases. Describe expected
behavior, not implementation. Avoid vague words like "fast" or "intuitive"
without defining what they mean concretely. Each criterion should be
independently checkable.

## Avoiding scope creep

Watch for: requirements getting added after the spec is agreed, "small"
additions piling up, features nobody asked for sneaking in ("while we're at
it..."), or the launch date slipping quietly instead of being explicitly
re-scoped.

Guard against it by: writing explicit non-goals, requiring any scope
addition to come with something removed or the timeline extended, keeping
"this version" clearly separate from "future version", and time-boxing open
investigations ("if we can't resolve X in 2 days, we cut it").
