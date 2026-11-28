---
name: brl-usd-analysis
description: "Analyze BRL/USD drivers, carry, hedging cost and currency matching of liabilities. Use for currency allocation, hedges and any cross-border decision."
---

# brl-usd-analysis (S12)

**Used by:** `chief-investment-officer`, `fixed-income-analyst`, `fx-strategist`, `risk-officer`
**Source docs:** `docs/06-investment-decisions_rev01.md`, `docs/07-risk-analysis_rev01.md`

## Procedure
1. Drivers: interest-rate differential (Selic vs. Fed funds), terms of trade, fiscal risk, flows, global dollar cycle.
2. Carry cost of holding USD: roughly the BRL-minus-USD short-rate gap (file 06 §2.3, Estimate).
3. Match currency to liabilities: what future spending is in USD vs. BRL.
4. Hedging tools and costs: forwards/NDFs, options, natural hedges (file 07 §8).
5. Include IOF on remittances: 1.1% when the purpose is investment, 3.5% otherwise (file 10 §B.6).

## Output
Current split, target split with reasoning, hedge options with annual cost.
