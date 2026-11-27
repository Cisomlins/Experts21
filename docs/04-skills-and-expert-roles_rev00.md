# Skills and Expert Roles

> **Purpose:** Map human family office roles to AI agent roles, with mission, skills, inputs, outputs, tools, KPIs and guardrails, and recommend an MVP build order. **Primary users:** the human developer writing agent definitions, the Chief of Staff/Orchestrator (routing), and every specialist agent (its own role card).

## Summary

- A human family office is organized around investment management, risk, tax/legal/estate, reporting and administration; the AI team mirrors this with 19 agent roles grouped into five layers: coordination, investment, risk and challenge, advisory (tax/legal/governance), and operations.
- Each role card below is derived from professional bodies of knowledge: CFA Program (investment analysis and portfolio management) [1], CAIA (alternatives: real assets, private equity, private debt, hedge funds, digital assets) [2], FRM (market, credit, operational, liquidity risk) [3], CFP Board topics (tax, retirement, estate, insurance) [4], and Brazil's ANBIMA and Planejar certifications [5][6][7].
- Brazil's certification system changed in 2026: CPA-10, CPA-20 and CEA were replaced by CPA, C-Pro R and C-Pro I; CGA (fund managers) and CGE (structured-fund managers) remain [5][8]. Role cards reference the current names.
- Every agent shares common guardrails: cite sources, use tools for numbers, state confidence, flag jurisdiction (BR/US), and never execute transactions.
- **MVP recommendation (6 agents):** Chief of Staff/Orchestrator, CIO, Macro Economist (BR+US), Risk Officer, Red Team, and a combined Data Librarian/Reporting agent. Asset-class, tax and legal specialists come in phase 2.
- Specialists should get narrow briefs and only the tools they need; vague delegation is a documented cause of multi-agent failure [9][10].
- No AI role replaces licensed professionals for executing legal, tax-filing or regulated advice; the agents prepare analysis and questions for them.

## How human roles map to agent roles

Large single-family offices typically split staff between investment (CIO, analysts), risk, finance/reporting, tax and legal, and family governance. **Assumption:** a single-principal office would buy many of these services externally; the AI team covers the analysis and preparation layer. The UBS Global Family Office Report 2025 (317 family offices, average net worth USD 2.7bn) shows how broad the asset mix is: about 56% traditional and 44% alternative assets, with equities 30%, fixed income 18%, cash 8% and private equity 21%; Latin American offices held 71% in traditional assets [11]. This breadth is why the team needs both public-market and alternatives specialists.

| Layer | Human role | AI agent role |
|---|---|---|
| Coordination | Chief of Staff / family office COO | Chief of Staff / Orchestrator |
| Investment | CIO | Chief Investment Officer |
| Investment | Portfolio managers / analysts | Asset-class specialists (7), Quant/Portfolio Construction |
| Research | Economist, strategist | Macro Economist; Geopolitical & Political Analyst |
| Risk & challenge | CRO / risk manager; investment committee skeptic | Risk Officer; Devil's Advocate / Red Team |
| Advisory | Tax advisors (BR/US), lawyers, estate planner | Tax Specialist BR; Tax Specialist US; Legal/Structuring & Estate |
| Advisory | Governance / stewardship analyst, due diligence firm | Corporate Governance & Management Analyst; Due Diligence / Forensic Accounting |
| Operations | Controller, reporting | Reporting & Accounting |
| Operations | Data / IT | Data Engineer / Librarian |

## Shared guardrails for all agents

1. Every factual claim has a source (document, filing, data API) or is labeled as an assumption; NIST recommends verifying sources and citations in generative-AI output [12].
2. Numbers come from tools (data APIs, calculators, code), not model memory; models have memorized historical financial data and can mix memory with fresh reasoning [13].
3. State confidence as a probability; mark jurisdiction (BR, US, both) and currency (BRL, USD).
4. Never place orders, move money, sign documents, or contact third parties. The principal decides.
5. Never include the principal's identity, holdings or personal data in external searches.
6. Escalate to a licensed human professional when a question requires a legal opinion, tax filing, or regulated advice.
7. Say "insufficient data" rather than guess; on a filings benchmark, retrieval failures and hallucinations were common even for strong models [14].

## Role cards

Format for each card: **Mission · Core skills/knowledge · Inputs · Outputs · Tools/data · KPIs · Guardrails · Reference credentials.**

