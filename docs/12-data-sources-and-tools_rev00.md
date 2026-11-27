# Data Sources and Tools for the AI Family Office

> **Purpose:** A catalog of data sources, analytics tools and AI connectors for Brazil and the US, with cost tiers, API availability, a lean starter stack and an upgrade path. **Primary users:** the data-engineering agent, research/market agents, macro and geopolitics agents, regulatory-watch agent, portfolio and risk agents, and the orchestrator when budgeting tools.

## Summary

- Most of what a single-family office needs for macro, filings and regulation is **free and official**: SEC EDGAR, FRED, the BCB's SGS and Olinda APIs (including the Focus survey), IBGE, Ipeadata, CVM open data and the Federal Register API [16][17][18][19][20][21][22][23][30].
- **Market data is where cost appears.** Low-cost APIs (Alpha Vantage, Massive/formerly Polygon.io, Financial Modeling Prep, Finnhub, Tiingo, brapi for B3) cost roughly US$0–150 per month [1][2][9][13][14][15]. Professional terminals cost five figures per seat per year: Bloomberg's single-terminal price was reported at US$31,980 per year from 2025 [4]. LSEG Workspace and FactSet are estimated at about US$12,000–40,000 per seat per year, and neither vendor publishes prices [5][6].
- **Brazil-specific gaps:** B3's official end-of-day service (UP2DATA) is a paid contract [7][8]. Economatica sells through commercial proposals with no public price [10]. brapi offers a free tier (15,000 requests per month, quotes delayed about 30 minutes) [9].
- **Geopolitical risk** can be covered free: the Caldara–Iacoviello GPR index (monthly) [26][27], Economic Policy Uncertainty indices including Brazil [28][29], GDELT (updated every 15 minutes) [24] and ACLED (free with registration, tiered access) [25].
- **Private markets data is expensive.** PitchBook is reported at about US$12,000–20,000 per seat per year. Crunchbase Pro costs about US$49–99 per month [32][33].
- **Family-office reporting platforms** (Addepar, Masttro, Asora) are mostly quote-based. Addepar is typically priced individually and suits large, complex estates [36][37][38].
- **MCP connectors:** MCP (Model Context Protocol) is a standard plug that lets AI agents call a data source directly. FactSet (December 2025) and LSEG (November 2025) have launched official MCP servers for entitled customers [39][40][41]. Low-cost options include brapi's MCP for B3 data and the Financial Datasets MCP server [9][42].
- **Recommendation:** start with a free/low-cost stack of about US$100–250 per month (Estimate). Upgrade to Koyfin-class tools, then to one institutional terminal only when assets and decision complexity justify it.

## 1. Cost tier definitions

| Tier | Typical price | Meaning |
|---|---|---|
| Free | US$0 | Public/official or free API tier |
| Low | < US$200/month | Retail/developer APIs and tools |
| Professional | US$200–2,000/month | Advisor-grade platforms |
| Institutional | > US$10,000/year per seat | Terminals, enterprise data, enterprise family-office platforms |

All prices are in nominal terms as reported in 2025–2026. Vendors change prices often, so the agent team should re-check before buying.

## 2. Market data

