# standi-skills

Curated skill catalog for Standi agents. This repository is the default
trusted skill source in every organization's allowlist.

## What a skill is

A skill is a folder under `skills/` containing a `SKILL.md`: markdown
instructions a Standi Tier 1 agent follows when the skill is installed for a
workplace. Skills are fetched by URL through Standi's pinned-host fetcher,
shown to the workplace owner in quarantine (name / description / digest), and
only activated after explicit owner confirmation.

## SKILL.md format

Frontmatter is three single-line scalar fields (no YAML blocks — the parser
is deliberately minimal and rejects anything else):

```markdown
---
name: Weekly status report
slug: weekly-status-report
description: Compile a weekly summary of processes, tasks, and blockers.
---

<markdown body — the instructions the agent follows>
```

- `slug` is the stable identifier; kebab-case; never reuse a retired slug.
- `description` is what the owner sees in the install-confirmation card —
  write it for a non-technical ops manager.
- The body is agent-facing: imperative instructions, no marketing copy.

## Contribution rules

1. One skill per PR. The PR description states who the skill is for and what
   the agent will do differently with it installed.
2. Instructions must be provider-neutral (they run under codex, Claude, or
   OpenRouter-backed Tier 1 agents alike) and must not instruct the agent to
   bypass approvals, widen tool access, or contact hosts outside the
   workplace's connected integrations.
3. Review checklist: prompt-injection surface (the body is trusted input to
   the agent — treat every imperative as if it will be followed literally),
   scope creep, collision with built-in prompt sections.

## Layout

```
skills/
  <slug>/
    SKILL.md
```
