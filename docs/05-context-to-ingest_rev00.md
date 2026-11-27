# Context the AI Family Office Must Ingest

> **Purpose:** An inventory of what the agent team must know about the principal, their balance sheet, documents, the outside world and past decisions, plus how to keep it current, structure it and protect it. **Primary users:** the orchestrator/chief-of-staff agent, portfolio and risk agents, tax and estate agents, the data-engineering agent, and any agent that writes recommendations.

## Summary

- Advice is only as good as the context behind it. The agents need five layers of context: **the principal**, **the balance sheet**, **documents**, **external context** (markets, macro, news, regulation) and **operating memory** (decisions, outcomes, learned preferences).
- The principal profile should follow the same factors regulators require human advisors to collect. In Brazil, that is the suitability duty under CVM Resolution 30/2021 [1][2]. In the US, it is FINRA Rule 2111's "investment profile" (age, other investments, financial situation and needs, tax status, objectives, experience, time horizon, liquidity needs, risk tolerance) [3], which Regulation Best Interest (Reg BI) now supersedes for broker-dealer recommendations [4].
- A written **Investment Policy Statement (IPS)**, a rulebook for how money is invested, is the single most useful document to give the agents. The CFA Institute's template for individual investors is a good base [5].
- Keep data current with automated feeds. In Brazil, use **Open Finance Brasil**, which has covered investment data since its fourth phase and needs a specific, revocable consent [6][7]. In the US, use aggregators such as **Plaid Investments**, which return holdings, cost basis and up to 24 months of investment transactions [8]. The US open-banking rule (CFPB Section 1033) is stayed and being rewritten, so do not rely on it yet [9][10].
- Store context in three linked stores: a **portfolio database** (structured numbers), a **document store with retrieval** (contracts, statements, returns) and a **knowledge base** (profile, IPS, decision journal).
- Share by need-to-know. Most agents need positions and exposures, not account numbers, tax IDs or full names. Brazilian law (LGPD) does not list financial data as "sensitive personal data," but bank secrecy (LC 105/2001) still applies, and practitioners advise extra care [13][14]. Treat it as highly sensitive anyway.

## 1. Context inventory

**Priority:** Must = agents cannot give sound advice without it; Should = materially improves advice; Could = nice to have.
**Sensitivity:** S1 public, S2 internal, S3 confidential (financial detail), S4 restricted (identifiers, credentials, legal and estate documents, health).

### 1.1 About the principal

| Item | Priority | Source | Update frequency | Sensitivity |
|---|---|---|---|---|
| Goals (e.g., grow capital, fund education, buy property, exit a business) with amounts and dates | Must | Interview with principal; IPS | Annually and at life events | S3 |
| Time horizon per goal (short <2y, medium 2–7y, long >7y) | Must | Interview; IPS | Annually | S3 |
| Liquidity needs: monthly spending, tuition, reserves for operating businesses, capital calls | Must | Cash-flow records; budgets | Quarterly | S3 |
| Risk tolerance (willingness to take risk) | Must | Suitability-style questionnaire (see 1.2) | Annually; after big market moves | S3 |
| Risk capacity (ability to absorb losses without changing goals) | Must | Computed from balance sheet and income stability | Quarterly | S3 |
| Investment knowledge and experience by product type | Must | Questionnaire | Annually | S2 |
| Tax residency and status (Brazil, US, any treaty or dual-status issues, entity tax status) | Must | Tax advisors; returns; visa or residency status | Annually and on any move | S4 |
| Family structure: spouse/partner, children, dependants, marital property regime | Must | Principal; legal documents | At life events | S4 |
| Succession and estate goals (who inherits what, control of operating businesses, philanthropy) | Should | Principal; estate counsel | Annually | S4 |
| Values and ESG preferences (exclusions, impact themes, sectors to favor or avoid) | Should | Interview; IPS | Annually | S2 |
| Currency of consumption (BRL vs USD spending split) | Must | Cash-flow records | Annually | S3 |
| Communication preferences (detail level, language, alert thresholds) | Could | Principal; learned over time | Ongoing | S2 |

### 1.2 How to measure risk tolerance and capacity

Use a questionnaire that maps to both regulatory regimes, so agent outputs speak the same language as the principal's banks and brokers.

