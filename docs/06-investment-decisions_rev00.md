# Investment Decisions: What, Where and When to Invest

> **Purpose:** Give the agent team one shared, evidence-based method for deciding what to buy, in which jurisdiction and wrapper, and when, for a Brazil-based principal with US ties. **Primary users:** Chief Investment Officer agent, Asset Allocation agent, Brazil Markets agent, US Markets agent, Alternatives agent, Tax and Structuring agent, Risk agent (see file 07), and the Decision Review ("red team") agent.

> **Disclaimer:** This document is research and education, not personalized investment, tax or legal advice. Any action should be confirmed with licensed professionals in Brazil and the US.

## Summary

- Decide top-down: **goals → Investment Policy Statement (IPS) → strategic asset allocation → tactical tilts → security/manager selection → execution → rebalancing**. Most of the long-run result is set by the first three steps [1][2].
- The famous "asset allocation explains 90%+ of performance" finding is about the *ups and downs over time* of one portfolio, not about why one investor beats another; across investors, policy explains roughly 40% of differences [1][2][3].
- For a Brazilian investor, the biggest single allocation choice is often the **BRL/USD split**. Home bias (keeping most money in your own country) is common worldwide and adds avoidable country risk [4]. The principal's operating businesses are already a large BRL bet.
- In Brazil, the risk-free hurdle is very high: the Selic policy rate was held at **13.75%** on 4 November 2026 [11]. Every risky asset must be judged against what the CDI pays for nearly no risk.
- On timing: lump-sum investing beat gradual "cost averaging" about two-thirds of the time in Vanguard's study [5]; valuation signals such as CAPE predict long-horizon returns loosely but are poor short-term timing tools [6][7]; trend signals have real but modest evidence [9][10].
- Investors lose returns by buying and selling at the wrong times: Morningstar estimates the average fund investor earned about 1.2 percentage points a year less than the funds they held [12].
- Every recommendation must come as a standard **investment memo** with scenarios, expected value, base rates, a pre-mortem, a position size and a conviction score.

## 1. The decision hierarchy

| Step | Question it answers | Who owns it | Typical review cycle |
|---|---|---|---|
| 1. Goals | What is the money for, and when? (liquidity for the businesses, family security, study costs in USD, legacy) | Principal, with CIO agent | Yearly or at life events |
| 2. Investment Policy Statement (IPS) | What are the return target, risk tolerance, liquidity needs, time horizon, tax and legal constraints, and who decides what? | CIO agent drafts; principal approves | Yearly |
| 3. Strategic asset allocation (SAA) | Long-run mix of asset classes and currencies (for example 40% BRL fixed income, 25% global equities…) | Asset Allocation agent | Yearly |
| 4. Tactical tilts | Small, temporary deviations from SAA based on valuation or the rate cycle, within bands set by the IPS | Asset Allocation + Macro agents | Quarterly |
| 5. Security / manager selection | Which bond, fund, ETF, stock or private manager fills each slot | Market and Alternatives agents | When needed |
| 6. Execution | How and when to trade: FX conversion, order type, staging, costs, taxes | Execution / Tax agents | Each trade |
| 7. Rebalancing and monitoring | Bring the portfolio back to target; report results and risk | Risk agent | Monthly check; act on bands |

An **Investment Policy Statement** is a short written "constitution" for the portfolio. The CFA Institute recommends that an individual's IPS cover scope and purpose, governance (who decides), investment objectives, risk tolerance, constraints and performance review, and notes that not every element fits every investor [27]. **Assumption:** the principal's IPS should also state (a) how much of total wealth sits in the operating businesses, (b) a minimum liquidity reserve to support those businesses, and (c) a target BRL/USD split.

## 2. What drives returns: the evidence

