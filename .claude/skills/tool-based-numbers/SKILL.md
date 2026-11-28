---
name: tool-based-numbers
description: "Compute every figure with a tool (Python via Bash, a data API, or a cited table), never from model memory. Use whenever an answer contains a number that is calculated, converted or looked up."
---

# tool-based-numbers (S02)

**Used by:** `chief-investment-officer`, `equities-analyst`, `fixed-income-analyst`, `real-estate-analyst`, `private-markets-analyst`, `commodities-energy-analyst`, `digital-assets-analyst`, `fx-strategist`, `quant-portfolio-analyst`, `risk-officer`, `macro-economist`, `tax-regulatory-brazil`, `tax-regulatory-us`, `forensic-analyst`, `red-team`, `reporting-accountant`, `operating-businesses-analyst`
**Source docs:** `docs/04-skills-and-expert-roles_rev01.md`, `docs/13-governance-security-limits_rev00.md`

## Procedure
1. Separate inputs (with source and date) from computed outputs.
2. Compute with code: `python3 -c "..."` or a short script. Show the formula and the inputs.
3. State units and currency (BRL or USD) and the FX rate and date used for conversions.
4. Round only in the final presentation; keep full precision in the calculation.
5. Sanity-check: order of magnitude, sign, and a second method where cheap.

## Output
A short "Calculation" block: inputs → formula → result, so anyone can re-run it.

## Never
Never present remembered historical prices or rates as current data. Models memorize past financial data (file 04, guardrail 2).
