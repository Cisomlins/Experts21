---
name: document-library
description: "Ingest, tag, search and cite the office's documents with access control. Use when a question depends on a document in docs/ or a knowledge folder."
---

# document-library (S22)

**Used by:** `legal-estate-planner`, `data-librarian`, `data-integration-engineer`
**Source docs:** `docs/03-how-the-ai-works_rev00.md`, `docs/05-context-to-ingest_rev01.md`

## Procedure
1. Search `docs/` (and knowledge folders when they exist) with Grep/Glob before answering from memory.
2. Quote the passage and cite the file path and section.
3. Tag new documents with: type, date, source, sensitivity (Public/Internal/Confidential/Restricted; file 13 §4.1), jurisdiction.
4. Respect sensitivity: in this public repository only Public and fictional Internal material may be stored.

## Never
Never add real personal or financial documents to this repository.