| Source | Coverage | Cost tier (price where public) | API | BR/US relevance |
|---|---|---|---|---|
| **Bloomberg Terminal** | All asset classes, news, analytics, messaging | Institutional: US$31,980/yr for a single terminal from 2025, on two-year contracts; data feeds such as B-PIPE extra [4] | Yes (Desktop API; B-PIPE extra) | Both; deep Brazil coverage (**Assumption**) |
| **LSEG Workspace (ex-Refinitiv Eikon)** | Global markets, Reuters news, fundamentals | Institutional: estimated US$12k–24k per seat/yr, depending on content sets [5] | Yes (Data Library); MCP for entitled clients [41] | Both |
| **FactSet** | Fundamentals, estimates, portfolio analytics | Institutional: estimates range from ~US$12k to US$40k+ per seat/yr [6] | Yes; MCP server [39][40] | Both |
| **B3 UP2DATA** | Official B3 end-of-day and reference data, in TXT/CSV/XML/JSON | Paid contract under B3's commercial policy [7][8] | File delivery (client or cloud) | Brazil (core) |
| **Economatica** | Brazilian and Latin American fundamentals and prices, long history | Commercial proposal and annual contract; no public price [10] | **Assumption:** offers API/Excel add-in | Brazil (core) |
| **Massive (formerly Polygon.io)** | US stocks, options, FX, crypto; real-time and historical | Low: rebranded October 2025; third-party reports list stock plans from US$0 up to ~US$199/mo for individual use [1] | REST + WebSocket | US |
| **Alpha Vantage** | US/global equities, FX, crypto, some fundamentals and indicators | Free: 25 requests/day [3]; Premium US$49.99–249.99/mo (75–1,200 requests/min) [2] | REST | US mainly; some global |
| **Financial Modeling Prep (FMP)** | Prices, fundamentals, transcripts | Low: a "Build" plan listed at US$139/mo; cheaper entry plans reported [13] | REST | US mainly; global on higher tiers |
| **Finnhub** | Quotes, fundamentals, news, alternative data | Free plan US$0/mo; paid plans higher [14] | REST + WebSocket | US mainly |
| **Tiingo** | EOD prices, IEX real-time, news, FX | Free "Starter" plan; paid plans; internal use only without redistribution license [15] | REST | US |
| **Yahoo Finance via yfinance** | Prices, basic fundamentals, including B3 tickers (".SA") | Free, but unofficial; the library says it is for research/education and defers to Yahoo's terms [11] | Unofficial Python library | Both; fine for prototypes, not for production |
| **brapi.dev** | B3 stocks, FIIs, BDRs, dividends, fundamentals | Free: 15,000 requests/month, ~30-min delay; paid Startup (~15-min) and Pro (~5-min) plans [9] | REST + MCP server [9] | Brazil (core) |
| **Status Invest** | Brazilian stock, FII and fixed-income screens | Free website | **Assumption:** no official public API (not verified) | Brazil |
| **Koyfin** | Charts, screening, fundamentals, dashboards | Free plan; Plus listed at US$39/mo; Pro folded into Premium in 2026 [12] | No public data API (**Assumption**) | US strong; some Brazil |

## 3. Fundamentals and filings

| Source | Coverage | Cost | API | BR/US relevance |
|---|---|---|---|---|
| **SEC EDGAR (data.sec.gov)** | All SEC filings; JSON submission history; XBRL company facts and "frames" (one fact across all companies) | Free; no API key; max 10 requests/second; nightly bulk ZIPs [16][17] | REST JSON + bulk | US (core); also Brazilian ADR issuers (20-F, 6-K) (**Assumption**) |
| **CVM Portal de Dados Abertos** | Listed company forms (DFP annual, ITR quarterly, FRE, cadastral data), funds data, securities held by insiders | Free [18] | CSV downloads + CKAN API [18] | Brazil (core) |
| **CVM RAD / ENET** | Filed documents, including material facts ("fatos relevantes") | Free | **Assumption:** web-based; no documented public API | Brazil |
| **Company IR pages** | Earnings releases, presentations, call transcripts | Free | Usually none; scrape or RSS | Both |
| **FMP / Finnhub / Alpha Vantage fundamentals** | Normalized statements | Low [2][13][14] | REST | US mainly |

## 4. Macroeconomic data

| Source | Coverage | Cost | API | BR/US relevance |
|---|---|---|---|---|
| **FRED (St. Louis Fed)** | Hundreds of thousands of US and international series, including global EPU | Free; registration for an API key required [19][29] | REST (JSON/XML) | US (core); some Brazil |
| **BLS** | CPI, payrolls, wages | Free | **Assumption:** public API v2 with free registration | US |
| **BEA** | GDP, PCE, trade, balance of payments | Free | **Assumption:** API with free user ID | US |
| **IMF, World Bank, OECD** | Cross-country macro, WEO forecasts, development indicators | Free | **Assumption:** each offers a public API (SDMX or REST) | Both, plus global context |
| **BCB SGS** | Time series: Selic, FX (e.g., series 1 USD/BRL), credit, IBC-Br | Free; date-range queries limited to 10 years per call [20] | REST JSON/CSV [20] | Brazil (core) |
| **BCB Olinda (Focus survey, PTAX)** | Market expectations by indicator × horizon × statistic; official FX rate | Free [21] | OData (a standard query format) [21] | Brazil (core) |
| **IBGE (SIDRA)** | IPCA, GDP, employment (PNAD), census | Free [22] | REST (`servicodados.ibge.gov.br/api/v3/agregados`) [22] | Brazil (core) |
| **IPEA (Ipeadata)** | Long macro, financial and regional series | Free [23] | OData v4; R wrapper `ipeadatar` [23] | Brazil |

