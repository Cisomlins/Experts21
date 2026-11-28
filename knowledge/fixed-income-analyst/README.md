# Knowledge folder: Paulo, Fixed Income Analyst (`fixed-income-analyst`)

`fixed-income-analyst` reads every file in this folder before answering. Documents here are treated as newer and more specific than the research in `docs/`.

## What belongs here
Public rate sheets, Tesouro Direto and Treasury yield tables, bond term sheets (fictional or public).

## What does NOT belong here (public repository)
- Real personal or financial data: names, IDs (CPF/SSN), account numbers, holdings, statements, tax returns, contracts, credentials.
- Anything not public or fictional. This repo is published on GitHub and Netlify (`CLAUDE.md`, Rule 1).

## Private documents (private copy only)
Put real documents in `knowledge/fixed-income-analyst/private/`. That folder is excluded by `.gitignore`, so it is never committed, and the agent reads it when it exists. Use it only in a private copy of this project, and check `git status` before every commit.

## How to add a document
Add the file here (Markdown, PDF, CSV or text), with a date in its name or first line, for example `2026-11-28-rate-sheet.md`. Then ask `@agent-fixed-income-analyst` a question that uses it.
