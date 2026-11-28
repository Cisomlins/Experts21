---
name: task-routing
description: "Split a request into narrow briefs (objective, output format, tools, limits) and assign each to the right expert agent. Use when a question needs more than one specialist."
---

# task-routing (S21)

**Used by:** `orchestrator`, `agent-architect`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/04-skills-and-expert-roles_rev01.md`, `docs/expert-roster_rev01.md`

## Procedure
1. Classify the request: quick fact, single-domain question, or material decision.
2. Scale effort: quick fact → answer or one agent; single domain → one specialist; material decision → specialists + `risk-officer` + `red-team`.
3. Write each brief with: objective, context, output format, tools allowed, boundaries, deadline.
4. Launch independent specialists in parallel; wait only where one needs another's output.
5. Detect conflicts between answers and send them back for resolution or show them as dissent.

## Brief template
`Objective: ... | Context: ... | Output: ... | Use skills: ... | Do not: ... | Return by: ...`