## 5. News and sentiment

| Source | Coverage | Cost | API | BR/US relevance |
|---|---|---|---|---|
| **Bloomberg / LSEG (Reuters) news** | Premium real-time news | Institutional (bundled) [4][5] | Yes | Both |
| **Finnhub news and sentiment** | Company news, social sentiment | Free/low; free-tier news access is unclear [14] | REST | US |
| **Tiingo News** | Financial news feed | Low [15] | REST | US |
| **Alpha Vantage News & Sentiment** | News with sentiment scores | Free/low [2] | REST | US |
| **GDELT** | Global news events and tone (positive/negative wording), 1979 onward | Free; updated every 15 minutes; also in BigQuery [24] | Files, APIs, BigQuery | Both, plus global |
| **Brazilian outlets (Valor, InfoMoney, Estadão, Folha)** | Local business and political news | Free to paid subscriptions | **Assumption:** RSS feeds; no official data APIs | Brazil |

## 6. Geopolitical and policy risk

| Source | What it measures | Cost | Access | BR/US relevance |
|---|---|---|---|---|
| **Caldara–Iacoviello GPR index** | Share of newspaper articles about geopolitical tensions; global and country-level indices; monthly updates [26] | Free with attribution [26] | Excel/Stata downloads [26]; method in *American Economic Review* 2022 [27] | Global; includes US; country indices (**Assumption:** includes Brazil) |
| **Economic Policy Uncertainty (Baker–Bloom–Davis)** | Newspaper-based policy uncertainty; Brazil EPU in local, foreign and combined press versions, monthly [28] | Free | Downloads; global EPU on FRED [29] | Both |
| **GDELT** | Event counts and tone [24] | Free | BigQuery / files | Both |
| **ACLED** | Political violence and protest events | Free for most registered users, with tiers (Open, Research, Partner, Enterprise); research tier gets data with a time lag [25] | API via myACLED account (OAuth) [25] | Brazil (protests, violence), US |

## 7. Regulatory feeds

| Source | Coverage | Cost | API | Relevance |
|---|---|---|---|---|
| **Federal Register** | US rules, proposed rules, notices, executive orders | Free; no key [30] | REST JSON (`federalregister.gov/api/v1`) [30] | US |
| **Diário Oficial da União (INLABS)** | Full DOU editions in PDF and XML, free since 2020-01-01 [31] | Free with registration [31] | XML downloads [31] | Brazil (core) |
| **CVM** | Resolutions, notices, enforcement | Free [18] | Open data portal [18]; news pages | Brazil |
| **BCB normativos** | CMN/BCB resolutions, circulars | Free | **Assumption:** web search and RSS; Open Finance rules at `normativos.bcb.gov.br` | Brazil |
| **Receita Federal** | Tax rules (Instruções Normativas), CNPJ open data | Free | **Assumption:** CNPJ bulk files on gov.br open data; rules via DOU | Brazil |
| **Sector regulators (ANEEL, ANP, EMBRATUR/MTur; FERC, EIA in US)** | Energy tariffs, auctions; tourism statistics | Free | **Assumption:** mixed open-data portals | Relevant to the principal's operating businesses |

## 8. Alternative data

Alternative data means non-traditional signals (web traffic, card spending, satellite imagery, job postings, app downloads).

| Source type | Example use | Cost | Notes |
|---|---|---|---|
| Social/news sentiment | Finnhub social sentiment [14] | Low | US-focused |
| Event data | GDELT [24], ACLED [25] | Free | Good for geopolitics |
| Search trends, job postings, app data | Demand signals for hospitality and energy | Free to institutional | **Assumption:** vendor landscape not verified in this round; evaluate case by case |

