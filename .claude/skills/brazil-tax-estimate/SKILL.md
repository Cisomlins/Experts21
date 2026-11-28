---
name: brazil-tax-estimate
description: "Estimate Brazilian tax on an investment or structure under current law (income tax tables, exemptions, Law 14.754, Law 15.270, IOF, ITCMD). Use for after-tax comparisons and tax questions. Estimates only."
---

# brazil-tax-estimate (S13)

**Used by:** `fixed-income-analyst`, `real-estate-analyst`, `tax-regulatory-brazil`, `legal-estate-planner`, `operating-businesses-analyst`, `br-tax-advisor-prep`
**Source docs:** `docs/10-regulation-and-tax_rev02.md`

## Procedure
1. Identify instrument, holder (individual, holding, fund), holding period and amounts.
2. Apply the rules in file 10 §B with their dates: regressive table; exemptions (LCI/LCA/CRI/CRA, incentivized debentures, qualifying FIIs); equities monthly R$20k exemption; 15% annual on foreign financial income (Law 14.754); 10% dividend withholding above R$50k/month per paying company and the IRPF-M (Law 15.270); IOF.
3. Compute with skill `tool-based-numbers`.
4. State which rules are pending or litigated (file 10 open items).
5. Write the questions a licensed Brazilian tax advisor must confirm (skill `professional-escalation`).

## Never
Never present the estimate as tax advice or a filing position.
