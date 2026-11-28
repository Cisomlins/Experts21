---
name: data-pipelines
description: "Connect and refresh market, macro, account and filing data, stored point-in-time. Use when designing or running data feeds."
---

# data-pipelines (S23)

**Used by:** `data-librarian`, `data-integration-engineer`
**Source docs:** `docs/05-context-to-ingest_rev01.md`, `docs/12-data-sources-and-tools_rev01.md`

## Procedure
1. Choose sources from the lean starter stack (file 12 §12.1); prefer official APIs (BCB SGS, FRED, SEC EDGAR, CVM).
2. Store every record with source, retrieval time and as-of date (point-in-time).
3. Validate: missing values, stale data, unit and currency checks.
4. Account data (Open Finance Brasil, Plaid; file 05 §2) is Confidential: never in this public repo, never in test sets.

## Output
Data-quality report: source, freshness, gaps, errors.