- **Brazil (CVM Resolution 30/2021):** firms must verify that products, services and operations suit the client's profile, based on the client's **objectives, financial situation and knowledge of products** [1]. CVM 30 replaced Instruction CVM 539/2013. A CVM impact review published in January 2025 found the rule effective but below its potential, and suggested sharing risk-profile data through Open Finance [2]. Brazilian brokers typically sort clients into conservative / moderate / aggressive profiles. **Assumption:** the three-profile labels are market practice, not a term the rule mandates.
- **US (FINRA Rule 2111 and Reg BI):** Rule 2111's investment profile lists age, other investments, financial situation and needs, tax status, investment objectives, investment experience, time horizon, liquidity needs and risk tolerance [3]. FINRA states that Rule 2111 no longer applies to recommendations covered by Reg BI (SEA Rule 15l-1), which uses a best-interest standard [4].

**Recommended scoring (Estimate:** a practical design, not a regulatory requirement):
1. **Willingness score (1–5):** questions on reaction to a 20% drawdown, preference between certain and uncertain outcomes, and past behavior in sell-offs.
2. **Capacity score (1–5):** computed by agents from liquid net worth ÷ annual spending, income stability (operating business cash flows), debt service coverage, and concentration in the operating businesses.
3. **Final profile = the lower of the two.** Record both scores, the date and the answers in the knowledge base.
4. **Knowledge flags by product** (equities, fixed income, funds, derivatives, private equity, crypto, real estate funds), mirroring the CVM 30 "knowledge" factor [1].

### 1.3 Balance sheet

| Item | Priority | Source | Update frequency | Sensitivity |
|---|---|---|---|---|
| Holdings at brokers and banks (BR and US), by security, quantity, price, currency | Must | Open Finance Brasil; Plaid/aggregator; broker statements | Daily (automated) / monthly (statements) | S3 |
| Cost basis and tax lots (purchase date, price, fees) | Must | Broker tax-lot reports; Plaid holdings cost basis [8]; Brazilian broker "notas de corretagem" | On every trade | S3 |
| Cash and deposits; FX positions | Must | Bank feeds | Daily | S3 |
| Operating businesses (hospitality, energy): ownership %, valuation, EBITDA, debt, capex plans, dividends | Must | Management accounts; auditors; shareholder agreements | Monthly (management accounts), annually (valuation) | S3–S4 |
| Other private company stakes and funds (PE/VC commitments, capital calls, NAV) | Should | GP reports; capital-call notices | Quarterly | S3 |
| Real estate: address class, value, rent, mortgage, expenses | Must | Appraisals; leases; tax assessments | Annually | S3 |
| Debt: loans, guarantees given (often by the principal for operating businesses), covenants | Must | Loan agreements; bank statements | Monthly | S3 |
| Insurance: life, property, D&O, liability, health; insured amounts, beneficiaries | Should | Policies | Annually | S4 |
| Legal entities: holdings, LLCs, trusts, foundations; ownership chart; jurisdiction; tax treatment | Must | Corporate documents; counsel | At changes | S4 |
| Cash-flow forecast: personal and business distributions, tuition, taxes | Must | Budgets; agents' model | Monthly | S3 |
| Crypto and other assets (art, vehicles) | Could | Wallet reads; appraisals | Quarterly | S3 |

### 1.4 Documents

| Document | Priority | Source | Update frequency | Sensitivity |
|---|---|---|---|---|
| Broker and bank statements (monthly) | Must | Institutions' portals | Monthly | S3 |
| Tax returns: Brazil (DIRPF, company returns), US (Form 1040/1040-NR and related forms, if filing) | Must | Accountants | Annually | S4 |
| Shareholder agreements, bylaws, operating agreements | Must | Counsel | At changes | S4 |
| Loan, lease, PPA and concession contracts of the operating businesses | Should | Business management | At changes | S3–S4 |
| Wills, trust deeds, prenuptial or marital regime documents, powers of attorney | Should | Estate counsel | At changes | S4 |
| Insurance policies | Should | Brokers | Annually | S4 |
| Fund documents (regulations, subscription agreements, LPAs) | Should | GPs/administrators | At subscription | S3 |
| Past advisor reports and IPS versions | Could | Advisors | As issued | S3 |

### 1.5 External context

| Item | Priority | Source (detail in file 12) | Update frequency | Sensitivity |
|---|---|---|---|---|
| Market prices (BR and US equities, rates, FX, commodities incl. energy) | Must | Market-data APIs | Intraday / daily | S1 |
| Macro data and expectations (Selic, IPCA, Focus survey, Fed funds, CPI, payrolls) | Must | BCB SGS/Olinda [16], FRED, BLS | Daily–monthly | S1 |
| Company filings (10-K/10-Q/8-K; DFP/ITR/fatos relevantes) | Must | SEC EDGAR [15]; CVM | As filed | S1 |
| News and sentiment | Should | News APIs | Continuous | S1 |
| Regulatory feeds (Federal Register, Diário Oficial, CVM, BCB, Receita Federal, energy and tourism regulators) | Must for sectors held | Official feeds | Daily | S1 |
| Geopolitical risk indices | Should | GPR, EPU, GDELT, ACLED | Daily–monthly | S1 |
| Sector data for hospitality and energy (occupancy, tariffs, auctions, power prices) | Should | Industry and regulator data | Monthly | S1 |
| Broker and independent research | Could | Subscriptions | As issued | S2 (licensed) |

