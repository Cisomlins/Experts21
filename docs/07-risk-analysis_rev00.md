# Risk Analysis for the Family Office

> **Purpose:** Define how the agent team identifies, measures, limits, hedges and explains risk across the principal's whole balance sheet (liquid portfolio plus operating businesses) in Brazil and the US. **Primary users:** Risk agent (owner), CIO agent, Asset Allocation agent, Macro/Geopolitics agent, Tax and Structuring agent, Insurance and Asset Protection agent, and the Reporting agent that presents risk to the principal.

> **Disclaimer:** This document is research and education, not personalized investment, insurance, tax or legal advice.

## Summary

- Risk is "the chance of not meeting goals," not just price swings. The biggest risk for a business owner is usually **concentration**: much of their wealth, income and reputation tied to the same country, currency and sectors as their operating companies.
- Use two governance frameworks: **COSO ERM (2017)** for linking risk to strategy and governance [1], and **ISO 31000:2018** for the risk process (identify, analyze, evaluate, treat, monitor, communicate) [2].
- Every risk number (volatility, VaR, beta, correlation) rests on assumptions that fail in crises: returns have "fat tails" [3] and correlations rise in falling markets [4]. Regulators have moved from VaR toward **Expected Shortfall (CVaR)** for this reason [5].
- Brazil-specific history shows deep, repeated shocks: Ibovespa fell about 60% in 2008 [6], the economy shrank in both 2015 and 2016 [7] as Brazil lost its investment grade [8], and Ibovespa fell about 30% in March 2020 alone while the dollar rose about 16% [9]. The real usually weakens when Brazilian assets fall, so USD assets have acted as a natural hedge.
- Set explicit limits (concentration, liquidity, currency, drawdown) and track them on a one-page dashboard with traffic lights.
- Hedge with simple, understandable tools (USD holdings, FX forwards, put options, gold, Treasuries) and insurance; avoid complex products the principal cannot explain.
- Present risk in money terms, with scenarios and plain words: "In a 2008-type event, the liquid portfolio could fall by about R$X; here is what we would do."

## 1. Governing frameworks

| Framework | What it gives us | How the agents use it |
|---|---|---|
| **COSO ERM: Integrating with Strategy and Performance (2017)** | Five components: Governance and Culture; Strategy and Objective-Setting; Performance; Review and Revision; Information, Communication and Reporting [1] | The principal sets **risk appetite** (how much risk is acceptable to pursue goals) in the IPS; the Risk agent reports against it |
| **ISO 31000:2018** | Principles, framework and a process to identify, analyze, evaluate, treat, monitor and communicate risk; guidelines, not a certifiable standard; confirmed current in 2023 [2] | The standard workflow for every new risk |
| **NIST Cybersecurity Framework 2.0** | Govern, Identify, Protect, Detect, Respond, Recover functions for cyber risk [18] | Cyber controls for the family office and the AI system |
| **NIST AI Risk Management Framework 1.0** | Govern, Map, Measure, Manage functions for AI risks [19] | Managing model risk from the AI agents themselves |
| **US Federal Reserve SR 11-7** | Model risk management: sound development, independent validation, governance [20] | Validation rules for any quantitative model the agents use |

## 2. Risk taxonomy

| Risk | Plain definition | Principal-specific angle |
|---|---|---|
| **Market** | Prices of stocks, bonds, property or commodities fall | Liquid portfolio plus value of the businesses |
| **Concentration** | Too much in one asset, sector, country or person | Hospitality and energy businesses, Brazil, BRL; **Assumption:** these are likely the largest share of net worth |
| **Liquidity** | Cannot sell quickly without a large price cut, or cannot meet cash needs | Businesses may need cash exactly when markets are stressed |
| **Credit / counterparty** | A borrower, bank or broker fails to pay | Bank CDBs above FGC limits [15]; private credit; broker failure |
| **Currency (FX)** | Exchange rate moves hurt you | BRL income vs. USD spending (studies, US ties) |
| **Inflation** | Rising prices erode purchasing power | IPCA in Brazil; US CPI for USD spending |
| **Interest rate** | Rate changes move bond prices and business financing costs | Selic held at 13.75% in Nov 2026 [14]; energy and hospitality are capital-intensive |
| **Political / sovereign** | Elections, fiscal crises or policy shifts hurt assets or the currency | Brazil's 2002 and 2015 episodes [10][8]; US policy shifts |
| **Regulatory / tax** | Rule changes alter returns or legality | Offshore taxation under Law 14,754/2023 [16]; US estate tax for non-residents [17]; energy-sector regulation |
| **Operational / fraud** | Errors, theft, poor controls, scams | Wire fraud, fake investment offers, weak custody |
| **Key-person** | Loss of a critical person damages value | The principal and key managers of the businesses |
| **Cyber** | Hacking, ransomware, account takeover | Brokerage, banking and business systems [18] |
| **Model risk (from the AI)** | Wrong output from models or AI agents: errors, outdated data, invented facts, overconfidence | The agents themselves [19][20] |

