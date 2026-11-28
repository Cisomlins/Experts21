---
name: valuation
description: "Value an asset with DCF, multiples, cap rates or yields, with every assumption explicit. Use when deciding whether a price is attractive."
---

# valuation (S06)

**Used by:** `equities-analyst`, `fixed-income-analyst`, `real-estate-analyst`, `private-markets-analyst`, `digital-assets-analyst`
**Source docs:** `docs/06-investment-decisions_rev01.md`

## Procedure
1. Pick at least two methods suited to the asset (DCF and multiples for equities; cap rate for property; yield-to-maturity and spread for bonds; NAV for funds).
2. List assumptions with sources: growth, margins, discount rate (state the risk-free rate used: CDI/Tesouro or US Treasuries), terminal value.
3. Compute with skill `tool-based-numbers`; show a sensitivity table (discount rate × growth).
4. Compare value with price: margin of safety in %.
5. Compare the expected return with the hurdle: CDI (BRL money) or T-bills (USD money), after tax and fees (file 06 checklist item 4).

## Output
Value range (low/base/high), margin of safety, key sensitivities, hurdle comparison.