**Assumption:** for a single family office, alternative data is a "Could." The principal's own operating businesses (occupancy, energy volumes) are a better proprietary signal than purchased datasets.

## 9. Private markets data

| Source | Coverage | Cost | API | Relevance |
|---|---|---|---|---|
| **PitchBook** | PE/VC deals, valuations, funds, LPs | Institutional: reported ~US$12k–20k/yr for one seat; no public price list [33] | Yes (enterprise); MCP partnerships reported (**Assumption**) | Global; US strongest |
| **Preqin** | Private funds, performance, LPs | Institutional | **Assumption:** quote-based; API for enterprise | Global |
| **Crunchbase** | Startups, funding rounds | Low: Pro ~US$49–99/mo per seat depending on billing and discounts; Business ~US$2,388/yr reported [32] | API on higher plans | Global; some LatAm |

## 10. Portfolio and risk analytics tools

### 10.1 Open-source libraries (free)

| Library | What it does (plain language) | License | Notes |
|---|---|---|---|
| **PyPortfolioOpt** | Builds portfolios: mean-variance (best return for a risk level), Black–Litterman (blends market view with your views), Hierarchical Risk Parity (spreads risk by clustering similar assets) [35] | MIT [35] | Easy entry point |
| **Riskfolio-Lib** | Wider set of risk measures (e.g., CVaR, drawdown) and asset-allocation models, built on the CVXPY optimizer [34] | BSD-3 [34] | Good for risk-budgeting |
| **QuantLib** | Pricing of bonds, swaps and options; yield curves | **Assumption:** open source (C++ with Python bindings); not verified in this round | Useful for Brazilian fixed income (DI curve) and US Treasuries |
| **pandas / yfinance / python-bcb / ipeadatar / sidra** | Data handling and Brazilian data access | Open source [11][23][22] | Glue code |

### 10.2 Family-office reporting platforms

| Platform | Positioning | Cost | Notes |
|---|---|---|---|
| **Addepar** | Enterprise wealth aggregation and reporting | Quote-based, priced per firm [36]; aimed at complex, large estates [37] | Implementation can take months [37] |
| **Masttro** | Family-office aggregation, entity mapping | Not published; fixed (non-AUM) pricing per vendor; third-party estimate ~US$900–1,000/mo starting [37][38] | Treat third-party estimates as approximate |
| **Asora** | Family-office reporting, tiered pricing, unlimited users | Tier-based; vendor publishes pricing [37][38] | Lighter-weight option |
| **Koyfin** | Analytics and model portfolios | Low to professional [12] | Not a full aggregation platform |

## 11. MCP servers and connectors

| Connector | Data | Access / cost | Relevance |
|---|---|---|---|
| **FactSet MCP** | Initially nine core datasets (Dec 2025); Portfolio Analytics MCP in limited release from June 2026 [39][40] | Requires FactSet subscription | Both |
| **LSEG MCP** | LSEG data with entitlement enforcement; launched on Databricks Marketplace Nov 2025 [41] | Requires LSEG entitlements | Both |
| **brapi MCP** | B3 quotes and fundamentals [9] | Free/low with brapi plan | Brazil |
| **Financial Datasets MCP** | US statements, prices, company news [42] | API key from Financial Datasets (paid usage) [42] | US |
| **Plaid / Pluggy (via custom connector)** | Account aggregation, US and Brazil [43][44] | Commercial agreements | Principal's own holdings |
| **Custom MCP wrappers** around EDGAR, FRED, BCB, IBGE, CVM, Federal Register | Official free data | Build cost only (**Estimate:** a few days of engineering each) | Both |

**Assumption:** community MCP servers exist for FRED, EDGAR and Yahoo data. Review their code and security before use, because a connector can see whatever it is given.

## 12. Recommended stack

### 12.1 Lean starter stack (free/low-cost)