## 3. Risk measures: what they mean and where they fail

| Measure | Plain definition | Weakness |
|---|---|---|
| **Volatility** (standard deviation) | How much returns typically swing around their average; e.g., 20% annual volatility means a typical year is within roughly ±20% of average | Treats up and down moves the same; understates rare crashes |
| **Maximum drawdown** | The largest peak-to-bottom fall before a new high (e.g., Ibovespa about −60% from May to October 2008 [6]) | Backward-looking; the next one can be worse |
| **Value at Risk (VaR)** | "With 95% confidence, we will not lose more than X in one month" | Says nothing about *how bad* the worst 5% can be; relies on normal-distribution assumptions that fail [3] |
| **CVaR / Expected Shortfall** | The *average* loss in the worst cases beyond the VaR cut-off | Better for tails, still dependent on data and model; Basel's market risk rules replaced VaR with Expected Shortfall [5] |
| **Beta** | How much an asset moves with the market; beta 1.5 means about 1.5% move per 1% market move | Unstable over time; rises in crises |
| **Correlation** | How closely two assets move together, from −1 (opposite) to +1 (together) | Large negative moves are much more correlated than normal models predict [4]; in 2022 US stocks and bonds both fell double digits [12] |
| **Stress test** | "What happens to us if 2008 repeats?" using historical shocks | Only as good as the scenarios chosen |
| **Scenario analysis** | Forward-looking "what if" stories (e.g., Brazil fiscal crisis + BRL −30%) | Probabilities are judgment calls |
| **Factor exposures** | Sensitivity to broad return drivers such as market, size and value [13] (a **factor** is a common characteristic that explains why many assets move together) | Factor premia vary and can disappear for years |
| **Liquidity ladder** | Table of how much can be converted to cash within 1 day, 1 week, 1 month, 1 year, >1 year | Market liquidity dries up in crises; lock-ups can be extended |

**Fat tails:** Mandelbrot showed in 1963 that price changes have far more extreme moves than the normal "bell curve" predicts [3]. **Rule for agents:** always report historical stress losses and CVaR next to VaR; never present VaR alone.

## 4. Historical stress scenarios

### 4.1 Brazil

| Episode | What happened | Lessons |
|---|---|---|
| **2002 election** | Rising odds of a Lula victory triggered an acute crisis: the real depreciated sharply, inflation rose, and sovereign spreads widened on default fears [10]. Markets later recovered as policy proved market-friendly [10] | Political risk hits currency, bonds and stocks at once; USD assets protected BRL wealth |
| **2008 global financial crisis** | Ibovespa fell from 73,516 (20 May 2008) to 29,435 (October 2008), roughly −60% [6] | Global shocks hit emerging markets harder; liquidity vanished |
| **2015–16 recession** | GDP fell in both years (IBGE revised: −3.5% in 2015 and −3.3% in 2016) [7]; S&P cut Brazil to junk (BB+) in September 2015, citing political problems [8] | Fiscal and political crises compound; credit spreads and unemployment hit businesses and portfolios together |
| **2020 COVID** | Six circuit-breaker trading halts in March; Ibovespa −29.9% in March 2020 (worst month since 1998) while the dollar rose about 16% [9] | Speed of crash; BRL weakness amplified USD gains for Brazilian holders |
| **2021–22 rate hikes** | The Selic reached 13.75% and was held there after the 2022 election [11] | Pre-fixed bonds and growth stocks fell; CDI became a strong competitor to risk assets |

### 4.2 United States