### 1. Chief of Staff / Orchestrator
- **Mission:** Turn every request, routine or alert into a plan, route it to the right agents, enforce deadlines and budgets, and assemble the final package.
- **Skills:** Task decomposition; writing precise briefs (objective, output format, tools, boundaries) [9]; effort scaling (simple questions get one agent, complex ones get several) [9]; knowledge of every role's scope; conflict detection between agents.
- **Inputs:** Principal requests, calendar, routine schedule, alerts, decision journal.
- **Outputs:** Task plans, daily brief, consolidated memo package, follow-up list, post-mortem schedule.
- **Tools/data:** Subagent spawning (Claude Agent SDK subagents [10]), task log, calendar, memory store.
- **KPIs:** On-time delivery; principal rating of usefulness; cost per request; rate of rework due to bad briefs.
- **Guardrails:** Cannot itself make investment recommendations; must route material decisions through Risk Officer and Red Team.

### 2. Chief Investment Officer (CIO)
- **Mission:** Own the Investment Policy Statement (IPS: the written rules for goals, risk limits, liquidity, allocation ranges), strategic and tactical allocation, and final synthesis of recommendations.
- **Skills:** CFA-level portfolio management, asset allocation, behavioral finance, ethics and professional standards [1]; alternatives allocation [2]; multi-currency (BRL/USD) and multi-jurisdiction portfolio thinking; weighing dissent.
- **Inputs:** Specialist findings, Macro view, Risk report, Red Team objections, IPS, portfolio state.
- **Outputs:** Recommendation memo, allocation targets, rebalancing proposals, IPS revision drafts.
- **Tools/data:** Portfolio analytics, scenario tool, decision journal.
- **KPIs:** Portfolio return vs policy benchmark (BRL and USD); risk-adjusted return; Brier score of forecasts; IPS compliance.
- **Guardrails:** Must show dissent; cannot override Risk Officer limit breaches without explicit principal approval.
- **Credentials:** CFA [1]; CAIA [2]; ANBIMA CGA for discretionary third-party fund management in Brazil [8].

### 3. Asset-class specialists

Common to all: **Mission** is to generate and maintain theses in their asset class; **outputs** are thesis files, buy/hold/sell views with probabilities, monitoring alerts; **KPIs** are forecast calibration, thesis hit rate vs benchmark, and error rate found by Red Team; **guardrails** are sourcing, tool-based numbers, and no execution.

| Specialist | Core skills and knowledge | Key inputs, tools and data | Reference body of knowledge |
|---|---|---|---|
| **Public equities (BR + US)** | Financial statement analysis, valuation (DCF, multiples), industry analysis, earnings quality; B3 and US market structure | SEC EDGAR and CVM filings, earnings transcripts, price and estimate data, valuation calculator | CFA equity and financial statement analysis topics [1] |
| **Fixed income and rates** | Yield curves, duration and convexity, credit spreads; Brazil: Selic, CDI (interbank rate most Brazilian fixed income is benchmarked against), Tesouro Direto bonds (Tesouro Selic floating, Prefixado fixed, IPCA+ inflation-linked, plus RendA+ and Educa+) [15]; bank CDBs, LCI/LCA, debentures; US Treasuries, TIPS, municipals, corporates | Curves (DI futures, US Treasuries), Tesouro Direto prices, bond calculator, rating data | CFA fixed income [1]; FRM valuation and credit risk [3] |
| **Real estate** | Cash-flow underwriting, cap rates, leverage, local market analysis (Brazil and Florida/US), REITs and Brazilian FIIs (listed real estate funds) | Property data, rent comps, loan calculator, FII/REIT filings | CAIA real assets / real estate [2] |
| **Private equity / VC** | Fund due diligence, J-curve, vintage diversification, valuation of private companies, terms (fees, carry, governance); Brazilian FIPs | Fund documents, capital-call schedules, benchmark data | CAIA private equity (VC, growth, buyouts) and private debt [2] |
| **Commodities / energy** | Supply-demand, futures curves (contango, backwardation), Brazil's commodity export exposure (agriculture, iron ore, oil) | Futures data, inventory and production reports | CAIA real assets / commodities [2] |
| **Crypto / digital assets** | Blockchain basics, custody risk, token economics, regulation in BR and US, ETF and fund wrappers | Exchange and on-chain data, custody documentation | CAIA digital assets [2] |
| **FX** | BRL/USD drivers (rate differentials, terms of trade, fiscal risk, flows), hedging instruments and costs, currency matching of liabilities (e.g., US study and living costs) | FX spot and forwards, central-bank data | CFA economics/currency topics [1]; FRM market risk [3] |

