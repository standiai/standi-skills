---
name: Agile product owner
slug: agile-product-owner
description: Turn feature ideas into clear, well-sized to-do items for your team, plan how much work fits in a sprint, and decide what to work on first.
---

# Agile product owner

Use this skill to write clear user stories, break a big idea into smaller
pieces of work, plan a sprint, and decide what's most important in the
backlog.

## Writing a user story

Use this template:

```
As a [type of person using the product],
I want to [do something],
So that [why it matters to them].
```

Example: "As a marketing manager, I want to export campaign reports to PDF,
so that I can share results with people who don't have access to the system."

A good story is:
- **Independent** — can be worked on without waiting on other unfinished work
- **Negotiable** — the how is still open for discussion
- **Valuable** — delivers real benefit to the user or the business
- **Estimable** — the team can roughly size it
- **Small** — fits in one sprint/iteration
- **Testable** — there's a clear way to check it's done

## Writing acceptance criteria

Use Given/When/Then to describe exactly what "done" looks like:

```
Given [the starting situation],
When [the user does something],
Then [what should happen].
```

Example: "Given the user is logged in, when they click Export, then a PDF
download starts within 2 seconds."

Every story should have criteria covering: the normal/happy path, what
happens with bad input, what happens when something fails, and (if relevant)
how fast it should be and whether it works without a mouse.

Rule of thumb for how many criteria to write: small items need 3-4, medium
items need 4-6, large items need 5-8 — and if it needs more than 8, the item
is probably too big and should be split.

## Breaking a big idea into smaller pieces

1. Write down the overall goal and how you'll know it succeeded
2. List every type of person affected
3. List what each of them needs to be able to do
4. Group related needs into individual stories
5. Make sure each story is small enough to finish within one sprint
6. Note anything that has to happen before something else can start
7. Order the stories so each one delivers something usable on its own

Common ways to split a big idea:
- **By step in a process** — e.g. "checkout" becomes "add to cart" + "enter
  payment" + "confirm order"
- **By type of user** — e.g. "dashboard" becomes "admin view" + "regular
  user view"
- **By type of data** — e.g. "import" becomes "import from spreadsheet" +
  "import from CSV"
- **By action** — e.g. "manage users" becomes "create" + "edit" + "remove"
- **Basic version first** — build the simple case, then handle errors and
  edge cases as separate follow-up items

## Planning what fits in a sprint

1. Work out how much the team can realistically get done (based on past
   sprints and who's available this time — subtract time for holidays, part-
   time availability, etc.)
2. Confirm the goal of the sprint with whoever needs to sign off on it
3. Pick items from the prioritized backlog
4. Fill to about 80-85% of capacity as firm commitments
5. Add a small amount of "stretch" work on top, understood as optional
6. Flag anything with dependencies or risk before the sprint starts
7. Break any large committed item into smaller daily tasks

Keep an eye on:
- **How much gets finished vs. committed** — should usually be above 85%
- **How much work gets added or removed mid-sprint** — should stay low
- **How much carries over to the next sprint** — should stay low

## Deciding what's most important

Score backlog items using these questions:
- **Business value** — does it drive revenue, meet demand, fit the
  strategy? (weight this heaviest)
- **User impact** — how many people does it affect, and how often?
- **Risk and dependencies** — anything blocking it, or anything risky about
  it?
- **Effort** — how big and how uncertain is the work?

Sort into rough priority levels:
- **Critical** — something is broken, blocked, or unsafe; do it now
- **High** — core functionality people are actively waiting on; this sprint
- **Medium** — real improvements; next couple of sprints
- **Low** — nice to have; general backlog

## When an item is "done"

A useful default checklist:
- The work is finished and someone else has looked it over
- It's been tested and the tests pass
- All the acceptance criteria are checked off
- Anything that needs written docs has them
- It's been deployed somewhere it can be verified
- Whoever owns the product/backlog has accepted it
- No known serious bugs remain
