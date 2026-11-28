---
name: regulatory-monitoring
description: "Track CVM, BCB, Receita Federal, Congress, SEC, IRS and FinCEN changes and record each one on the change-impact template. Use for regulatory watch and 'what changed' questions."
---

# regulatory-monitoring (S15)

**Used by:** `geopolitical-analyst`, `tax-regulatory-brazil`, `tax-regulatory-us`, `br-securities-counsel-prep`
**Source docs:** `docs/10-regulation-and-tax_rev02.md`

## Procedure
1. Check the feeds in file 10 §D.1 at their stated frequency.
2. For each change: instrument and number, status (proposed / published / in force / suspended / litigated), effective date.
3. Fill the change-impact record (file 10 §D.2) and triage High/Medium/Low.
4. Route High items to the orchestrator the same day.

## Output
One change-impact record per change, sources primary first.
