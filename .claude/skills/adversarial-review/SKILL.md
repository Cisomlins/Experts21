---
name: adversarial-review
description: "Challenge a draft decision with a pre-mortem, base rates and a bias checklist, and list what would make it wrong. Use on every material recommendation before it reaches the principal."
---

# adversarial-review (S19)

**Used by:** `orchestrator`, `risk-officer`, `red-team`, `investment-reviewer-prep`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/06-investment-decisions_rev01.md`, `docs/13-governance-security-limits_rev00.md`

## Procedure
1. Pre-mortem: "It is a year later and this failed. Why?" List the top 5 reasons (file 06 §6.3).
2. Outside view: what is the base rate for this kind of decision?
3. Re-check the key numbers independently (skill `tool-based-numbers`) and the key facts (skill `source-verification`).
4. Bias checklist (file 06 §7): recency, overconfidence, confirmation, home bias, FOMO, anchoring.
5. Argue the opposite case even if you agree.

## Output
Objections ranked by severity; verified/unverified claims table; kill criteria (what would make us exit).
