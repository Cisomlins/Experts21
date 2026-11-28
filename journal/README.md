# Decision Journal

The office's record of recommendations and decisions, so they can be reviewed and scored later. The format comes from `docs/03-how-the-ai-works_rev00.md` (Decision journal) and the scoring from `docs/13-governance-security-limits_rev00.md` §6.3.

> **Public repository:** every entry here concerns the **fictional example investor** (`CLAUDE.md`, Rule 1). Real decisions with real data belong in a private copy of this project.

## Rules
- **One file per decision:** `journal/YYYY-MM-DD-<short-topic>_rev00.md`.
- **Never overwrite an entry.** When the decision or its outcome changes, save `_rev01`, `_rev02` and so on.
- **Who writes:** `data-librarian`, or the main session at the end of `/ask-the-team`, **only when the principal asks** for the entry to be saved.
- **Review:** on the review date, add the outcome and Brier scores in a new revision (skill `decision-journal`).
- Add each entry to the index below.

## Entry template

```markdown
# <Question> (fictional example investor)

- **Date:** YYYY-MM-DD | **Status:** draft / approved / rejected / reviewed
- **Question:**
- **Options considered:**
- **Recommendation:** (and the memo it came from)
- **Principal's decision and reasoning:** pending / ...
- **Forecasts:** `<event> | p = 0.xx | by <date> | resolves on <source>`
- **Expected value:**
- **Key assumptions:**
- **Kill criteria:**
- **Information available at the time:** (doc snapshots and dates)
- **Dissent:**
- **Experts consulted:**
- **Review date:**

## Outcome (filled in at review)
- **What happened:**
- **Brier score per forecast:**
- **Result vs. passive benchmark and vs. "do nothing":**
- **Lessons:**
```

## Index

| Date | Entry | Status | Review date |
|---|---|---|---|
| 2026-11-28 | [CDI to US Treasuries (test run)](2026-11-28-cdi-to-treasuries_rev00.md) | Draft; principal's decision pending | 2027-05-28 |