### 1.6 Operating context (memory)

| Item | Priority | Source | Update frequency | Sensitivity |
|---|---|---|---|---|
| Decision journal: date, question, options, recommendation, rationale, decision taken, expected outcome, review date | Must | Agents + principal | Every decision | S3 |
| Recommendation outcomes vs. benchmark (did it work, and why) | Must | Portfolio DB + journal | At review dates | S3 |
| Learned preferences ("dislikes leverage above X", "wants USD reserve of Y months") | Should | Conversation history, confirmed by principal | Ongoing | S2–S3 |
| Open tasks, watchlists, alerts and thresholds | Should | Agents | Ongoing | S2 |
| Advisor and counterparty roster (banks, lawyers, accountants) | Should | Principal | At changes | S3 |

## 2. Keeping context current

### 2.1 Brazil: Open Finance Brasil

- Open Finance Brasil rolled out in phases. The fourth phase, sometimes called "Open Investment," added sharing of investment data between participating institutions [6].
- Consent must be free, informed, prior and unambiguous, given electronically for a defined purpose [7]. A consent given earlier for another purpose (e.g., credit) does not cover investments; a new, specific consent is needed [6].
- Agents cannot join Open Finance directly. Access normally goes through a regulated aggregator. Examples: **Pluggy**, which says it aggregates balances, statements, cards and investments from 130+ institutions through one API [11], and **Belvo** [12]. **Assumption:** the principal's main banks and brokers have implemented the investment endpoints. Confirm institution by institution.
- Backstop: monthly PDF statements and broker trade notes, parsed into the portfolio database.

### 2.2 US: account aggregation

- **Plaid Investments** returns holdings (quantity, price, value, cost basis, currency) and up to 24 months of investment transactions. Updates usually happen overnight; an on-demand refresh is a paid add-on [8].
- Regulatory backdrop: the CFPB's Section 1033 "personal financial data rights" rule is on the books but its compliance dates were stayed by a federal court in October 2025 [9]. A reconsideration proposal was sent for White House (OIRA) review in August 2026 [10]. Expect aggregator terms and fees to change.
- Alternatives: direct broker APIs or file exports (CSV/OFX) where aggregators are weak.

### 2.3 Pipeline design (Estimate: reference architecture)

1. **Ingest:** scheduled jobs pull aggregator data (daily), statements (monthly), market and macro data (daily), filings and regulatory feeds (daily).
2. **Normalize:** map every position to one security master (ISIN/CUSIP/B3 ticker), one currency table and one entity tree.
3. **Reconcile:** compare aggregator positions with statements monthly; flag breaks over a tolerance.
4. **Snapshot:** keep a dated snapshot of positions and NAV each day so agents can answer "what did we own on date X?"
5. **Alert:** stale-data warnings when any feed is older than its expected frequency.

## 3. How to structure the context

| Store | What goes in | Plain-language explanation | Who reads it |
|---|---|---|---|
| **Portfolio database** (relational, e.g., Postgres) | Securities, positions, tax lots, transactions, prices, FX, entities, cash flows | Tables of numbers that can be summed and filtered exactly | Portfolio, risk, tax agents |
| **Document store with retrieval** | PDFs and scans of statements, contracts, returns, policies | "Retrieval" (often called RAG, retrieval-augmented generation) means the system searches the documents and hands the AI only the relevant passages, rather than everything | Legal, tax, estate agents |
| **Knowledge base** (versioned Markdown or wiki) | Principal profile, IPS, decision journal, learned preferences, glossary | Human-readable files that the principal can review and correct | All agents |
| **External data cache** | Market, macro, filings, news | Local copies so agents do not re-download and can cite the version used | Research agents |

Rules: each fact has one "home" store; every number shown to the principal has a source and an "as of" date; the IPS and profile are versioned, so old decisions can be judged against the rules in force at the time.

## 4. What to share with the AI vs. redact

- **Legal context:** under Brazil's LGPD (Law 13,709/2018), financial data is personal data but is not on the closed list of "sensitive personal data" in Article 5, II. Commentators still advise special care because financial data can reveal sensitive data, and bank secrecy (LC 105/2001) also applies [13][14].
- **Principle (Assumption: house policy recommended for this office):**

