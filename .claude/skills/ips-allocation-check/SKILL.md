---
name: ips-allocation-check
description: "Check any proposal against the Investment Policy Statement (goals, ranges, limits, liquidity, currency). Use before any recommendation is finalized."
---

# ips-allocation-check (S07)

**Used by:** `chief-investment-officer`, `quant-portfolio-analyst`, `risk-officer`, `investment-reviewer-prep`
**Source docs:** `docs/02-traditional-family-office_rev01.md`, `docs/05-context-to-ingest_rev01.md`, `docs/06-investment-decisions_rev01.md`

## Procedure
1. Load the current IPS and its version. In this public repo only a **fictional example IPS** may exist (file 05 §5.1 outline).
2. Check: return target, risk limits, liquidity reserve, horizon buckets, currency split (BRL/USD), allocation ranges, position and concentration limits, exclusions.
3. Include the operating businesses in total-wealth exposure (file 07 §5).
4. Run the 10-item decision checklist (file 06 §6.4).
5. Flag every breach; a breach goes to the Risk Officer and needs the principal's logged approval.

## Output
`IPS check (version x): PASS / BREACH` + table of each limit, current, proposed, status.