### 2.1 Brinson-Hood-Beebower and the critiques
- **Brinson, Hood and Beebower (1986)** studied 91 large US pension funds from 1974–1983 and found that investment policy (the long-run asset mix) explained on average **93.6%** of the *variation* in quarterly returns [1][3].
- This is widely misread as "allocation explains 93.6% of returns." It means that most of a portfolio's quarter-to-quarter movement comes from what asset classes it holds [3].
- **Ibbotson and Kaplan (2000)** showed that the answer depends on the question: policy explains about **90%** of a fund's variability over time, about **40%** of the differences in returns *between* funds, and about **100%** of the return *level* on average, because the average active manager does not add value after costs [2].
- **Practical meaning:** spend most effort on the SAA and the currency split, and treat stock-picking and tactical calls as smaller, costlier, harder-to-win bets.

### 2.2 Diversification and home bias
**Diversification** means holding assets that do not all fall at the same time, so one loss is partly offset by others. **Home bias** is the tendency to hold far more domestic assets than the home market's share of the world. Vanguard documents persistent home bias (for example, Canadians still held about 50% of equities at home in 2024, versus a recommended ~30%) and links it to avoidable, country-specific risk [4]. **Estimate:** Brazil is a small fraction of global stock market value, so a Brazilian portfolio with mostly B3 equities is a concentrated country bet.

### 2.3 BRL/USD currency allocation for a Brazilian investor
- The principal **spends partly in USD** (US study and ties) and **earns mostly in BRL** (Brazilian businesses). **Assumption:** USD needs for the next 2–5 years should be held in USD assets, so a weak real does not force selling at a bad rate.
- Holding USD assets has historically protected Brazilian investors in crises, because the real tends to fall when global or local stress rises (see file 07 stress scenarios). This makes USD a partial hedge for BRL-heavy wealth.
- Holding USD has a cost: the investor gives up the high BRL interest rate differential. With the Selic at 13.75% [11] and US short-term rates far lower, the "carry" given up is large. **Estimate:** a rough guide is that the carry cost per year roughly equals the BRL-minus-USD short-rate gap.
- **Assumption (starting framework, to be set in the IPS):** compute a "currency need" (future USD spending + desired crisis hedge) and treat the USD share as a strategic decision, not a tactical bet on the exchange rate.

## 3. WHAT: asset classes and instruments