| Data | Share with agents? | How |
|---|---|---|
| Positions, weights, exposures, P&L | Yes | Full detail in portfolio DB |
| Account numbers, tax IDs (CPF, SSN/ITIN), passport numbers | No | Replace with tokens (e.g., ACCT_BR_01) |
| Login credentials, tokens, passwords | Never | Kept in a secrets vault; only the pipeline uses them |
| Names of family members | Minimal | Use roles ("Child 1") except in estate work |
| Contracts and estate documents | Only to legal/estate agents | Retrieval with per-agent access rules |
| Health information (for insurance) | Only when needed | Summarized, not raw |
| Operating business financials | Yes, to relevant agents | Aggregated monthly; raw ledgers only on request |

Other controls: log every agent access to S4 data; prefer providers with zero-retention or no-training terms; keep a human approval step before any external sharing.

## 5. Templates

### 5.1 Investment Policy Statement outline

Based on the CFA Institute's elements for individual investors (scope and purpose, governance, investment objectives, risk, constraints, monitoring) [5], adapted for a Brazil/US principal.

1. **Scope and purpose:** which assets and entities the IPS governs (and which it excludes, e.g., the operating businesses' working capital).
2. **Governance:** who decides (principal), who advises (agent team, human advisors), approval thresholds, how and when the IPS is reviewed.
3. **Principal background:** summary of the principal profile (5.2).
4. **Investment objectives:** return target (real, in BRL and in USD), by goal bucket.
5. **Risk:** risk profile (willingness, capacity, final), maximum acceptable drawdown, volatility range, loss limits per position.
6. **Constraints:**
   - Time horizon by bucket
   - Liquidity: minimum cash reserve (months of spending), business support reserve
   - Taxes: residency, entity structure, tax-lot rules, treaty considerations
   - Legal/regulatory: product eligibility (e.g., qualified/professional investor status in Brazil; accredited investor status in the US)
   - Unique circumstances: concentration in hospitality and energy; correlation of portfolio with operating businesses
7. **Currency policy:** target BRL/USD split and hedging rules.
8. **Strategic asset allocation:** target weights and ranges by asset class and jurisdiction.
9. **Rebalancing rules:** calendar and band triggers.
10. **Permitted and prohibited investments:** including ESG exclusions, leverage limits, derivatives use.
11. **Manager and product selection criteria:** fees, liquidity terms, custody.
12. **Monitoring and reporting:** benchmarks, reporting frequency, review triggers.
13. **Signatures, version and date.**

### 5.2 Principal profile (read by all agents)

```markdown
# Principal Profile  v<N>  (as of YYYY-MM-DD)
## Identity (tokenized)
- ID: PRINCIPAL_01 | Tax residency: <BR / US / both - per advisors> | Base currencies: BRL, USD
## Goals
| Goal | Amount | Currency | Target date | Priority |
## Time horizon buckets
- Short (<2y): ... | Medium (2-7y): ... | Long (>7y): ...
## Liquidity
- Monthly spending: ... | Reserve target: N months | Known outflows: tuition, capex, capital calls
## Risk
- Willingness score (1-5): ... | Capacity score (1-5): ... | Final profile: ...
- Max drawdown tolerated: ...% | Date of last questionnaire: ...
## Knowledge and experience by product
## Values / ESG
- Exclusions: ... | Themes to favor: ...
## Family and succession (summary only; details in restricted store)
## Operating businesses (summary)
- Hospitality: ... | Energy: ... | Personal guarantees: ...
## Communication preferences
- Language: ... | Detail level: ... | Alert thresholds: ...
## Hard rules for agents
- e.g., "Never recommend leverage above X", "Escalate any decision > R$ Y to principal"
## Change log
```

## Implications for the agent team

- The orchestrator must refuse to give allocation advice when Must items (goals, horizon, liquidity, risk profile, tax residency) are missing or stale, and should ask for them.
- Every recommendation must state the IPS version and profile version it relied on, and be written to the decision journal.
- Risk agents should treat the operating businesses as part of the portfolio: hospitality and energy exposure is already large before any listed investment.
- Tax agents must work at the tax-lot level and by entity; aggregated positions are not enough.
- Data agents own freshness monitoring and reconciliation; other agents must show "as of" dates.
- Access control is per agent: legal/estate agents see S4 documents; market agents never do.

## Open questions and assumptions

- Exact tax residency and filing status of the principal (Brazil, US or both) must be confirmed by tax advisors; it drives the whole tax layer.
- Which of the principal's institutions expose investment data through Open Finance Brasil and Plaid is unverified.
- The outcome of the CFPB Section 1033 rewrite (fees, scope) is unknown as of this writing [10].
- **Assumption:** the operating businesses can provide monthly management accounts in a consistent format.
- **Assumption:** the principal will complete the questionnaire and review the profile and IPS at least annually.
- Whether the principal qualifies as a qualified/professional investor (Brazil) or accredited investor (US) is not yet known and affects which products agents may consider.

## Sources

1. Resolution CVM 30 (English version), Comissão de Valores Mobiliários, 2021, https://www.gov.br/cvm/en/foreign-investors/regulation-files/RESOLUTIONCVM30_.pdf (accessed 2026-11-27)
2. "Estudo sobre eficácia da CVM 30, de suitability, aponta melhorias para a norma," Capital Aberto, 2025, https://capitalaberto.com.br/regulacao/2025/01/estudo-sobre-cvm-30-aponta-melhorias-para-a-norma (accessed 2026-11-27)
3. FINRA Rule 2111 (Suitability) FAQ, FINRA, n.d., https://www.finra.org/rules-guidance/key-topics/suitability/faq (accessed 2026-11-27)
4. Suitability (key topic page), FINRA, n.d., https://www.finra.org/rules-guidance/key-topics/Suitability (accessed 2026-11-27)
5. Elements of an Investment Policy Statement for Individual Investors, CFA Institute, 2010, https://rpc.cfainstitute.org/-/media/documents/article/position-paper/investment-policy-statement-individual-investors.pdf (accessed 2026-11-27)
6. "Open Investments: nova etapa do Open Finance agora abarca os investidores," InfoMoney, n.d., https://www.infomoney.com.br/minhas-financas/open-investments-nova-etapa-do-open-finance-agora-abarca-os-investidores-veja-o-que-muda-na-pratica/ (accessed 2026-11-27)
7. Resolução Conjunta nº 1 (Open Finance), Banco Central do Brasil / CMN, consolidated version, https://normativos.bcb.gov.br/Lists/Normativos/Attachments/51028/Res_Conj_0001_v9_L.pdf (accessed 2026-11-27)
8. Investments (product documentation), Plaid, n.d., https://plaid.com/docs/investments/ (accessed 2026-11-27)
9. Personal financial data rights (compliance page), Consumer Financial Protection Bureau, n.d., https://www.consumerfinance.gov/compliance/compliance-resources/other-applicable-requirements/personal-financial-data-rights/ (accessed 2026-11-27)
10. "CFPB sends new Section 1033 open banking proposal to OIRA for review," Consumer Finance Monitor (Ballard Spahr), 2026, https://www.consumerfinancemonitor.com/2026/08/06/cfpb-sends-new-section-1033-open-banking-proposal-to-oira-for-review/ (accessed 2026-11-27)
11. "Fintech Pluggy capta US$ 3,5 milhões de olho em novos produtos," Finsiders Brasil, 2026, https://finsidersbrasil.com.br/negocios-em-fintechs/fintech-pluggy-capta-us-35-milhoes-de-olho-em-novos-produtos/ (accessed 2026-11-27)
12. "Belvo lança solução de Open Finance para instituições reguladas," Finsiders Brasil, n.d., https://finsidersbrasil.com.br/reportagem-exclusiva-fintechs/belvo-lanca-solucao-de-open-finance-para-instituicoes-reguladas (accessed 2026-11-27)
13. "Dados pessoais bancários são considerados dados sensíveis para a LGPD?", Migalhas, n.d., https://www.migalhas.com.br/depeso/350335/dados-pessoais-bancarios-sao-considerados-dados-sensiveis-para-a-lgpd (accessed 2026-11-27)
14. "LGPD e o diálogo das fontes: a vez da Lei do Sigilo Bancário," Jus.com.br, n.d., https://jus.com.br/artigos/84714/lei-geral-de-protecao-de-dados-e-dialogo-das-fontes-4-lei-do-sigilo-bancario (accessed 2026-11-27)
15. EDGAR Application Programming Interfaces, U.S. Securities and Exchange Commission, n.d., https://www.sec.gov/edgar/sec-api-documentation (accessed 2026-11-27)
16. Taxa de juros - Meta Selic definida pelo Copom (SGS 432, API resource), Banco Central do Brasil Portal de Dados Abertos, n.d., https://dadosabertos.bcb.gov.br/dataset/432-taxa-de-juros---meta-selic-definida-pelo-copom/resource/2cb57a62-49de-405d-938b-482051a6e166 (accessed 2026-11-27)
