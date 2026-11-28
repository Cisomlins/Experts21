---
name: forecast-calibration
description: "State views as explicit probabilities with a horizon and resolution criteria, and log them for Brier scoring. Use for any forecast, scenario probability or buy/sell view."
---

# forecast-calibration (S03)

**Used by:** `chief-investment-officer`, `equities-analyst`, `fixed-income-analyst`, `real-estate-analyst`, `private-markets-analyst`, `commodities-energy-analyst`, `digital-assets-analyst`, `fx-strategist`, `quant-portfolio-analyst`, `risk-officer`, `macro-economist`, `geopolitical-analyst`, `red-team`, `prompt-eval-engineer`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/06-investment-decisions_rev01.md`, `docs/13-governance-security-limits_rev00.md`

## Procedure
1. Write each forecast as: *event*, *probability*, *horizon/date*, *how it will be resolved* (source that decides yes/no).
2. Start from a base rate (outside view), then adjust for specifics. Write both numbers.
3. Avoid 0% and 100%; avoid vague words ("likely") without a number.
4. Record the forecast in the decision journal (skill `decision-journal`).
5. On resolution, compute the Brier score: (probability − outcome)². Lower is better; always saying 50% scores 0.25.

## Output
`Forecast: <event> | p = 0.xx | by <date> | resolves on <source> | base rate: 0.yy`

## Note
Model-stated confidence tends to be overconfident; when stakes are high, sample the judgment more than once and check consistency (file 03, Scoring).