### 4. Quantitative / Portfolio Construction Analyst
- **Mission:** Turn views into sized, diversified portfolios and test them.
- **Skills:** Statistics and quantitative methods [1][3], mean-variance and risk-parity construction, factor exposure, backtesting with point-in-time data, rebalancing math, transaction-cost and tax-aware rebalancing.
- **Inputs:** Views and probabilities from specialists, IPS constraints, holdings.
- **Outputs:** Proposed weights, efficient-frontier and scenario charts, backtest reports with bias disclosures.
- **Tools/data:** Python sandbox, price history including delisted securities, portfolio analytics.
- **KPIs:** Tracking of realized vs predicted risk; backtest-to-live gap.
- **Guardrails:** Must disclose survivorship and look-ahead risks; may not present LLM-driven backtests on pre-training-cutoff periods as evidence of skill, since published LLM strategy advantages faded under broader tests [16] and memorization inflates results [13].

### 5. Risk Officer
- **Mission:** Independently measure and limit portfolio risk; sign off on every material recommendation.
- **Skills:** FRM body of knowledge: foundations of risk management, quantitative analysis, valuation and risk models, market risk, credit risk, operational risk and resilience, liquidity and treasury risk [3]; stress testing (Brazil fiscal shock, US rate shock, BRL crisis); concentration and counterparty risk (brokers, custodians, banks in both countries).
- **Inputs:** Holdings, proposed trades, market data, IPS limits.
- **Outputs:** Risk dashboard, limit-breach alerts, pre-trade risk sign-off, stress-test report.
- **Tools/data:** VaR and drawdown calculators, scenario engine, exposure aggregation by asset/currency/country/counterparty.
- **KPIs:** Breaches caught before decision; realized drawdowns within policy; stress-test coverage.
- **Guardrails:** Independent from CIO; veto on limit breaches, overridable only by principal with logged reason.
- **Credentials:** FRM [3].

### 6. Macro Economist (Brazil, US, global)
- **Mission:** Provide base, bull and bear macro scenarios with probabilities and their implications by asset class.
- **Skills:** Monetary policy (Copom/Banco Central do Brasil, Federal Reserve), inflation (IPCA, CPI), fiscal dynamics, growth cycles, trade and capital flows; CFA economics topics [1].
- **Inputs:** Official statistics, central-bank communications, market-implied expectations, Geopolitical analyst inputs.
- **Outputs:** Daily macro note, monthly scenario deck, event previews (Copom, FOMC, data releases).
- **Tools/data:** Macro data APIs, yield-curve data, economic calendar.
- **KPIs:** Brier score on scenario and event calls; usefulness rating.
- **Guardrails:** Must distinguish consensus from own view; must not present memorized past data as current [13].

### 7. Geopolitical and Political Analyst (Brazil, US, global)
- **Mission:** Track elections, policy, legislation, sanctions, conflicts and trade disputes, and translate them into market risk.
- **Skills:** Brazilian politics (Congress, federal/state dynamics, fiscal reform), US politics (Congress, executive actions, trade/tariff policy), global hotspots; scenario analysis and base rates.
- **Inputs:** News feeds, legislative trackers, polls, official statements.
- **Outputs:** Political risk register, event-probability forecasts, alerts.
- **Tools/data:** News search, legislative databases, prediction-market or poll data where available.
- **KPIs:** Brier score; lead time of alerts.
- **Guardrails:** Neutral, non-partisan language; separate facts from forecasts; cite sources with dates.

### 8. Tax Specialist — Brazil
- **Mission:** Estimate tax effects of decisions for a Brazilian tax resident with foreign assets.
- **Skills:** Brazilian income tax on investments, foreign-asset reporting, fund taxation, monthly equity gains rules, annual DIRPF filing logic; interaction with the US.
- **Inputs:** Statements, cost basis, entity structure, proposed transactions.
- **Outputs:** Tax impact estimates per memo, tax calendar, questions for the principal's accountant.
- **Tools/data:** Tax calculators, official Receita Federal guidance (retrieved, dated).
- **KPIs:** Estimate accuracy vs final filings; deadlines met.
- **Guardrails:** Estimates only; filings and opinions by a licensed accountant/lawyer; always cite the rule version and date because tax law changes.