| Need | Pick | Monthly cost (Estimate) |
|---|---|---|
| US prices and fundamentals | FMP or Massive starter plan; Alpha Vantage free as backup [1][2][13] | US$30–140 |
| Brazil prices and fundamentals | brapi Startup plan + CVM open data [9][18] | Low (brapi plan) |
| Filings | SEC EDGAR + CVM portal [16][18] | Free |
| Macro | FRED, BCB SGS/Olinda, IBGE, Ipeadata [19][20][21][22][23] | Free |
| Geopolitics | GPR, EPU, GDELT, ACLED [24][25][26][28] | Free |
| Regulation | Federal Register API + INLABS DOU XML + CVM/BCB pages [30][31] | Free |
| Charts and screening for the principal | Koyfin Free or Plus [12] | US$0–39 |
| Holdings aggregation | Pluggy (BR) + Plaid (US), or monthly statement parsing [43][44] | **Estimate:** usage-based; may be low for one family |
| Analytics | PyPortfolioOpt, Riskfolio-Lib, QuantLib [34][35] | Free |
| Storage | Postgres + document store | **Estimate:** US$0–50 hosting |
| **Total** | | **Estimate:** US$100–250/month |

### 12.2 Upgrade path

1. **Stage 2 (professional, about US$300–1,000/month, Estimate):** real-time US data (higher Massive or FMP tiers), B3 UP2DATA or Economatica for reliable Brazilian history [7][10], Crunchbase Pro for deal flow [32], Koyfin Premium [12].
2. **Stage 3 (family-office platform):** Asora or Masttro for consolidated entity-level reporting once there are several entities, custodians and private holdings [37][38]. Addepar if the estate becomes large and complex [36].
3. **Stage 4 (institutional):** one terminal seat (Bloomberg, LSEG Workspace or FactSet), chosen partly on whether its MCP server fits the agent architecture [4][5][6][39][41]. PitchBook or Preqin only if private markets become a major allocation [33].

**Trigger rule (Estimate):** upgrade when (a) a data gap has caused a wrong or delayed decision, or (b) the yearly tool cost is below about 0.1% of the assets it serves.

## Implications for the agent team

- The data-engineering agent should build connectors to free official sources first (EDGAR, FRED, BCB, IBGE, CVM, Federal Register, DOU) and cache them with "as of" dates.
- Agents must respect licenses: yfinance is unofficial [11]; Tiingo and many vendors restrict redistribution [15]; ACLED restricts sharing by tier [25]. Outputs shared beyond the principal must not republish licensed raw data.
- Market agents should label data latency (real-time, 15-minute, 30-minute, end-of-day), especially for brapi tiers [9].
- Macro agents should handle the Focus survey as a matrix (indicator × horizon × statistic), not a simple time series [21].
- The orchestrator should track tool spend against the upgrade trigger and propose upgrades with evidence.
- Security: each MCP connector gets least-privilege credentials, and none may see S4 data (see file 05).

## Open questions and assumptions

- Prices for Massive, FMP and Finnhub conflict across third-party sources; check vendor pages before buying [1][13][14].
- Not verified in this round (web search budget ran out): BLS, BEA, IMF, World Bank and OECD API details; QuantLib license; Status Invest API status; Receita Federal open-data formats; Preqin pricing; alternative-data vendors. These are labeled **Assumption** in the tables.
- Whether B3 UP2DATA offers retail-friendly pricing for a single family office is unknown [7][8].
- Whether the principal's custodians are supported by Pluggy and Plaid is unknown.
- **Assumption:** the principal prefers owning data pipelines over buying an all-in-one platform at the start.

## Sources

