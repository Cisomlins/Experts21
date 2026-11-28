---
name: source-verification
description: "Cite and verify every claim: attach a dated source or an Assumption/Estimate label, then check the claim against the source. Use for any factual statement in an answer, memo or brief."
---

# source-verification (S01)

**Used by:** `orchestrator`, `agent-builder`, `chief-investment-officer`, `equities-analyst`, `fixed-income-analyst`, `real-estate-analyst`, `private-markets-analyst`, `commodities-energy-analyst`, `digital-assets-analyst`, `fx-strategist`, `quant-portfolio-analyst`, `risk-officer`, `macro-economist`, `geopolitical-analyst`, `tax-regulatory-brazil`, `tax-regulatory-us`, `legal-estate-planner`, `governance-analyst`, `forensic-analyst`, `red-team`, `reporting-accountant`, `data-librarian`, `operating-businesses-analyst`, `agent-architect`, `prompt-eval-engineer`, `data-integration-engineer`, `security-privacy-engineer`, `br-securities-counsel-prep`, `br-tax-advisor-prep`, `us-tax-advisor-prep`, `investment-reviewer-prep`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/13-governance-security-limits_rev00.md`

## Procedure
1. List every factual claim and number in your draft.
2. For each one, attach a source: document path, filing, data API or URL, plus its date ("as of").
3. If you cannot source it, label it **Assumption:** or **Estimate:**, or remove it.
4. Re-open the source and confirm the claim says what the source says (number, unit, date, jurisdiction).
5. Prefer primary sources (regulator, central bank, statute, filing) over press or blogs. Mark secondary sources as such.
6. For anything dated (rates, prices, election results, laws), say how old it is. If it is older than the question needs, say so.

## Output
End every answer with a **Sources** list: `[n] Title, publisher, date, URL or path`. Unsupported claims carry their label inline.

## Never
Never invent a source, URL, statute number or figure. Say "insufficient data" instead.