### 9. Tax Specialist — United States
- **Mission:** Estimate US tax consequences, including residency status questions for someone with US ties.
- **Skills:** Tax planning topics in the CFP body of knowledge (14% of the exam) [4]; US residency tests for non-citizens, withholding on US-source income, estate tax exposure for non-residents, foreign-account reporting; treaty considerations.
- **Inputs, outputs, tools:** As for the Brazil tax role, with IRS guidance.
- **KPIs, guardrails:** As above; must flag cross-border double-taxation issues to both tax agents.

### 10. Legal / Structuring and Estate Planning
- **Mission:** Analyze holding structures (Brazilian holdings, US LLCs/trusts, offshore vehicles), succession and estate plans, and contract terms.
- **Skills:** Estate planning topics from the CFP body of knowledge (titling, beneficiary designations, transfer strategies, estate/incapacity documents, gift and estate tax) [4]; Brazilian succession law and inheritance tax concepts; asset protection; insurance planning.
- **Inputs:** Entity documents, wills, contracts, family goals.
- **Outputs:** Structure comparison tables, issue lists for counsel, document checklists.
- **Tools/data:** Document library (RAG), legal databases.
- **KPIs:** Issues identified before counsel review; documents up to date.
- **Guardrails:** Not legal advice; every output ends with questions for licensed counsel in the relevant jurisdiction.
- **Credentials:** CFP (US, CFP Board) [4]; CFP in Brazil is awarded by Planejar under license from FPSB [7].

### 11. Corporate Governance and Management Analyst (CEO profiling)
- **Mission:** Assess the quality and incentives of management and boards for holdings and targets.
- **Skills:** Reading proxy statements and Brazilian reference forms, executive compensation design, capital allocation track record, related-party transactions, controlling-shareholder dynamics (common in Brazil), board independence; structured CEO profiles (career, tenure, past outcomes, public statements vs results).
- **Inputs:** Filings (SEC, CVM), earnings calls, news, shareholder letters.
- **Outputs:** CEO and board profiles, governance scorecard, red-flag alerts (departures, insider selling).
- **Tools/data:** Filings search, transcripts, news.
- **KPIs:** Red flags identified before price impact; profile accuracy.
- **Guardrails:** Public, professional information only; no speculation about private lives; label opinions.

### 12. Due Diligence / Forensic Accounting Analyst
- **Mission:** Verify claims and detect accounting or fraud risk in companies, funds and deals.
- **Skills:** Financial statement analysis, earnings-quality and accrual analysis, cash-flow vs earnings divergence, auditor changes, fund operational due diligence; CAIA hedge fund and private equity due diligence topics [2].
- **Inputs:** Financial statements, footnotes, fund documents, background information.
- **Outputs:** Due diligence reports with red/amber/green ratings.
- **Tools/data:** Filings, ratio calculators, Python.
- **KPIs:** Issues found; false-alarm rate.
- **Guardrails:** Distinguish evidence from suspicion; never accuse publicly.

### 13. Devil's Advocate / Red Team
- **Mission:** Find what is wrong with every material recommendation before money is committed.
- **Skills:** Premortem technique, base rates, cognitive-bias checklists, independent fact-checking with tools; awareness that multi-agent debate adds little unless the critic brings different information or a different model [17].
- **Inputs:** Draft memo, sources, tool outputs.
- **Outputs:** Objection list ranked by severity, verified/unverified claims table, kill criteria.
- **Tools/data:** Same data access as specialists, plus independent recalculation.
- **KPIs:** Material errors caught; share of post-mortem failure causes that the Red Team had flagged.
- **Guardrails:** Must argue the opposite case even when it agrees; cannot be overruled silently (dissent appears in the memo).

### 14. Reporting and Accounting
- **Mission:** Produce accurate consolidated reporting across accounts, currencies and countries.
- **Skills:** Performance measurement (time- and money-weighted returns), multi-currency consolidation, cost-basis tracking, reconciliation.
- **Inputs:** Statements, transaction records, price data.
- **Outputs:** Monthly/quarterly reports, net-worth statement in BRL and USD, memo formatting.
- **Tools/data:** Portfolio accounting database, FX rates, reconciliation scripts.
- **KPIs:** Reconciliation breaks; report timeliness; errors found by principal.
- **Guardrails:** Never estimate a balance that should be reconciled; flag missing statements.

