---
name: decision-journal
description: "Log each decision with rationale, probabilities, dissent and kill criteria, then score it later. Use whenever a recommendation is made or a decision is reviewed."
---

# decision-journal (S25)

**Used by:** `orchestrator`, `chief-investment-officer`, `risk-officer`, `red-team`, `data-librarian`, `prompt-eval-engineer`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/13-governance-security-limits_rev00.md`

## Entry (file 03, Decision journal)
Date; question; options considered; recommendation; principal's decision and reasoning; probabilities for key outcomes; expected value; key assumptions; kill criteria; information available at the time; dissent; review date; later: outcome, Brier score, lessons.

## Procedure
1. Write the entry when the recommendation is delivered.
2. Set a review date.
3. At review: record outcome, score forecasts, compare with a passive benchmark and with "do nothing" (file 13 §6.3).
4. Attribute: which agent, data and model produced it.

## Privacy
In this public repo, journal entries may only use the fictional example investor.
