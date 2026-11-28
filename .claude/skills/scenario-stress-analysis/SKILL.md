---
name: scenario-stress-analysis
description: "Build bear/base/bull scenarios with probabilities and signposts, and stress-test a portfolio against the standard historical and forward-looking shocks. Use for allocation decisions, macro views and risk reviews."
---

# scenario-stress-analysis (S04)

**Used by:** `chief-investment-officer`, `fixed-income-analyst`, `commodities-energy-analyst`, `fx-strategist`, `quant-portfolio-analyst`, `risk-officer`, `macro-economist`, `geopolitical-analyst`, `operating-businesses-analyst`
**Source docs:** `docs/06-investment-decisions_rev01.md`, `docs/07-risk-analysis_rev01.md`, `docs/08-economy-and-macro_rev01.md`, `docs/09-geopolitics-and-politics_rev01.md`

## Procedure
1. Define 3 scenarios (bear, base, bull): narrative, probability (sums to 100%), key variable paths (Selic, IPCA, Fed funds, BRL/USD, equities).
2. For each, state **signposts**: data or events that would tell us we are moving into it.
3. Compute the expected value across scenarios with skill `tool-based-numbers`.
4. Stress set (file 07 §4, run at least quarterly): 2002-type Brazil political shock; 2008 global crisis; 2015–16 Brazil recession; 2020 sudden crash; 2022 inflation/rate shock; forward-looking combined shock (Brazil fiscal stress + BRL −30% + shock to the operating businesses' sector).
5. Report loss in BRL and USD and the effect on liquidity needs.

## Output
Scenario table (probability, narrative, variables, portfolio impact) + stress table + "what would change this view".