| Episode | What happened | Lessons |
|---|---|---|
| **2007–09 financial crisis** | S&P 500 fell about 57% peak to trough [21] | Credit crisis spread to all risk assets |
| **2020 COVID** | S&P 500 fell about 34% between 19 February and 23 March 2020 [21] | Fastest bear market; fast recovery after policy response |
| **2022 inflation shock** | US stocks fell a little over 18% and the aggregate US bond market about 13%, a rare year when both fell double digits [12] | Bonds do not always hedge stocks when inflation drives rates up |

**Standard stress set (Assumption):** the Risk agent should run, at least quarterly: (1) 2002-type Brazil political shock, (2) 2008-type global crisis, (3) 2015–16-type Brazil recession, (4) 2020-type sudden crash, (5) 2022-type inflation/rate shock, (6) a forward-looking combined scenario: Brazil fiscal stress + BRL −30% + a sector shock to hospitality or energy.

## 5. Concentration in the operating businesses

- Measure **total-wealth risk**, not only the liquid portfolio. Estimate the value, debt and cash-flow sensitivity of each business.
- **Assumption:** hospitality is sensitive to recessions, travel shocks (2020) and FX (inbound tourism); energy is sensitive to regulation, commodity prices and interest rates.
- **Rule:** the liquid portfolio should be built to *offset* the businesses: lower weights in Brazilian real estate, hospitality and energy stocks; more global, USD and defensive assets; and a liquidity reserve sized to cover business stress needs (**Assumption:** e.g., 12–24 months of fixed costs and debt service).

## 6. Risk limits (illustrative; to be set in the IPS)

| Limit | Illustrative level (**Assumption**) |
|---|---|
| Single security (ex-government bonds and broad funds) | ≤5% of liquid portfolio |
| Single private fund / manager | ≤10% |
| Single bank (deposits/CDBs) | Within FGC limit of R$250k per CPF per institution unless approved [15] |
| Illiquid assets (> 1 year to cash) | ≤25% of liquid portfolio |
| Minimum USD share of liquid wealth | Covers 3–5 years of USD needs plus hedge target |
| Portfolio 1-year CVaR (95%) | ≤ a stated BRL amount the principal accepts |
| Maximum drawdown trigger | −15% triggers a formal review (not automatic selling) |
| Leverage | None at portfolio level without explicit approval |

## 7. Risk dashboard design

A one-page monthly dashboard, traffic-light coded (green / amber / red against limits):

```
RISK DASHBOARD — <month> — values in BRL and USD
1. Headline: total liquid wealth, month & YTD return, vs. CDI and vs. benchmark
2. Allocation vs. target: asset class, BRL/USD, country — with band breaches flagged
3. Total-wealth view: businesses + portfolio, exposure by sector/country/currency
4. Risk numbers: volatility, 1-month VaR(95%) and CVaR(95%), current drawdown
5. Stress results: loss under each standard scenario, in BRL and USD
6. Liquidity ladder: cash available in 1 day / 1 week / 1 month / 1 year
7. Concentration: top 10 exposures, bank/FGC exposure, custodian split
8. Limits table: each limit, current value, status color
9. Watchlist: macro/political events (Copom, Fed, elections, tax changes)
10. Model-risk notes: data dates, stale inputs, assumptions changed this month
```

## 8. Hedging tools

| Tool | What it does | Cost / caveat |
|---|---|---|
| **Holding USD assets** | Natural hedge: BRL tends to fall in Brazilian and global crises [9] | Gives up the BRL-USD interest differential (high while Selic is 13.75% [14]) |
| **FX forwards / futures** (e.g., B3 dollar futures) | Lock in an exchange rate | Cost roughly equals the interest differential; margin calls |
| **Put options** | Right to sell at a set price: insurance against crashes | Premium paid regularly; expensive after volatility spikes |
| **Gold** | Historically held as a crisis and inflation hedge (**Assumption**) | No income; can fall for years |
| **US Treasuries** | Often rise in deflationary crises | Failed in 2022's inflation shock [12] |
| **Trend-following strategies** | Diversified trend strategies did best in extreme markets historically [22] | Long flat periods; fees |

**Rule:** prefer structural hedges (diversification, USD allocation, liquidity reserve) over constant derivative hedging; use options tactically and only with defined maximum cost.

## 9. Insurance and asset protection