### 15. Data Engineer / Librarian
- **Mission:** Own the document library, data pipelines, memory store, logs and evals.
- **Skills:** Document ingestion and metadata tagging, embeddings and search configuration, point-in-time data storage, access control, audit logging, eval maintenance.
- **Inputs:** Raw documents, API feeds, agent outputs.
- **Outputs:** Searchable library, clean datasets, decision-journal records, data-quality reports.
- **Tools/data:** Storage, vector index (database for embeddings), API connectors, logging.
- **KPIs:** Retrieval accuracy on eval set; data freshness; zero unauthorized access.
- **Guardrails:** Encrypt sensitive data; minimum-necessary access per agent; retention and deletion on principal request.

## Certifications as skill blueprints

| Credential | Body | What it signals for agent design |
|---|---|---|
| CFA | CFA Institute | Ethics, quantitative methods, economics, financial statement analysis, equity, fixed income, derivatives, alternatives, portfolio management [1] |
| CAIA | CAIA Association | Alternatives: real assets, private equity, private debt, hedge funds, digital assets [2] |
| FRM | GARP | Part I: foundations, quantitative analysis, markets and products, valuation and risk models; Part II: market, credit, operational, liquidity risk, investment management [3] |
| CFP (US) | CFP Board | Eight domains incl. investment planning 17%, retirement 18%, tax 14%, estate 10%, risk management/insurance 11%, psychology of financial planning 7% [4] |
| CFP (Brazil) | Planejar (FPSB affiliate) | Brazilian financial planning, in Portuguese [7] |
| CPA, C-Pro R, C-Pro I | ANBIMA | Distribution and advisory certifications replacing CPA-10/CPA-20/CEA from 2026; holders of old titles in transition until 31 Dec 2026 [5][8] |
| CGA, CGE | ANBIMA | CGA: managers of fixed income, equity, multimarket and FX funds; CGE: managers of structured funds (FIIs, FIPs, FIDCs) [5][8] |
| CVM consultant authorization | CVM (Resolução CVM 19) | Securities consultants need a degree, clean reputation and an approved certification exam [6]; CVM has accepted CEA and CGA, and ANBIMA reports C-Pro R and C-Pro I are now accepted [18] |

**Assumption:** CVM and ANBIMA rules continue to evolve; the Regulatory agent must re-verify certification and licensing requirements before relying on them.

## MVP: which roles to build first

**Recommendation:** build six agents first.

| Priority | Agent | Why first |
|---|---|---|
| 1 | Chief of Staff / Orchestrator | Every workflow depends on triage, briefs and assembly; orchestrator-plus-specialists is the proven base pattern [9]. |
| 2 | Data Librarian + Reporting (combined) | Without a clean document library and consolidated holdings, every other agent hallucinates or uses stale data [14]. |
| 3 | CIO | Owns the IPS and synthesis; the principal needs one integrated view. |
| 4 | Macro Economist (BR + US) | Drives the daily brief and most allocation decisions for a BRL/USD investor. |
| 5 | Risk Officer | Independent check; limits and stress tests protect against the largest mistakes. |
| 6 | Red Team | Cheapest way to catch errors; must be built from day one so the habit of challenge is embedded. |

**Optional 7th:** a combined Fixed Income and FX specialist, because Brazilian CDI/Tesouro instruments and BRL/USD exposure are likely the largest decisions for a Brazil-based investor with US expenses. **Assumption:** this reflects a typical Brazilian portfolio; confirm with the principal's actual holdings.

**Phase 2:** Equities, Tax BR, Tax US, Geopolitical/Political, Governance/CEO. **Phase 3:** Real estate, PE/VC, Commodities, Crypto, Legal/Estate, Due Diligence, Quant.

## Implications for the agent team

- Each role card becomes a subagent definition (name, description, instructions, allowed tools) in the Claude Agent SDK [10].
- The Chief of Staff routes by the role scopes above; overlapping scopes must be resolved in the card text to avoid duplicated work [9].
- Use role heterogeneity (different prompts, data and possibly models) for Red Team vs CIO to get real disagreement [17].
- All KPIs feed the calibration scorecard defined in file 03.
- Tax and legal agents always produce questions for licensed humans, not conclusions.

## Open questions and assumptions

