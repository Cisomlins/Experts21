---
name: portfolio-construction-backtest
description: "Turn views into sized positions and backtest with point-in-time data and bias disclosures. Use when proposing weights or testing a strategy."
---

# portfolio-construction-backtest (S08)

**Used by:** `chief-investment-officer`, `quant-portfolio-analyst`
**Source docs:** `docs/04-skills-and-expert-roles_rev01.md`, `docs/06-investment-decisions_rev01.md`

## Procedure
1. Inputs: views with probabilities, IPS constraints, current holdings, costs and taxes.
2. Size with conviction scores (file 06 §6.7) and, at most, one-quarter to one-half Kelly as an upper bound (file 06 §6.6), capped by IPS limits.
3. Construct with a transparent method (equal-risk, mean-variance with constraints, or simple rules). Use open-source libraries listed in file 12 §10.1.
4. Backtest with point-in-time data including delisted securities; include costs, taxes and FX.
5. Disclose survivorship, look-ahead and overfitting risks.

## Never
Never present an LLM-driven backtest over periods before the model's training cutoff as evidence of skill (memorization inflates results; file 04 role 4).