- **Deposit and broker protection:** FGC (Brazil) R$250k per CPF per institution, up to R$1m per 4 years [15]; FDIC USD 250,000 per depositor per bank per ownership category [23]; SIPC up to USD 500,000 against broker failure, not market loss [24].
- **Personal and business insurance (Assumption, to be reviewed by an insurance broker):** life and disability (key-person), D&O for company boards, property and business interruption for hotels and energy assets, liability umbrella, cyber insurance.
- **Estate and structure:** US-situs assets of non-residents may face US estate tax above USD 60,000 [17]; holding structures, wills and succession plans in both countries are an asset-protection priority for the Tax and Structuring agent.
- **Fraud controls:** dual approval for wires, call-back verification on a known number, no investment decisions based on unsolicited messages, hardware security keys for financial accounts [18].

## 10. Model risk from the AI itself

- **Risks:** outdated data, invented facts or sources, false precision, overfitting to history, and shared blind spots across agents.
- **Controls:** every number has a source and date; estimates and assumptions are labeled; a red-team agent independently checks major recommendations; models are validated before use and re-checked periodically, following SR 11-7 principles [20] and the NIST AI RMF [19]; the principal (or a human advisor) approves every transaction; the AI never has unilateral authority to move money.

## 11. Presenting risk to a non-quant principal

1. **Lead with money, not statistics:** "In a 2008-type crisis, the liquid portfolio could fall about R$X (US$Y)."
2. **Use scenarios and stories** rather than distributions; give the plan for each.
3. **Use ranges and frequencies:** "a year this bad has happened about once a decade in this history" is clearer than "5% VaR."
4. **Frame against goals:** "Even in this scenario, business reserves and study costs are covered for N years."
5. **Show both sides** of each trade-off: "Hedging the dollar fully costs about Z% per year in lost carry."
6. **Watch the framing effect:** people react more strongly to losses than equal gains [25]; present gains and losses symmetrically and in total-wealth context.
7. **Define every term on first use** and keep one glossary across reports.

## Implications for the agent team
- The Risk agent owns the dashboard, limits and quarterly stress tests, and can veto trades that breach limits pending principal approval.
- All risk reports must include total-wealth exposure, including the operating businesses.
- Never report VaR without CVaR and historical stress losses; flag correlation assumptions.
- The Macro/Geopolitics agent maintains the political/sovereign scenario library for Brazil and the US and updates it after each Copom, Fed meeting and election.
- The Tax and Structuring agent tracks regulatory/tax risk (offshore rules, LCI/LCA, estate tax) and issues alerts.
- Model-risk controls apply to every agent; outputs without sources and dates are not decision-ready.

## Open questions and assumptions
- Values, debt and cash-flow sensitivity of the hospitality and energy businesses are unknown; concentration analysis needs them.
- The principal's risk appetite (maximum acceptable loss in BRL/USD) and liquidity needs must be set in the IPS; all limits here are **Assumptions**.
- US tax residency status affects estate-tax exposure and structuring.
- Exact BRL/USD peak levels in 2002 and the EMBI spread peak were not verified from a primary source and are omitted.
- Historical drawdown figures differ slightly by data source and date convention [21].
- Gold's hedging role is stated as a common view, not verified with a cited study here.