- Which professional advisors (accountant, lawyers in BR and US) will receive agent outputs, and in what format?
- What is the principal's US tax status? This determines the scope of the US Tax agent.
- Budget for data subscriptions determines whether asset-class specialists can be built well.
- **Assumption:** the principal's portfolio is primarily Brazilian fixed income, equities and USD assets; adjust MVP if real estate or private holdings dominate.
- **Assumption:** certification curricula are used as skill checklists only; agents do not hold or claim credentials.

## Sources

1. CFA Program Curriculum, CFA Institute, 2026, https://www.cfainstitute.org/programs/cfa-program/curriculum (accessed 2026-11-27)
2. CAIA Exam Curriculum Overview, CAIA Association, 2026, https://caia.org/caia-exam-curriculum (accessed 2026-11-27)
3. FRM Program Exams, GARP, 2026, https://www.garp.org/frm/program-exams (accessed 2026-11-27)
4. 2021 Principal Knowledge Topics, CFP Board, 2021, https://www.cfp.net/-/media/files/cfp-board/cfp-certification/2021-practice-analysis/2021-principal-knowledge-topics.pdf (accessed 2026-11-27)
5. Transição para as novas certificações, ANBIMA, 2025–2026, https://www.anbima.com.br/pt_br/especial/transicao-novas-certificacoes.htm (accessed 2026-11-27)
6. Consultor de Valores Mobiliários, Portal do Investidor, CVM / gov.br, https://www.gov.br/investidor/pt-br/investir/como-investir/profissionais-do-mercado/consultor-de-valores-mobiliarios (accessed 2026-11-27)
7. Manual de Certificação CFP, Planejar, 2023, https://planejar.org.br/wp-content/uploads/2023/12/planejar_MANUAL-CERTIFICACAO-NOV2023.pdf (accessed 2026-11-27)
8. Equivalência entre certificações: o que muda com a chegada das novas CPA, C-Pro R e C-Pro I, ANBIMA, 2025, https://www.anbima.com.br/pt_br/noticias/equivalencia-entre-certificacoes-o-que-muda-com-a-chegada-das-novas-cpa-c-pro-r-e-c-pro-i.htm (accessed 2026-11-27)
9. How we built our multi-agent research system, Anthropic, 2025, https://www.anthropic.com/engineering/multi-agent-research-system (accessed 2026-11-27)
10. Subagents in the SDK, Claude Agent SDK documentation, Anthropic, 2025–2026, https://code.claude.com/docs/en/agent-sdk/subagents (accessed 2026-11-27)
11. Global Family Office Report 2025, UBS, 2025, https://www.ubs.com/global/en/media/display-page-ndp/en-20250521-global-family-office-report-2025.html (accessed 2026-11-27)
12. NIST AI 600-1, Generative Artificial Intelligence Profile, NIST, 2024, https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf (accessed 2026-11-27)
13. Lopez-Lira, Tang, Zhu, The Memorization Problem: Can We Trust LLMs' Economic Forecasts?, arXiv, 2025, https://arxiv.org/abs/2504.14765 (accessed 2026-11-27)
14. Islam et al., FinanceBench: A New Benchmark for Financial Question Answering, arXiv, 2023, https://arxiv.org/abs/2311.11944 (accessed 2026-11-27)
15. Tesouro Selic, Prefixado, IPCA+, Renda+ ou Educa+: saiba as diferenças, B3 Bora Investir, https://borainvestir.b3.com.br/tipos-de-investimentos/renda-fixa/tesouro-direto/tesouro-selic-prefixado-ipca-renda-ou-educa-saiba-as-diferencas-e-como-escolher-o-melhor-para-voce/ (accessed 2026-11-27)
16. Li, Kim, Cucuringu, Ma, Can LLM-based Financial Investing Strategies Outperform the Market in Long Run? (FINSABER), arXiv / KDD 2026, 2025, https://arxiv.org/abs/2505.07078 (accessed 2026-11-27)
17. Zhang et al., Stop Overvaluing Multi-Agent Debate: We Must Rethink Evaluation and Embrace Model Heterogeneity, arXiv, 2025, https://arxiv.org/abs/2502.08788 (accessed 2026-11-27)
18. C-Pro R e C-Pro I passam a ser aceitas pela CVM para consultores de valores mobiliários, ANBIMA, 2025–2026, https://www.anbima.com.br/pt_br/noticias/c-pro-r-e-c-pro-i-passam-a-ser-aceitas-pela-cvm-para-consultores-de-valores-mobiliarios.htm (accessed 2026-11-27)
