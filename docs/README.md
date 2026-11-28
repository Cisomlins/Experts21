# AI Family Office: Research Knowledge Base

> **Purpose:** the context base for a private team of AI expert agents. The team acts as a personal family office for one principal: it suggests and analyzes investments (what, where, when), measures risk, and answers questions on the economy, geopolitics, politics, regulation, and company management.
> **Scope:** Brazil and the USA, including cross-border issues. **Research date:** 2026-11-27.
> **Status:** research pass plus revisions (the current rev of each file is linked below). This is research and education, **not** investment, legal, or tax advice. Check anything you act on with licensed Brazilian and US professionals.
> **Public repository, fictional principal:** this is an academic project published on GitHub and Netlify. The "principal" throughout is a **fictional example investor**: a Brazil-resident investor with US assets who owns operating businesses. Hospitality and energy are used only as illustrative sectors. No real person's documents or data belong in this repository.

## How to use this folder

- **Building agents:** start with 01 (vision), 03 (operating model) and 04 (roles and MVP team). Then give each agent the topic files its role card in 04 points to.
- **Agents at run time:** treat these files as background, not live data. Re-check every dated figure, especially in 08 and 09, against its primary source before using it in a recommendation.
- **Reading claims:** every claim carries a numbered citation [n] that maps to the file's Sources list, or is labelled **Assumption**, **Estimate**, **Recommendation**, or **Unverified**.
- **Versioning:** files are never overwritten. A revision is saved as `_rev01`, `_rev02`, and so on, and this index points to the newest one. Exception (2026-11-28, approved by the owner): the earlier revisions of files 02, 04–10, 12 and the roster were removed from the folder in a privacy edit. They remain in git history.

## Index

| # | Topic | File (current rev) | What it covers | Main agent users |
|---|---|---|---|---|
| 01 | What a personal AI Family Office is and does | [01-what-it-is_rev00.md](01-what-it-is_rev00.md) | Purpose, scope, what it may and may not do on its own, comparison with SFO/MFO/wealth managers/robo-advisors, KPIs for "best on the planet", current limits, AI adoption trends | All, especially Chief of Staff |
| 02 | How a traditional family office works | [02-traditional-family-office_rev01.md](02-traditional-family-office_rev01.md) | SFO/MFO/virtual FO, wealth thresholds, functions, investment process, org chart, costs, typical allocations, Brazil and US structures | Chief of Staff, CIO |
| 03 | How the AI version works | [03-how-the-ai-works_rev00.md](03-how-the-ai-works_rev00.md) | Request-to-post-mortem pipeline, multi-agent patterns (orchestrator, debate, red team, investment-committee simulation), RAG and memory, routines, memo template, decision journal, calibration; evidence and failure modes of AI agents in finance | Chief of Staff, all builders |
| 04 | Skills and expert roles | [04-skills-and-expert-roles_rev01.md](04-skills-and-expert-roles_rev01.md) | 21 role cards (mission, skills, inputs, outputs, tools, KPIs, guardrails), certification blueprint (CFA, CAIA, FRM, CFP, ANBIMA); **6-agent MVP:** Chief of Staff, CIO, Macro, Risk, Red Team, Data/Reporting | All builders |
| 05 | Context to ingest | [05-context-to-ingest_rev01.md](05-context-to-ingest_rev01.md) | Inventory in five layers (principal, balance sheet, documents, external, operating memory) with priority, frequency and sensitivity (S1–S4); suitability profiling (CVM Res. 30, FINRA/Reg BI); Open Finance Brasil and Plaid; share-vs-redact policy; IPS and principal-profile templates | Data/Librarian, CIO, Risk |
| 06 | Investment decisions: what, where, when | [06-investment-decisions_rev01.md](06-investment-decisions_rev01.md) | Decision hierarchy, asset classes and instruments in BR/US, BRL/USD allocation, timing evidence (valuation, momentum, lump sum vs. DCA), rebalancing, scenario/EV analysis, position sizing, investment memo, biases | CIO, asset-class specialists |
| 07 | Risk analysis | [07-risk-analysis_rev01.md](07-risk-analysis_rev01.md) | Risk taxonomy (including concentration in operating businesses and AI model risk), risk measures and their weaknesses, BR/US stress scenarios, limits and dashboard, hedging, insurance, ERM frameworks, presenting risk to a non-quant | Risk Officer, Red Team |
| 08 | Economy and macro | [08-economy-and-macro_rev01.md](08-economy-and-macro_rev01.md) | Macro framework and regimes, US and Brazil indicators with release calendars, **dated snapshot as of 2026-11-27**, macro-to-asset links, limits of forecasting, scenario method, weekly brief template, energy and hospitality drivers | Macro Economist |
| 09 | Geopolitics and politics | [09-geopolitics-and-politics_rev01.md](09-geopolitics-and-politics_rev01.md) | Political-risk frameworks, market impact of shocks, **dated landscape** (US, Brazil after the Oct-2026 election, US–China, US–Brazil, Middle East, Russia–Ukraine, LatAm), monitoring sources, neutrality rules, country-risk and event-impact templates | Geopolitical/Political Analyst |
| 10 | Regulation and tax (Brazil and USA) | [10-regulation-and-tax_rev02.md](10-regulation-and-tax_rev02.md) | The rev01 verification pass re-checked all 27 items rev00 marked Unverified (see its revision log). Regulating the AI office itself (CVM, LGPD, PL 2338, SEC family office rule); Brazilian investment tax (Law 14.754/2023, Law 15.270/2025, consumption tax reform, ITCMD, holdings); US NRA rules (withholding, US$60k estate exemption), US residency risks (PFIC, FBAR/FATCA); monitoring plan | Regulatory & Tax (BR, US), Legal/Estate |
| 11 | Management and CEO profiling | [11-management-and-ceo-profiling_rev00.md](11-management-and-ceo-profiling_rev00.md) | Evidence that managers matter, profiling from public material (language, insider trades, pay, capital allocation) with how valid each method is, scorecard and red flags (Beneish M-score), ethical and legal limits, profile template, Brazilian governance specifics | Governance/Management Analyst, Due Diligence |
| 12 | Data sources and tools | [12-data-sources-and-tools_rev01.md](12-data-sources-and-tools_rev01.md) | Tables of market, fundamentals, macro, news, geopolitical, regulatory, private-market and alternative data; analytics libraries; FO reporting platforms; MCP connectors; starter stack (about US$100–250/month, estimate) and upgrade path | Data Engineer/Librarian, all |
| 13 | Governance, security, privacy and limits | [13-governance-security-limits_rev00.md](13-governance-security-limits_rev00.md) | Decision-rights matrix (no money movement or signing; each trade needs explicit approval), AI failure modes and fixes, over-trust in automation, security and fraud threats to wealthy families, privacy, governing the agent team (calibration, Brier score, kill switches), NIST AI RMF and ISO 42001 | Chief of Staff, Risk, all |