## Sources
1. COSO, "Enterprise Risk Management: Integrating with Strategy and Performance" (2017), summary via NC State ERM Initiative, https://erm.ncsu.edu/library/article/cosos-erm-framework (accessed 2026-11-27)
2. ISO, "ISO 31000:2018 Risk management — Guidelines," https://www.iso.org/standard/65694.html (accessed 2026-11-27)
3. Mandelbrot, B., "The Variation of Certain Speculative Prices," Journal of Business, 1963, https://doi.org/10.1086/294632 (accessed 2026-11-27)
4. Longin, F., Solnik, B., "Extreme Correlation of International Equity Markets," Journal of Finance 56(2), 2001, https://econpapers.repec.org/RePEc:bla:jfinan:v:56:y:2001:i:2:p:649-676 (accessed 2026-11-27)
5. Basel Committee on Banking Supervision, "Minimum capital requirements for market risk," BIS, 2019, https://www.bis.org/bcbs/publ/d457.htm (accessed 2026-11-27)
6. Agrolink, "O 20 de maio de 2008" (Ibovespa record of 73,516 and October low of 29,435), https://www.agrolink.com.br/colunistas/o-20-de-maio-de-2008_386785.html (accessed 2026-11-27)
7. IBGE Agência de Notícias, "In 2016, GDP reaches R$6.3 trillion and records a 3.3% drop in volume" (revised series), https://agenciadenoticias.ibge.gov.br/en/agencia-press-room/22972-in-2016-gdp-reaches-r-6-3-trillion-and-records-a-3-3-drop-in-volume.html (accessed 2026-11-27)
8. MercoPress, "Brazil loses investment grade credit rating with outlook remaining negative," 2015, https://en.mercopress.com/2015/09/10/brazil-loses-investment-grade-credit-rating-with-outlook-remaining-negative (accessed 2026-11-27)
9. InfoMoney, "Ibovespa fecha o mês com queda de 30% e tem pior trimestre da história; dólar sobe 16% em março," 2020, https://www.infomoney.com.br/mercados/ibovespa-fecha-o-mes-com-queda-de-30-e-tem-pior-trimestre-da-historia-dolar-sobe-16-em-marco/ ; and Forbes Brasil, "Ibovespa acelera queda e aciona circuit breaker pela 6ª vez em março," 2020, https://forbes.com.br/colunas/2020/03/ibovespa-acelera-queda-e-aciona-circuit-breaker-pela-6a-vez-em-marco/ (accessed 2026-11-27)
10. Blanchard, O., "Fiscal Dominance and Inflation Targeting: Lessons from Brazil," NBER Working Paper 10389, 2004, https://www.nber.org/papers/w10389.pdf (accessed 2026-11-27)
11. Investidor10, "Copom mantém a Selic em 13,75% ao ano na 1ª decisão após vitória de Lula," 2022, https://investidor10.com.br/noticias/copom-mantem-a-selic-em-13-75-ao-ano-na-1-decisao-apos-vitoria-de-lula-123689/ (accessed 2026-11-27)
12. The Motley Fool, "2022 was the worst year since 1937 for this investing strategy," 2023, https://www.fool.com/investing/2023/01/26/2022-was-the-worst-year-since-1937-for-this-invest (accessed 2026-11-27)
13. Fama, E.F., French, K.R., "Common Risk Factors in the Returns on Stocks and Bonds," Journal of Financial Economics, 1993, https://doi.org/10.1016/0304-405X(93)90023-5 (accessed 2026-11-27)
14. Banco Central do Brasil, Copom 282nd meeting minutes (Selic held at 13.75%, Nov 2026), https://www.bcb.gov.br/content/copom/copomminutes/Minutes_282_v2.pdf (accessed 2026-11-27)
15. Fundo Garantidor de Créditos, "About FGC guarantee," https://fgc.org.br/en/sobre-garantia-fgc (accessed 2026-11-27)
16. Brazil, Lei nº 14.754, de 12 de dezembro de 2023, https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/Lei/L14754.htm (accessed 2026-11-27)
17. IRS, "Some nonresidents with U.S. assets must file estate tax returns," https://www.irs.gov/individuals/international-taxpayers/some-nonresidents-with-us-assets-must-file-estate-tax-returns (accessed 2026-11-27)
18. NIST, "Cybersecurity Framework 2.0," 2024, https://www.nist.gov/cyberframework (accessed 2026-11-27)
19. NIST, "AI Risk Management Framework (AI RMF 1.0)," 2023, https://www.nist.gov/itl/ai-risk-management-framework (accessed 2026-11-27)
20. Board of Governors of the Federal Reserve System, "SR 11-7: Guidance on Model Risk Management," 2011, https://www.federalreserve.gov/supervisionreg/srletters/sr1107.htm (accessed 2026-11-27)
21. Stacker, "Every major stock market correction since 1950 and how long recovery took," 2026, https://stacker.com/stories/business-economy/every-major-stock-market-correction-1950-and-how-long-recovery-took (accessed 2026-11-27)
22. Moskowitz, T.J., Ooi, Y.H., Pedersen, L.H., "Time Series Momentum," Journal of Financial Economics, 2012, https://econpapers.repec.org/RePEc:eee:jfinec:v:104:y:2012:i:2:p:228-250 (accessed 2026-11-27)
23. FDIC, "Deposit Insurance," https://www.fdic.gov/resources/deposit-insurance (accessed 2026-11-27)
24. SIPC, "What SIPC Protects," https://www.sipc.org/for-investors/what-sipc-protects (accessed 2026-11-27)
25. Kahneman, D., Tversky, A., "Prospect Theory: An Analysis of Decision under Risk," Econometrica, 1979, https://doi.org/10.2307/1914185 (accessed 2026-11-27)