Key terms: **CDI** (Certificado de Depósito Interbancário) is the average overnight rate banks charge each other in Brazil and tracks the **Selic** (the central bank's policy rate) very closely; most Brazilian fixed income is quoted as "% of CDI." **Liquidity** is how fast you can sell without a big price cut. **Duration** is how sensitive a bond's price is to interest rate changes (a duration of 5 means roughly a 5% price fall if rates rise 1 percentage point).

### 3.1 Brazil (onshore)

| Instrument | What it is | Risk | Return driver | Liquidity | Tax notes (individual) |
|---|---|---|---|---|---|
| **Tesouro Direto** (Selic, Prefixado, IPCA+) | Federal government bonds bought directly via B3 [17] | Sovereign credit (lowest in BRL); price risk on Prefixado/IPCA+ if sold early | Selic, fixed rate, or inflation + real rate | Daily | Regressive income tax by holding period |
| **CDB** | Bank deposit certificate | Bank credit; covered by FGC up to R$250k per CPF per institution, R$1m per 4 years [13] | % of CDI or fixed | Varies; some daily | Regressive income tax |
| **LCI / LCA** | Bank notes backed by real estate / agribusiness loans | Bank credit; FGC-covered [13] | % of CDI | Lock-up periods | Exempt for individuals as of 2026 [16]; a 2025 proposal to tax them was dropped in the final text, per press reports [16] |
| **Debentures** (incl. incentivized infrastructure) | Corporate bonds | Company credit; no FGC | CDI + spread or IPCA + spread | Thin secondary market | Incentivized ones exempt for individuals |
| **FIIs** | Listed real estate funds | Property and tenant risk; price volatility | Rent income + price | Daily on B3 (can be thin) | Distributions generally exempt for qualifying individuals |
| **FIAGROs** | Agribusiness funds created by Law 14,130/2021 [18] | Agri credit / land risk | Income | Daily (listed) | Similar to FIIs, check current rules |
| **B3 equities** | Brazilian shares | High; country and sector concentrated | Earnings growth, dividends | Daily | Capital gains and dividend rules subject to change |
| **BDRs** | Receipts for foreign shares and ETFs traded on B3; open to retail since 2020 [28] | Foreign equity + FX risk; limited shareholder rights on unsponsored BDRs [28] | Foreign stock + BRL/USD | Daily but thinner than the original | Taxed as Brazilian assets |
| **Funds** | Investment funds under CVM Resolution 175 [19] (fixed income, multimarket, equity, FX) | Depends on mandate; manager risk | Manager skill + asset class | Daily to months | "Come-cotas" semiannual tax on many open funds |

**Note:** uncited tax notes in this table (regressive income tax, FII and incentivized-debenture exemptions, "come-cotas") are **Assumption** pending verification by the Tax agent; Brazilian investment taxation has been under active reform.

### 3.2 United States

| Instrument | Risk | Liquidity | Notes for a Brazilian resident |
|---|---|---|---|
| Treasuries (bills, notes, TIPS) | Lowest USD credit risk; price risk rises with duration | Very high | TIPS pay inflation plus a real yield |
| Equities / ETFs | High; broad ETFs diversify thousands of firms | Very high | Low-cost global or US index ETFs are a core building block |
| Municipal bonds | Low-moderate credit | Moderate | Their US federal tax exemption mostly benefits US taxpayers; low value for a Brazilian resident (**Assumption**) |
| Private funds (PE, VC, private credit, hedge funds) | High; manager-dependent | Low; multi-year lock-ups | Usually require accredited/qualified status |

Investor protections differ: US bank deposits are FDIC-insured up to USD 250,000 per depositor, per bank, per ownership category [25]; SIPC protects brokerage customers up to USD 500,000 (including USD 250,000 cash) against broker failure, **not** against market losses [24].

### 3.3 Alternatives (typical profiles)

| Asset | Return potential | Risk | Liquidity | Main caveat |
|---|---|---|---|---|
| Private equity | Higher than public equity hoped | High, hidden by smooth appraisals | 7–12 year lock-ups (**Estimate**) | Fees and manager dispersion are large |
| Venture capital | Very high dispersion; most funds lag | Very high | 10+ years (**Estimate**) | Returns concentrated in a few managers |
| Real estate (direct) | Income + inflation link | Moderate-high; concentrated | Low | Overlaps with hospitality business exposure |
| Private credit | Income above public bonds | Credit and liquidity risk | Low | Defaults appear late in cycles |
| Commodities / gold | Inflation and crisis hedge | High volatility | High via ETFs | No cash flow; long flat periods |
| Crypto | Speculative | Extreme; custody and fraud risk | High but 24/7 crashes | Taxed as a foreign financial asset under Law 14,754 when held abroad [14] |

**Assumption:** because the principal already owns operating businesses in hospitality and energy, direct real estate and energy assets add *more of the same* risk; the team should prefer alternatives that diversify away from them.

## 4. WHERE: jurisdiction, wrapper and custody

- **Onshore vs. offshore.** Since 1 January 2024, Law 14,754/2023 taxes financial investments held abroad by Brazilian-resident individuals at a flat **15%**, assessed annually in the tax return, and ended tax deferral for many controlled offshore companies [14][15]. Offshore is no longer mainly a tax deferral play; it is a diversification, currency and asset-protection decision.
- **US estate tax for non-US persons.** Nonresident aliens may owe US estate tax on US-situs assets (such as US stocks) above USD 60,000 [23]. **Assumption:** whether the principal counts as a US resident for tax purposes (given study in Florida) is an open question for the Tax agent; it changes this answer completely.
- **Custody.** Split assets across institutions to stay within FGC/FDIC/SIPC limits [13][24][25]; prefer segregated custody at large, regulated custodians; keep a documented list of accounts and access for succession.
- **Vehicle choice** (direct holdings, Brazilian funds, BDRs, US brokerage, offshore company, trust) must be decided by the Tax and Structuring agent before execution.

## 5. WHEN: timing evidence

### 5.1 Time in the market vs. market timing
Missing a few strong days can cut long-run returns sharply, and strong days often cluster near crashes. The behavior gap is measurable: Morningstar estimates the average dollar in US funds earned about 1.2 percentage points a year less than the funds' reported returns over the latest 10-year period studied, with larger gaps in more volatile funds [12].

### 5.2 Valuation signals
- **CAPE** (cyclically adjusted price-to-earnings) divides the price by 10-year average inflation-adjusted earnings; Shiller publishes the US series back to 1871 [6]. High CAPE has been associated with lower 10-year returns, but it can stay high for years [7].
- **Equity risk premium (ERP):** the extra return stocks are expected to earn above government bonds. Damodaran's implied US ERP was about **4.14%** on 1 September 2026 [8].
- **Real yields:** the yield after inflation. US TIPS yields and Brazilian Tesouro IPCA+ yields show what a "safe" real return pays. **Estimate:** with Selic at 13.75% and the central bank projecting 5.6% IPCA inflation for 2026 [11], the ex-ante real policy rate is roughly 7.7% (1.1375/1.056 − 1), which is very high by global standards.
- **Rule for the agents:** use valuation to set *small* tactical tilts within IPS bands, never all-in/all-out moves.

### 5.3 Momentum and trend following
- **Cross-sectional momentum:** stocks that rose most over the past 3–12 months tended to keep outperforming for some months [10].
- **Time-series momentum (trend following):** an asset's own past 1–12 month return tends to persist, then partly reverses later; diversified trend strategies did best in extreme markets [9]. Useful as a risk-control overlay; expect long flat periods.

### 5.4 Dollar-cost averaging (DCA) vs. lump sum
**DCA** means investing a sum in equal parts over time. Vanguard found lump-sum investing beat cost averaging about **two-thirds of the time** (68% for 1976–2022 in the US) because markets usually rise, while DCA still beat holding cash [5]. **Rule:** default to lump sum into the target allocation; use a short, pre-scheduled DCA (for example 3–12 months) only if regret risk might otherwise stop the principal from investing at all. Write the schedule down and do not change it based on news.

### 5.5 Rebalancing rules
- **Calendar:** rebalance once or twice a year.
- **Bands:** rebalance when an asset class drifts beyond a set band (**Assumption:** ±5 percentage points absolute, or ±20% relative for small sleeves).
- Use new cash flows and income first to reduce taxes and FX costs.

### 5.6 The Selic cycle and the CDI's opportunity cost
In Brazil, cash is not "trash." The Copom held the Selic at 13.75% in November 2026 after five cuts since April, citing exchange-rate pressure and inflation expectations above target [11]. Guidelines:
- While real rates are very high, the hurdle for equities, private deals and USD conversion is high. Ask: "Does this beat 100% of CDI after tax, risk and illiquidity?"
- When a cutting cycle is likely, **longer-duration** fixed-rate (Prefixado) and IPCA+ bonds gain value; locking in high real yields can be attractive. This is a rate view and must be labeled as such.
- Business liquidity reserves belong in daily-liquidity Selic/CDI instruments, not in risky assets.

## 6. Decision frameworks the AI must use

### 6.1 Expected value and scenarios
**Expected value (EV)** = the probability-weighted average of outcomes. Always use at least three scenarios (bear / base / bull), each with a probability, a return, and a "what would have to be true" narrative. Report the downside in currency terms, not just percentages.

### 6.2 Base rates / outside view
Start from how similar investments *usually* turn out (the "outside view"), then adjust for specifics. Kahneman and Lovallo showed that decision-makers tend to over-rely on the specifics of their own case and make overly optimistic forecasts [26].

### 6.3 Pre-mortem
Imagine it is three years later and the investment failed; list why. Gary Klein's pre-mortem technique surfaces risks that groups otherwise suppress [22].

### 6.4 Decision checklist
1. Does it fit the IPS (return, risk, liquidity, horizon, currency)?
2. What is the base rate for this type of investment?
3. Bear/base/bull scenarios and EV written down?
4. Does it beat CDI (or US T-bills for USD money) after tax, fees and illiquidity?
5. How does it correlate with the operating businesses and the rest of the portfolio?
6. Position size and maximum loss in BRL and USD?
7. Exit rules: what would make us sell or add?
8. Tax, legal and custody structure confirmed?
9. Pre-mortem done; red-team agent reviewed?
10. Is anyone (including the AI) rushing because of recent news or fear of missing out?

### 6.5 Standard investment memo template
```
INVESTMENT MEMO — <name> — <date> — Author agent: <role>
1. Recommendation (buy/hold/sell/pass) and size (% of liquid portfolio, BRL & USD)
2. Thesis in 3 sentences
3. Fit with IPS and strategic allocation
4. Scenarios: bear / base / bull (probability, return, narrative) and expected value
5. Base rate and outside view
6. Hurdle comparison: vs. CDI / T-bills, after tax and fees
7. Key risks and pre-mortem (top 5 failure reasons)
8. Correlation with operating businesses and existing holdings
9. Liquidity, lock-up, exit plan and review triggers
10. Tax, jurisdiction, vehicle, custody
11. Conviction score (1-5) with justification; confidence in data
12. Sources, data dates, and labeled assumptions
```

### 6.6 Position sizing and the Kelly criterion
The **Kelly criterion** [20] gives the fraction of capital to bet that maximizes long-run growth when you know your odds. For a simple bet: **f = p − (1 − p) / b**, where p is the probability of winning and b is the payoff ratio (win amount per 1 unit lost). Example: 55% win chance, even payoff (b = 1): f = 0.55 − 0.45 = 10%.
Caveats: (1) real probabilities are uncertain, and overestimating them leads to overbetting and large losses; (2) full Kelly produces very deep drawdowns; (3) mathematically, betting half the Kelly fraction keeps about three-quarters of the growth rate with much lower volatility. **Rule:** use Kelly only as an *upper bound* and size at one-quarter to one-half of it, capped by the IPS position limits (see file 07).

### 6.7 Conviction scoring
| Score | Meaning | Maximum size (**Assumption**, set in IPS) |
|---|---|---|
| 1 | Idea only, weak evidence | 0% (watchlist) |
| 2 | Plausible, untested | ≤1% |
| 3 | Solid thesis, base rate supports it | ≤3% |
| 4 | Strong evidence, margin of safety, red-team survived | ≤5% |
| 5 | Exceptional; still subject to concentration limits | ≤8% |

## 7. Behavioral biases and countermeasures

| Bias | Plain description | AI countermeasure |
|---|---|---|
| Loss aversion | Losses hurt about twice as much as equal gains feel good [21] | Show outcomes in total-wealth terms; pre-commit to rebalancing rules |
| Overconfidence / planning fallacy | Forecasts too precise and optimistic [26] | Require base rates and wide scenario ranges |
| Home bias / familiarity | Prefer what is known (Brazil, own sector) [4] | Report country and sector weights vs. world benchmark |
| Recency and herding | Extrapolate recent news; follow the crowd | Cooling-off period for news-driven trades; checklist item 10 |
| Anchoring | Fixate on purchase price or past exchange rate | Evaluate positions on forward-looking merits only |
| Confirmation bias | Seek supporting evidence | Mandatory red-team memo arguing the opposite |
| Disposition effect | Sell winners too early, hold losers too long | Written exit rules in each memo |
| Sunk cost | Keep funding because of money already spent | Ask "Would we invest today at this price?" |
| AI-specific: automation bias | Trust the model output because it is confident | Every number cites a source and date; label estimates |

## Implications for the agent team
- The CIO agent must keep a living IPS and reject any recommendation that cannot be mapped to it.
- All recommendations use the memo template, include scenarios and EV, and compare against CDI and T-bills.
- Treat the operating businesses as part of the portfolio when measuring BRL, sector and real estate/energy exposure.
- Timing decisions are limited to small tilts within IPS bands; default to lump-sum investing and rule-based rebalancing.
- The Tax and Structuring agent signs off on jurisdiction and vehicle before execution; cross-border rules change frequently and must be re-checked.
- A red-team agent challenges every conviction-4 or conviction-5 idea.

## Open questions and assumptions
- The principal's US tax residency status (affects estate tax, reporting, and vehicle choice) is unknown.
- Total net worth, share held in the operating businesses, and liquidity needs of those businesses are unknown; all size limits here are **Assumptions**.
- Rebalancing bands, conviction size caps and the USD target share are illustrative and must be set in the IPS.
- Brazilian tax rules for LCI/LCA, dividends and funds have been under active reform; status as of 2026 is based on press and B3 education sources, not on a primary legal text [16].
- The Selic and ERP figures are point-in-time (November and September 2026) and must be refreshed before use.

## Sources
1. Brinson, G.P., Hood, L.R., Beebower, G.L., "Determinants of Portfolio Performance," Financial Analysts Journal (1986; CFA Institute reprint 1995), https://rpc.cfainstitute.org/en/research/financial-analysts-journal/1995/determinants-of-portfolio-performance (accessed 2026-11-27)
2. Ibbotson, R.G., Kaplan, P.D., "Does Asset Allocation Policy Explain 40, 90, or 100 Percent of Performance?", Financial Analysts Journal, 2000, https://rpc.cfainstitute.org/research/financial-analysts-journal/2000/does-asset-allocation-policy-explain-40-90-or-100-percent-of-performance (accessed 2026-11-27)
3. "Setting the Record Straight on Asset Allocation," CFA Institute Enterprising Investor, 2012, https://blogs.cfainstitute.org/investor/2012/02/16/setting-the-record-straight-on-asset-allocation (accessed 2026-11-27)
4. Vanguard Canada, home bias research paper, 2024, https://www.vanguard.ca/content/dam/intl/americas/canada/en/documents/HOBI_052024_V14_secure.pdf (accessed 2026-11-27)
5. Vanguard, "Cost averaging: Invest now or temporarily hold your cash?", 2023, https://corporate.vanguard.com/content/dam/corp/research/pdf/cost_averaging_invest_now_or_temporarily_hold_your_cash.pdf (accessed 2026-11-27)
6. Shiller, R.J., "Online Data" (US stock market and CAPE since 1871), Yale University, http://www.econ.yale.edu/~shiller/data.htm (accessed 2026-11-27)
7. Campbell, J.Y., Shiller, R.J., "Valuation Ratios and the Long-Run Stock Market Outlook," Journal of Portfolio Management, 1998, https://doi.org/10.3905/jpm.24.2.11 (accessed 2026-11-27)
8. Damodaran, A., Damodaran Online (implied equity risk premium, monthly), NYU Stern, 2026, https://pages.stern.nyu.edu/~adamodar/New_Home_Page/home.htm (accessed 2026-11-27)
9. Moskowitz, T.J., Ooi, Y.H., Pedersen, L.H., "Time Series Momentum," Journal of Financial Economics 104(2), 2012, https://econpapers.repec.org/RePEc:eee:jfinec:v:104:y:2012:i:2:p:228-250 (accessed 2026-11-27)
10. Jegadeesh, N., Titman, S., "Returns to Buying Winners and Selling Losers," Journal of Finance, 1993, https://doi.org/10.1111/j.1540-6261.1993.tb04702.x (accessed 2026-11-27)
11. Banco Central do Brasil, Copom 282nd meeting statement (4 Nov 2026) and minutes, 2026, https://www.bcb.gov.br/content/copom/copomminutes/Minutes_282_v2.pdf (accessed 2026-11-27)
12. Morningstar, "Mind the Gap" US study, 2025/2026 edition, https://www.morningstar.com/business/insights/research/mind-the-gap-2025 (accessed 2026-11-27)
13. Fundo Garantidor de Créditos, "About FGC guarantee," https://fgc.org.br/en/sobre-garantia-fgc (accessed 2026-11-27)
14. Brazil, Lei nº 14.754, de 12 de dezembro de 2023, Presidência da República, 2023, https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/Lei/L14754.htm (accessed 2026-11-27)
15. Ministério da Fazenda, Perguntas e respostas: offshores, Lei 14.754 e IN RFB 2.180, 2024, https://www.gov.br/fazenda/pt-br/acesso-a-informacao/perguntas-frequentes/tributacao-offshore/29-4-24-perguntas-e-respostas-offshores-lei-14-754-e-in-rfb-2-180.pdf (accessed 2026-11-27)
16. B3 Bora Investir, "Investimentos isentos: como declarar LCI e LCA corretamente no Imposto de Renda 2026," 2026, https://borainvestir.b3.com.br/tipos-de-investimentos/renda-fixa/lci-lca-e-lc/investimentos-isentos-como-declarar-lci-e-lca-corretamente-no-imposto-de-renda-2026/ (accessed 2026-11-27)
17. Tesouro Nacional / B3, Tesouro Direto official site, https://www.tesourodireto.com.br/ (accessed 2026-11-27)
18. Brazil, Lei nº 14.130, de 29 de março de 2021 (FIAGRO), https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14130.htm (accessed 2026-11-27)
19. CVM, Resolução CVM nº 175 (investment funds framework), 2022, https://conteudo.cvm.gov.br/legislacao/resolucoes/resol175.html (accessed 2026-11-27)
20. Kelly, J.L., "A New Interpretation of Information Rate," Bell System Technical Journal, 1956, https://www.princeton.edu/~wbialek/rome/refs/kelly_56.pdf (accessed 2026-11-27)
21. Kahneman, D., Tversky, A., "Prospect Theory: An Analysis of Decision under Risk," Econometrica, 1979, https://doi.org/10.2307/1914185 (accessed 2026-11-27)
22. Klein, G., "Performing a Project Premortem," Harvard Business Review, 2007, https://hbr.org/2007/09/performing-a-project-premortem (accessed 2026-11-27)
23. IRS, "Some nonresidents with U.S. assets must file estate tax returns," https://www.irs.gov/individuals/international-taxpayers/some-nonresidents-with-us-assets-must-file-estate-tax-returns (accessed 2026-11-27)
24. SIPC, "What SIPC Protects," https://www.sipc.org/for-investors/what-sipc-protects (accessed 2026-11-27)
25. FDIC, "Deposit Insurance," https://www.fdic.gov/resources/deposit-insurance (accessed 2026-11-27)
26. Kahneman, D., Lovallo, D., "Timid Choices and Bold Forecasts: A Cognitive Perspective on Risk Taking," Management Science, 1993, https://doi.org/10.1287/mnsc.39.1.17 (accessed 2026-11-27)
27. CFA Institute, "Elements of an Investment Policy Statement for Individual Investors," 2010, https://rpc.cfainstitute.org/policy/positions/elements-of-an-investment-policy-statement-for-individual-investors (accessed 2026-11-27)
28. B3, "BDRs não patrocinados nível I" (product page and investor alert), https://b3.com.br/pt_br/produtos-e-servicos/negociacao/renda-variavel/brazilian-depositary-receipts-bdrs-nao-patrocinados-nivel-i.htm; and CVM, Caderno CVM nº 14 – BDR, 2020, https://www.gov.br/investidor/pt-br/educacional/publicacoes-educacionais/cadernos/cvm-caderno-14.pdf (accessed 2026-11-27)