**Team design:** [expert-roster_rev01.md](expert-roster_rev01.md) lists the 22 agents that run the office (A01–A22, adding an Operating Businesses Analyst to file 04's 21) and the 8 experts needed to build it (B01–B08). Each has a one-line job, a priority, the docs it must read and its decision rights. It also defines 28 shared skills with a skill-by-agent mapping; 16 of them cover the 6-agent MVP.

**Using the team:** [how-to-talk-to-your-experts_rev00.md](how-to-talk-to-your-experts_rev00.md) shows how to ask one expert or the whole team, with four example prompts and a real test run of the orchestrator.

## Points that apply across files

1. **The principal's US tax status changes the advice.** As a Brazilian tax resident who is a US non-resident alien, US estate tax applies above US$60k of US-situs assets and dividends are withheld at 30%. If the principal becomes a US tax resident (green card or the substantial-presence test), worldwide income, FBAR/FATCA and PFIC rules apply. Files 02, 05, 06, 07 and 10 all flag this. It needs a professional answer before the tax agents are built.
2. **No US–Brazil income tax treaty (confirmed in 10 rev02).** Brazil is not on the IRS treaty list. File 02 still labels this an assumption; 10 rev02 is the reference.
3. **Brazilian tax notes in 06 defer to 10 rev02.** File 06 marks its tax remarks as assumptions. 10 rev02 settles the Law 15.270 transition rule, confirms LCI/LCA/CRI/CRA are outside the minimum-tax base, and confirms IOF of 1.1% on remittances for investment (3.5% without an investment purpose).
4. **Copom projection vs. actual IPCA.** The Copom's 5.6% IPCA projection for 2026 (used in 06) is a forecast. The 4.63% in 08 is the latest actual 12-month rate. Both are correct; don't mix them up.
5. **The dated snapshots go stale.** The figures in 08 and 09 describe 27 Nov 2026. The Macro and Geopolitical agents should refresh them on every run.

## Research method and quality

- **How it was produced:** 7 parallel research agents each covered one or two topics using web search and page retrieval. They were told to prefer primary sources (regulators, central banks, official statistics, peer-reviewed papers, major bank and consultancy reports).
- **Review:** the lead reviewer checked structure, scanned for consistency across files, and spot-checked several high-impact current facts against fresh sources. These matched the docs: the Selic hold at 13.75% on 4 Nov 2026 with a 5.6% IPCA projection, Lula's 25 Oct 2026 runoff win, and the 20 Feb 2026 Supreme Court ruling striking down the IEEPA tariffs.
- **Known limits:**
  - The shared web-search budget ran out near the end, so later items in 05, 08, 09, 10 and 12 are labelled **Assumption** or **Unverified** instead of cited.
  - Some primary sites (planalto.gov.br, anbima.com.br) could not be fetched, so a few legal and certification facts rest on search summaries.
  - Some vendor prices in 12 come from third-party sites.
- **Next revision (`_rev01`):** resolve the **Unverified** items, starting with file 10 and the 2002/2008 crisis figures in 07. Replace secondary-source figures with primary ones.

## Counts

13 topic files, roughly 50,000 words, about 345 cited sources.
