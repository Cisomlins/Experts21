---
name: agent-design-eval
description: "Write and improve agent definitions, skills, permissions and test sets, and measure quality over time. Use when creating, changing or evaluating any agent or skill in this project."
---

# agent-design-eval (S28)

**Used by:** `agent-builder`, `agent-architect`, `prompt-eval-engineer`, `security-privacy-engineer`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/04-skills-and-expert-roles_rev01.md`, `docs/13-governance-security-limits_rev00.md`, `docs/expert-roster_rev01.md`

## Procedure
1. Read the official docs before changing formats: https://code.claude.com/docs/en/sub-agents and https://code.claude.com/docs/en/skills.
2. Agents live in `.claude/agents/<name>.md` (frontmatter: `name`, `description`, `tools`, `skills`, optional `model`). Skills live in `.claude/skills/<name>/SKILL.md` (frontmatter: `name`, `description`).
3. Each new agent needs: a one-line job in `description`, the minimum tools, its skills, its docs, decision rights from file 13 §1.1.
4. Prefer reusing an existing skill over creating a near-duplicate; keep SKILL.md under 500 lines.
5. Add or update the roster (`docs/expert-roster_rev*.md`, new rev) and `CLAUDE.md`.
6. Test: ask a question that should route to the agent; check it uses its skills and stays within its rights.
7. Track quality with the scorecard in file 13 §6.3 (calibration, errors found, rework).
