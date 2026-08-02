---
name: PRD development
slug: prd-development
description: Turn scattered notes and ideas about a new feature into one clear document that explains the problem, the plan, and how you'll know it worked.
---

# PRD development

A PRD (product requirements document) is a single place that answers: what
problem are we solving, for whom, why now, what are we building, how will we
know it worked, what exactly is required, and what are we deliberately NOT
building. It's a living document, not a frozen contract — expect it to
evolve as you learn.

Use this when starting a real feature or initiative that needs several
people aligned. Skip it for small fixes or when the problem and solution are
already obvious — just write the to-do items directly in that case.

## Structure

Work through these sections, in order. Each has a short goal and a rough
time budget if done as a working session — adjust to fit the size of the
feature.

### 1. Executive summary (~30 min)
One paragraph, written first for clarity and polished last. Format: "We're
building [solution] for [who] to solve [problem], which will result in
[impact]."

### 2. Problem statement (~60 min)
- Who has this problem?
- What exactly is the problem?
- Why does it hurt (for the user, and for the business)?
- Evidence: quotes, support tickets, usage data — not just "we believe..."

### 3. Target users (~30 min)
- Primary persona: role, needs, pain points, current behavior
- Secondary persona(s) if relevant, and how their needs differ

### 4. Strategic context (~45 min)
- What business goal does this support, and why?
- Why prioritize this now instead of later?
- (Optional) size of the opportunity, competitive context

### 5. Solution overview (~60 min)
- 2-3 paragraphs, high level — describe the user-facing behavior, not pixel-
  level UI decisions (leave that to design)
- Walk through the flow step by step in plain language
- List the key features/capabilities included

### 6. Success metrics (~30 min)
- **Primary metric**: the one number this feature must move, with a current
  value and a target (e.g. "activation rate: 40% -> 60%, measured 30 days
  post-launch")
- **Secondary metrics**: other things worth watching
- **Guardrail metrics**: things that must NOT get worse as a result

### 7. Requirements / stories (~90-120 min)
- One-sentence hypothesis: "We believe [change] will cause [outcome]
  because [reason]. We'll measure it by [metric]."
- Break the solution into individual stories: "As a [user], I want [thing],
  so that [benefit]" — with acceptance criteria for each
- Note constraints and edge cases (what if a step is skipped, done out of
  order, etc.)

### 8. Out of scope and dependencies (~30 min)
- What is explicitly NOT being built this round, and why
- What has to happen before work can start (design, other teams, external
  parties)
- Key risks and how you'd respond if they happen
- Open questions still unresolved

## Common mistakes to avoid

- **Written alone, presented as final** — collaborate on the requirements
  section with whoever will build and design it; share drafts before
  finalizing
- **No evidence in the problem statement** — "we believe users have this
  problem" invites pushback; back it with quotes, tickets, or data
- **Too prescriptive** — specifying exact UI details removes room for design
  to do its job; keep the solution section at the behavior level
- **No success metric** — without one, nobody can say whether it worked
- **No out-of-scope section** — invites scope creep; write it down explicitly

## Time investment (rough guide)

- Fast track (clear, simple feature): 1.5-2 days
- Typical (needs some research synthesis, one review round): 2-3 days
- Complex (major initiative, multiple personas): 3-4 days