1. "Polygon to Massive rebrand: API pricing," APICostCalc (third-party), 2026, https://apicostcalc.com/blog/polygon-massive-rebrand-api-pricing.html (accessed 2026-11-27)
2. Premium API plans, Alpha Vantage, n.d., https://www.alphavantage.co/premium (accessed 2026-11-27)
3. Claim your Free API Key (support page), Alpha Vantage, n.d., https://www.alphavantage.co/support/ (accessed 2026-11-27)
4. "Bloomberg Terminals: How Much More You'll Pay Next Year," NeuGroup, 2024, https://connect.neugroup.com/public/blogs/bloomberg-terminals-how-much-more-youll-pay-next-year (accessed 2026-11-27)
5. "LSEG API Pricing and Alternatives (2026)," Multiples.vc (third-party), 2026, https://multiples.vc/compare/lseg-api-alternatives (accessed 2026-11-27)
6. "FactSet vs Refinitiv Eikon (2026): Pricing," CostBench (third-party), 2026, https://www.costbench.com/compare/factset-vs-refinitiv-eikon/ (accessed 2026-11-27)
7. About UP2DATA, B3, n.d., https://www.b3.com.br/en_us/market-data-and-indices/data-services/up2data/about-up2data/ (accessed 2026-11-27)
8. How to hire and access UP2DATA, B3, n.d., https://b3.com.br/en_us/market-data-and-indices/data-services/up2data/how-to-hire-and-access/ (accessed 2026-11-27)
9. brapi.dev documentation, pricing, FAQ and MCP pages, brapi, 2026, https://brapi.dev/pricing.md ; https://brapi.dev/faq/qual-a-diferenca-real-no-atraso-delay-dos-dados-entre-os-planos ; https://brapi.dev/faq/o-plano-gratuito-tem-limitacoes-importantes ; https://brapi.dev/mcp (accessed 2026-11-27)
10. "brapi vs Economatica: comparativo," brapi blog (competitor material), n.d., https://brapi.dev/blog/brapi-vs-economatica-comparativo (accessed 2026-11-27)
11. yfinance README, ranaroussi/yfinance (GitHub), n.d., https://raw.githubusercontent.com/ranaroussi/yfinance/main/README.md (accessed 2026-11-27)
12. Koyfin Pricing and Plan Guide, Koyfin, 2026, https://www.koyfin.com/pricing-llm-info/ ; Changes to the Koyfin Pro Plan, https://www.koyfin.com/help/pro-discontinuation/amp/ (accessed 2026-11-27)
13. Financial Modeling Prep pricing, TrustRadius, 2026, https://www.trustradius.com/products/financial-modeling-prep/pricing (accessed 2026-11-27)
14. Pricing, Finnhub, n.d., https://finnhub.io/pricing (accessed 2026-11-27)
15. Tiingo API, Tiingo, n.d., https://api.tiingo.com (accessed 2026-11-27)
16. EDGAR Application Programming Interfaces, U.S. SEC, n.d., https://www.sec.gov/edgar/sec-api-documentation (accessed 2026-11-27)
17. Accessing EDGAR Data, U.S. SEC, n.d., https://www.sec.gov/os/accessing-edgar-data (accessed 2026-11-27)
18. Portal de Dados Abertos da CVM, Comissão de Valores Mobiliários, n.d., https://dados.cvm.gov.br/ (accessed 2026-11-27)
19. FRED API Terms of Use, Federal Reserve Bank of St. Louis, n.d., https://fred.stlouisfed.org/docs/api/terms_of_use.html (accessed 2026-11-27)
20. SGS API resource (Meta Selic, series 432), Banco Central do Brasil Portal de Dados Abertos, n.d., https://dadosabertos.bcb.gov.br/dataset/432-taxa-de-juros---meta-selic-definida-pelo-copom/resource/2cb57a62-49de-405d-938b-482051a6e166 (accessed 2026-11-27)
21. "Séries do Banco Central: como consultar o SGS, a Focus e a PTAX," TabNews (community guide), n.d., https://www.tabnews.com.br/SidneyBissoli/series-do-banco-central-como-consultar-o-sgs-a-focus-e-a-ptax-sem-cair-nas-armadilhas (accessed 2026-11-27)
22. API de dados agregados (v3), IBGE, n.d., https://servicodados.ibge.gov.br/api/docs/agregados?versao=3 (accessed 2026-11-27)
23. ipeadatar: API Wrapper for Ipeadata, CRAN / Ipea, n.d., https://cran.r-project.org/web/packages/ipeadatar/index.html (accessed 2026-11-27)
24. Data, The GDELT Project, n.d., https://www.gdeltproject.org/data.html (accessed 2026-11-27)
25. Frequently Asked Questions about myACLED, ACLED, 2025, https://acleddata.com/myacled-faqs (accessed 2026-11-27)
26. Geopolitical Risk (GPR) Index, Matteo Iacoviello, 2026, https://www.matteoiacoviello.com/gpr.htm (accessed 2026-11-27)
27. Caldara, D. and Iacoviello, M., "Measuring Geopolitical Risk," American Economic Review 112(4), 2022, https://www.aeaweb.org/doi/10.1257/aer.20191823 (accessed 2026-11-27)
28. Economic Policy Uncertainty (EPU) Indices for Latin America, Banco de España, n.d., https://www.bde.es/wbe/en/areas-actuacion/analisis-e-investigacion/recursos/indices-de-incertidumbre-de-la-politica-economica--epu--para-los-principales-paises-de-america-latin-a4a57615df14481.html (accessed 2026-11-27)
29. Global Economic Policy Uncertainty Index: PPP-Adjusted GDP (GEPUPPP), FRED, n.d., https://fred.stlouisfed.org/series/GEPUPPP (accessed 2026-11-27)
30. REST API, FederalRegister.gov, n.d., https://www.federalregister.gov/reader-aids/developer-resources/rest-api (accessed 2026-11-27)
31. Imprensa Nacional (INLABS repository), GitHub, n.d., https://github.com/Imprensa-Nacional (accessed 2026-11-27)
32. "Crunchbase Pricing 2026," Private Equity List (third-party), 2026, https://privateequitylist.com/intelligence/crunchbase-pricing (accessed 2026-11-27)
33. "PitchBook Pricing 2026," Private Equity List (third-party), 2026, https://privateequitylist.com/intelligence/pitchbook-pricing (accessed 2026-11-27)
34. Riskfolio-Lib documentation, D. Cajas, n.d., https://riskfolio-lib.readthedocs.io/ (accessed 2026-11-27)
35. PyPortfolioOpt, GitHub, n.d., https://github.com/PyPortfolio/PyPortfolioOpt (accessed 2026-11-27)
36. "Addepar Pricing," Kubera (competitor blog), n.d., https://www.kubera.com/blog/addepar-pricing (accessed 2026-11-27)
37. "The Best Software Tools for Family Offices in 2026," ValueAddVC, 2026, https://valueaddvc.com/blog/the-best-software-tools-for-family-offices-in-2026-portfolio-reporting-and-tax (accessed 2026-11-27)
38. "Asora vs Masttro" comparison, Asora (vendor material), n.d., https://asora.com/compare/asora-vs-masttro (accessed 2026-11-27)
39. "FactSet Meets Demand for AI Ready Data, First to Announce MCP Sans Intermediary," FactSet via GlobeNewswire, 2025, https://www.globenewswire.com/fr/news-release/2025/12/16/3206057/7768/en/FactSet-Meets-Demand-for-AI-Ready-Data-First-to-Announce-MCP-Sans-Intermediary.html (accessed 2026-11-27)
40. "FactSet Expands Model Context Protocol Suite with Portfolio Analytics," FactSet, 2026, https://investor.factset.com/news-releases/news-release-details/factset-expands-model-context-protocol-suite-portfolio-analytics (accessed 2026-11-27)
41. LSEG MCP and "LSEG launches MCP server on Databricks Marketplace," LSEG, 2025, https://www.lseg.com/en/solutions/ai-finance-solutions/lseg-mcp ; https://www.lseg.com/en/solutions/ai-finance-solutions/updates/lseg-launches-mcp-server-databricks-marketplace-ai-ready-access (accessed 2026-11-27)
42. Financial Datasets MCP Server listing, mcpservers.org, n.d., https://mcpservers.org/servers/financial-datasets/mcp-server (accessed 2026-11-27)
43. Investments (product documentation), Plaid, n.d., https://plaid.com/docs/investments/ (accessed 2026-11-27)
44. "Fintech Pluggy capta US$ 3,5 milhões de olho em novos produtos," Finsiders Brasil, 2026, https://finsidersbrasil.com.br/negocios-em-fintechs/fintech-pluggy-capta-us-35-milhoes-de-olho-em-novos-produtos/ (accessed 2026-11-27)
