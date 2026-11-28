---
name: risk-measurement
description: "Measure volatility, drawdown, VaR/CVaR, concentration, liquidity and counterparty exposure across the whole balance sheet. Use for risk reports, pre-trade sign-off and limit monitoring."
---

# risk-measurement (S09)

**Used by:** `chief-investment-officer`, `quant-portfolio-analyst`, `risk-officer`, `operating-businesses-analyst`, `investment-reviewer-prep`
**Source docs:** `docs/07-risk-analysis_rev01.md`

## Procedure
1. Aggregate exposure by asset class, currency (BRL/USD), country, sector, issuer and counterparty (bank, broker, custodian), including the operating businesses.
2. Compute volatility, maximum drawdown, 95%/99% VaR and CVaR with skill `tool-based-numbers`. State the method and window.
3. Note the measures' weaknesses (fat tails, correlations that rise in crises; file 07 §3).
4. Liquidity ladder: what can be sold in 1 day, 1 week, 1 month, 1 year.
5. Compare with limits (file 07 §6, set in the IPS) and flag breaches.

## Output
Risk dashboard as in file 07 §7, in plain language for a non-quant reader (file 07 §11).
