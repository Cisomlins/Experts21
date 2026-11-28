# Geopolitics and Politics
> **Purpose:** Give the agent team frameworks, a dated landscape, monitoring methods and templates for political and geopolitical risk analysis, focused on Brazil and the USA and then the world. **Primary users:** Geopolitical and Political Risk agent, Regulatory agent, Chief Economist / Macro agent, Risk Manager, Portfolio Strategist, and the Operating Businesses agent.

> **Privacy edit (rev01, 2026-11-28):** the "principal" in this file is a **fictional example investor**: a Brazil-resident investor with US assets who owns operating businesses. Hospitality and energy are used only as illustrative sectors. No real person's data is in this public repository. Content is otherwise unchanged from the previous revision.

## Summary
- Political risk is analyzed as **likelihood × market impact × duration**. Established methods include Eurasia Group's annual Top Risks, BlackRock's Geopolitical Risk Dashboard (which scores risks by likelihood and market attention) and the Caldara–Iacoviello **GPR index**, which counts news articles about geopolitical tensions [1][2][3].
- **Most geopolitical shocks fade within weeks for broad equity markets. Shocks that change energy supply, monetary policy or a country's fiscal path can last much longer.** The 2026 Iran war and the closure and later restriction of the Strait of Hormuz are a live example of a lasting shock [12][13].
- **US (as of 2026-11-27):** Democrats won both chambers in the 3 November 2026 midterms (about 56–44 in the Senate and at least 259 House seats), so divided government starts in January 2027 [6]. The Supreme Court struck down IEEPA tariffs in February 2026 [8]. Kevin Warsh became Fed chair in May 2026 amid a debate over Fed independence [9].
- **Brazil:** Lula won re-election on 25 October 2026 with 51.79% against Flávio Bolsonaro (48.21%) [4]. The PL party won the largest blocs in both the Chamber (121 seats) and the Senate (about 28 seats from 2027), so Congress will constrain the government [5]. Markets sold off sharply, then recovered partially after Luiz Carlos Trabuco was named finance minister [17][18].
- **US–Brazil:** relations are tense. A 25% Section 301 tariff on some Brazilian goods has applied since July 2026, a new aircraft and sugar tariff was proposed on 25 November, and Brazil has taken the dispute to the WTO [10].
- **Global:** US–China tensions are managed through repeated truces (the Busan truce was extended to January 2027) [14]. Russia–Ukraine talks have stalled [15]. Maduro was removed in Venezuela [16]. BRICS met in New Delhi in September [19].
- The agents must monitor with balanced sources and quantitative trackers (GDELT, ACLED, prediction markets), express probabilities, and keep analysis separate from opinion.

## 1. Frameworks for political and geopolitical risk

### 1.1 Core definitions
- **Political risk:** the chance that political decisions or events (elections, laws, regulation, expropriation, unrest) change the value of an investment or business.
- **Geopolitical risk:** risk from tensions between states (war, sanctions, trade conflict, terrorism) [3].
- **Event risk vs structural risk:** an event is a discrete shock (a coup, a strike). Structural risk is a slow-moving shift (de-globalization, fiscal decay, institutional erosion).

### 1.2 Reference frameworks
| Framework | What it does | How we use it |
|---|---|---|
| **Eurasia Group Top Risks** | An annual ranked list of the year's top 10 risks plus "red herrings" (issues that get attention but are unlikely to drive instability). The 2026 list put "US political revolution" first and also included "The Donroe Doctrine" (US control of the Western Hemisphere), "Russia's second front," "China's deflation trap" and "Zombie USMCA" [1] | Annual baseline. Check against our own list each January |
| **BlackRock Geopolitical Risk Dashboard** | Tracks about 10 top risks. Each gets a likelihood rating and a market-attention indicator based on text analysis of analyst reports and news [2] | A model for our scorecard. Distinguish "priced in" from "under-appreciated" |
| **Caldara–Iacoviello GPR index** | Monthly and daily index built from the share of newspaper articles mentioning geopolitical tensions, back to 1900. Higher GPR is associated with lower investment and employment and higher downside tail risk [3] | Quantitative input. Alert when the daily GPR spikes above its 90th percentile (**Assumption:** a threshold to calibrate) |
| **PESTLE / country risk ratings** | Political, economic, social, technological, legal, environmental checklist | Scorecard structure (section 6) |

### 1.3 Transmission channels to markets
1. **Energy and commodities** (supply disruption → oil and gas prices → inflation → central banks).
2. **Trade policy** (tariffs → margins, supply chains, FX).
3. **Fiscal path** (election promises → debt → yields, currency).
4. **Institutions** (central-bank and court independence → risk premium).
5. **Sanctions and capital controls** (frozen assets, payment-system access).
6. **Risk sentiment** (safe-haven flows to the USD, US Treasuries and gold).

### 1.4 How geopolitical events historically affected markets
- **Typical pattern:** equity markets sell off on the shock and then recover within weeks to a few months when the event does not change the economic trajectory. **Assumption:** this pattern is widely reported in broker event studies of the S&P 500. The search budget ran out before a specific study could be retrieved, so the Research agent should source one, such as the LPL or Deutsche Bank event tables.
- **Exceptions that last:** shocks that change energy supply (the 1973 oil embargo, 1990 Kuwait), that coincide with monetary tightening or recession, or that change a country's fiscal or institutional path. Caldara and Iacoviello find that elevated *threats* as well as *acts* depress real activity [3].
- **2026 live examples:**
  - The Iran war (from 28 February 2026) and the Hormuz closure took Brent to a 52-week high of about $126 on 30 April. Brent was still around $91–97 in late November as Hormuz stayed restricted. The shock persisted because it hit supply [12][13].
  - Brazil's election: the Ibovespa fell 10% at the open on 26 October and triggered the B3 circuit breaker. The close is reported as −13.9% or −17%, and sources disagree. The BRL lost ground. Assets **recovered partly within a month** after a market-friendly finance minister was named [17][18]. That is a "political shock that fades when the policy signal changes."

## 2. Current landscape (dated snapshot as of 2026-11-27)

> Every item is sourced. Where sources conflict, the conflict is noted. Re-verify before use.

### 2.1 United States: politics and policy
- **Midterms (3 November 2026):** Democrats won the Senate (about 56–44 after the Alaska race was called on 17 November) and the House (at least 259 seats, with a few races uncalled as of 24 November). The President keeps the veto, and the Senate filibuster still limits legislation [6]. **Implication:** gridlock from January 2027, more congressional oversight, and a harder path for tax and spending bills. The executive will likely rely more on executive action and trade tools.
- **Trade and tariffs:** the Supreme Court ruled 6–3 on 20 February 2026 that IEEPA (the emergency-powers law) does not authorize tariffs. Refunds run through CBP's CAPE process. A temporary 10% Section 122 surcharge ran from 24 February to 24 July 2026, and the Court of International Trade later invalidated it for the plaintiffs, with an appeal pending. Section 232 and 301 duties remain the main tools [8].
- **Fiscal:** the FY2026 deficit was $2.0 trillion (6.2% of GDP), and debt held by the public reached 100% of GDP. Lower-than-expected customs revenue contributed [7].
- **Fed independence:** Kevin Warsh was confirmed 54–45 (some reports say 55–45) and took office as chair on 22 May 2026. Powell stayed on as a governor. A court injunction kept Governor Lisa Cook in office after the administration tried to remove her [9]. The Fed **raised** rates in September 2026, and Cook and Hammack dissented in October in favor of another hike (see file 08).

### 2.2 Brazil: politics
- **Presidential election:** first round on 4 October 2026, with Flávio Bolsonaro (PL) at 47.03% and Lula (PT) at 45.16%. In the runoff on 25 October, **Lula won 51.79% to 48.21%**, with turnout of 80.78% [4].
- **Congress (from February 2027):** PL won 121 of 513 Chamber seats, the largest bloc (up 24). The PT–PCdoB–PV federation won 88 seats. In the Senate, 54 of 81 seats were contested, and PL is projected to hold about 28 seats against about 9 for the PT [5]. **Implication:** the government will need the "Centrão" (the large bloc of center and center-right parties that trade support for budget resources and posts) for majorities. Constitutional amendments need three-fifths of both houses, which will be hard. Opposition-driven investigations and impeachment rhetoric are possible.
- **Fiscal politics:** Lula campaigned on more social spending. Investors had expected a Bolsonaro win and repriced fiscal risk. JPMorgan cut its BRL and rates recommendation to market weight [17]. Luiz Carlos Trabuco (chairman of Bradesco) accepted the finance ministry on 26 November. The dollar fell 4% to about R$5.51 on 27 November [18]. TS Lombard's base case is a modest fiscal reform that avoids a 2027 crisis [17].
- **STF (Supreme Court):** the STF remains central to Brazilian politics, deciding cases on electoral matters, platform regulation, taxes and the January 2023 riots. **Not verified in this cycle:** no current-state search was completed on 2026 STF rulings or appointments, so the Regulatory agent should update this item.

### 2.3 US–Brazil relations
- 2025 background: the US imposed an extra 40% "national emergency" tariff on top of a 10% baseline, linked partly to the prosecution of Jair Bolsonaro and to tech regulation. The February 2026 Supreme Court ruling voided those IEEPA duties [10].
- July 2026: USTR imposed a **25% Section 301 tariff** on some Brazilian goods. It excludes beef, orange juice, aircraft and parts, and energy. Brazil requested a WTO panel, and the US blocked it [10].
- 25 November 2026: the US proposed further tariffs, including 10% on finished aircraft (an Embraer exposure) and measures on sugar. A separate 12.5% tariff applies under a forced-labor Section 301 case. A bilateral working group set up in September has stalled [10]. PIIE argues the exemptions show the limits of the strategy [11].

### 2.4 US–China
The October 2025 Busan truce cut tariffs and paused Chinese rare-earth export controls. It was extended in September 2026 to 10 January 2027. China extended its critical-minerals pause by two months in early November [14]. Trump was scheduled to visit China for APEC in November and Xi to visit the US for the G20 in December. **The outcome of the November meetings could not be verified** [14]. Brazil gains soybean market share when US–China trade is disrupted (file 08).

### 2.5 Latin America
- **Venezuela:** a US military operation captured Nicolás Maduro on 3 January 2026, and he is held in New York. Delcy Rodríguez leads an interim government that cooperates with Washington. Oil output was about 1.16 million barrels a day in October 2026 (OPEC secondary sources). The government's plan targets 2.9 million b/d by about 2036. The US is the largest buyer [16].
- Eurasia Group's "Donroe Doctrine" risk describes a US push for direct influence over the Western Hemisphere [1]. That frames US relations with Brazil, Colombia, Mexico (USMCA review) and Cuba.

### 2.6 Russia–Ukraine
The first US-mediated talks in nine months took place in Abu Dhabi on 10–11 November 2026. They produced a prisoner exchange but no breakthrough. Ukraine rejected ceding all of Donbas. The Kremlin says another round could come "soon" with no date set. The FT reported a US target of a deal by early January 2027 [15]. Russia controls about a fifth of Ukraine, and its battlefield gains slowed in 2026 [15].

### 2.7 Middle East and energy geopolitics
- **The 2026 Iran war:** US–Israeli strikes began on 28 February 2026. Iran closed the Strait of Hormuz (confirmed 2 March). The US imposed a naval blockade on 13 April. A ceasefire on 21 April and a 17 June memorandum followed. Sources **disagree** on whether the ceasefire collapsed in July (Wikipedia) or nominally continues with limited strikes (one tracker) [12].
- **As of 26 November:** Hormuz is "restricted." Iran exempts India, China, Iraq and Qatar from its curbs. The US says the main routes are free of mines. New tanker incidents occurred, and Houthis attacked Saudi Arabia's Ras Tanura refinery. Brent is around $91–97, but analysts expect a 2027 surplus, and OPEC+ is likely to roll over output targets [12][13].
- **Energy geopolitics for Brazil:** higher oil prices help Petrobras and Brazil's oil exports, which narrowed the current-account deficit per the IMF (file 08). They hurt fuel-intensive sectors such as aviation and tourism.

### 2.8 BRICS
The 18th summit in New Delhi (12–13 September 2026) unanimously adopted a 140-paragraph declaration. It called for restraint in the Middle East without condemning either side, and it announced no common currency [19]. **Assessment (Estimate):** BRICS remains a forum for coordination, not a bloc. Brazil uses it to diversify partners, which can create friction with Washington.

## 3. Election cycles and markets
- **Brazil:** election years bring volatility in the BRL, the DI curve and the Ibovespa, priced on the candidates' fiscal stances. 2026 confirmed it: polls and markets favored the opposition candidate, and the incumbent's win caused a single-day crash [17]. **Assumption:** the 2002 pre-election sell-off and the 2014 and 2018 patterns are similar historical cases. The Research agent should source exact moves. After the vote, markets re-price quickly on **cabinet signals** (especially the finance minister) and the **first budget**, as with Trabuco in 2026 [18].
- **US:** midterms usually produce divided government. **Assumption:** studies of the presidential cycle often find the 12 months after midterms historically strong for US equities. Treat this as a weak base rate, not a rule, because sample sizes are small. In 2026, Democratic control of Congress raises odds of investigations, budget brinkmanship (debt-ceiling and shutdown risk) and limits on new fiscal expansion.
- **Rules for the agents:** use polls and prediction markets as probabilities, not certainties. Model market reaction by scenario *before* the vote. Expect polling errors of several points (2026: the first-round leader lost the runoff [4]).

## 4. Monitoring: how the agents should watch
| Layer | Sources | Use |
|---|---|---|
| Wire news | Reuters, AP, Bloomberg, FT; Valor, Folha, Estadão, O Globo | Facts, first reports |
| Official | White House, USTR, Treasury/OFAC, Fed; Planalto, Fazenda, BCB, TSE, STF, Câmara/Senado | Primary documents |
| Event data | **GDELT** (a free global database of news events coded by actor and tone, updated every 15 minutes) [20]; **ACLED** (curated data on political violence and protests by location) [21] | Trend detection, unrest heat maps |
| Indices | Caldara–Iacoviello GPR [3]; BlackRock dashboard [2]; Economic Policy Uncertainty index | Quantitative regime signal |
| Prediction markets | Polymarket, Kalshi; Brazilian platforms where legal | Crowd probabilities. Check liquidity, and beware manipulation and thin markets |
| Think tanks (balanced) | CSIS, CFR, Brookings, Heritage, AEI, PIIE, Carnegie, Chatham House; Brazil: FGV (IBRE, CPDOC), Insper, CEBRI, IFI (Senate fiscal watchdog) | Analysis. Always pair viewpoints from across the spectrum |
| Risk consultancies | Eurasia Group [1], Oxford Analytica | Annual and periodic baselines |

### 4.1 Building scenarios and assigning probabilities
1. **Define the question** precisely, with a date and a resolution criterion (for example, "Will Hormuz traffic exceed 80% of pre-war levels by 31 March 2027?").
2. **Start from a base rate** (how often similar situations resolved a given way), then adjust for specifics (superforecasting method [22]).
3. **Triangulate** with prediction-market prices, expert surveys and our own model, and record why each differs.
4. Write **3–4 scenarios** with probabilities summing to 100%, a market impact for each, and **signposts**.
5. **Update** in small steps as signposts move, and log Brier scores (a measure of forecast accuracy).

### 4.2 Avoiding partisan bias
- **Balanced sourcing:** for each political topic, cite at least one source from each side of the political spectrum, or neutral primary data.
- **Separate layers:** label sections **Facts** (sourced), **Analysis** (causal reasoning) and **Judgment** (probabilities). Never use **Opinion** (what *should* happen) in investment memos.
- **Market lens only:** assess policies by their effect on cash flows, rates, FX and risk, not on moral merit.
- **Neutral language:** use official names and titles, and avoid loaded labels.
- **Red-team review:** before any high-impact call, a second agent argues the opposite case.
- **Symmetry check:** would the same evidence produce the same rating if the other party had done it?

## 5. Illustrative scenario set (Estimate, as of 2026-11-27)
| Theme (6–12 months) | Scenario | Prob. | Signposts |
|---|---|---|---|
| Hormuz / Iran | Gradual reopening with a negotiated deal | 35% | Direct US–Iran talks; blockade eased; tanker transits up |
| | Frozen conflict, restricted strait | 45% | Continued incidents; Brent $85–100 |
| | Re-escalation, closure | 20% | Mine attacks spread; Brent above $110 |
| Brazil governance | Pragmatic fiscal deal with Centrão | 45% | Trabuco package passes; 2027 budget meets targets |
| | Gridlock, slow erosion | 40% | Targets eased; spending-rule exceptions |
| | Confrontation (fiscal and institutional) | 15% | Rule abandoned; clashes between Congress and the STF; BRL above R$6 |
| US–Brazil trade | Negotiated de-escalation | 30% | Working group resumes; exemptions widened |
| | Status quo plus targeted tariffs | 50% | Aircraft and sugar tariffs implemented |
| | Broad escalation | 20% | New Section 301 actions; sanctions on officials |

## 6. Templates

### 6.1 Country risk scorecard
```
COUNTRY RISK SCORECARD — <Country>   Date: <YYYY-MM-DD>   Analyst agent: <name>
Scale 1 (low risk) – 5 (high risk); Trend: ↑ worsening / → stable / ↓ improving

| Dimension                         | Score | Trend | Key evidence (cited) | Signpost to watch |
|-----------------------------------|-------|-------|----------------------|-------------------|
| Political stability & governance  |       |       |                      |                   |
| Policy predictability (fiscal)    |       |       |                      |                   |
| Monetary/central-bank credibility |       |       |                      |                   |
| Rule of law & courts              |       |       |                      |                   |
| Regulatory risk (energy, tourism) |       |       |                      |                   |
| External/geopolitical exposure    |       |       |                      |                   |
| Trade & sanctions exposure        |       |       |                      |                   |
| Social unrest / security          |       |       |                      |                   |
| FX & capital-flow risk            |       |       |                      |                   |
| Overall (weighted)                |       |       |                      |                   |

Weights (default): equal; Portfolio Strategist may override.
Market pricing check: CDS 5y, FX implied vol, sovereign spread — is risk priced?
Implications for principal: operating businesses (by sector) | portfolio
Sources: numbered list
```

### 6.2 Event-impact assessment
```
EVENT-IMPACT ASSESSMENT   Event: <name>   Date/time detected: <UTC>   Agent: <name>
1. Facts (sourced, ≥2 independent): what happened, who, where
2. Classification: event vs structural; channel(s): energy | trade | fiscal | institutions | sanctions | sentiment
3. Historical analogues + base rate of lasting market impact
4. Scenarios (prob. sum 100%): escalation / contained / reversal — each with duration
5. Market impact grid (by scenario): S&P 500, Ibovespa, UST 10y, DI, BRL, DXY, Brent, gold, sector names
6. Principal impact (example sectors): energy ops (fuel, power prices, supply), hospitality (bookings, FX, travel advisories), portfolio exposures
7. Is it priced? (market move so far vs scenario-weighted fair impact)
8. Recommended actions (for human review): hedge / monitor / no action
9. Signposts & next review time
10. Confidence (L/M/H) and dissent from red-team agent
11. Sources
```

## Implications for the agent team
- The Geopolitical agent maintains a living Top-10 risk register with likelihood, market attention and principal impact, modeled on BlackRock's dashboard [2], and reviews it weekly with the Macro agent.
- Priority watch items now: **Hormuz/oil**, the **Trabuco fiscal package and the 2027 budget**, **US–Brazil Section 301 escalation**, **US–China truce expiry on 10 January 2027**, the **Fed under Warsh and the new Democratic Congress**, and **Russia–Ukraine talks**.
- Translate every political call into P&L channels for the operating businesses (examples: energy (fuel, power regulation, oil prices) and hospitality (FX, tourist flows, travel safety)).
- Enforce the bias controls in section 4.2 on every political memo.
- Escalate any event-impact assessment rated "High" to the principal within the same day.

## Open questions and assumptions
- **Not verified:** the outcome of the November 2026 APEC Trump–Xi meeting; whether the Iran ceasefire formally holds; current STF rulings and composition; the final count of uncalled US House seats; the exact Ibovespa close on 26 October 2026.
- **Not verified:** historical event-study statistics (days to bottom and recovery) and the Brazil 2002/2014/2018 election market moves. These are labeled as assumptions because the web search budget ran out.
- Scenario probabilities are agent **estimates** and should be checked against prediction markets.
- **Assumption:** the new Brazilian Congress takes office in February 2027 and the new US Congress in January 2027, per standard constitutional calendars.

## Sources
1. "The Top Risks of 2026," Eurasia Group, 2026, https://www.eurasiagroup.net/issues/top-risks-2026 (accessed 2026-11-27)
2. "Geopolitical Risk Dashboard," BlackRock Investment Institute, ongoing, https://www.blackrock.com/corporate/insights/blackrock-investment-institute/interactive-charts/geopolitical-risk-dashboard (accessed 2026-11-27)
3. Caldara, D., Iacoviello, M., "Measuring Geopolitical Risk," American Economic Review 112(4), 2022; data at https://www.matteoiacoviello.com/gpr.htm (accessed 2026-11-27)
4. "Election Guide: Brazil 2026," IFES ElectionGuide, 2026, https://electionguide.org/elections/id/5254/ ; "2026 Brazilian general election," Wikipedia, https://en.wikipedia.org/wiki/2026_Brazilian_general_election (accessed 2026-11-27)
5. "Eleições 2026: veja como ficou a composição partidária da Câmara," TV Senado, 2026, https://www12.senado.leg.br/tv/programas/noticias-1/2026/10/eleicoes-2026-veja-como-ficou-a-composicao-partidaria-da-camara ; "Novo Congresso: como fica o tamanho das bancadas partidárias," CNN Brasil, 2026, https://www.cnnbrasil.com.br/eleicoes/eleicoes-como-fica-o-tamanho-das-bancadas-partidarias-do-congresso/ (accessed 2026-11-27)
6. "2026 midterm election results: House, Senate," CNBC, 2026, https://www.cnbc.com/2026/11/04/2026-midterm-election-results-live-updates.html ; "2026 Midterm Results: Which Races Are Still Undecided?," US News, 2026, https://www.usnews.com/news/national-news/articles/2026-midterm-results-which-races-are-still-undecided (accessed 2026-11-27)
7. "Monthly Budget Review: Summary for Fiscal Year 2026," Congressional Budget Office, 2026, https://www.cbo.gov/publication/61986 (accessed 2026-11-27)
8. "Supreme Court Strikes Down IEEPA Tariffs; Trump Responds With Section 122 Global Surcharge," Troutman Pepper Locke, 2026, https://www.troutman.com/insights/supreme-court-strikes-down-ieepa-tariffs-trump-responds-with-section-122-global-surcharge/ ; "US Trade Court Strikes Down Section 122 Tariffs," Skadden, 2026, https://www.skadden.com/insights/publications/2026/05/us-trade-court-strikes-down-section-122-tariffs (accessed 2026-11-27)
9. "Kevin Warsh confirmed as Fed chair, succeeding Jerome Powell," CNN, 2026, https://edition.cnn.com/2026/05/13/economy/kevin-warsh-confirmation-trump-fed-chair ; "Senate confirms Trump pick Warsh as chairman of the Federal Reserve," PBS NewsHour, 2026, https://www.pbs.org/newshour/politics/senate-confirms-trump-pick-warsh-as-chairman-of-the-federal-reserve-following-powell (accessed 2026-11-27)
10. "USTR Section 301 Action on Brazil's Unreasonable Acts, Policies, and Practices," USTR, 2026, https://ustr.gov/about/policy-offices/press-office/press-releases/2026/july/ustr-section-301-action-brazils-unreasonable-acts-policies-and-practices ; "US Proposes Surprise New Tariffs on Brazil Imports, Including 10% Duty on Aircraft," US News/Reuters, 2026, https://www.usnews.com/news/top-news/articles/2026-11-25/us-proposes-higher-tariffs-on-brazil-imports-including-10-duty-on-aircraft ; "Brazil Condemns U.S. Decision to Impose 25% Tariffs," TIME, 2026, https://time.com/article/2026/07/16/brazil-condemns-us-tariffs-lula-trump-greer/ (accessed 2026-11-27)
11. "Trump's new tariffs on Brazil reflect the weakness of US trade strategy," Peterson Institute for International Economics, 2026, https://www.piie.com/blogs/realtime-economics/2026/trumps-new-tariffs-brazil-reflect-weakness-us-trade-strategy (accessed 2026-11-27)
12. "2026 Iran war" and "2026 Iran war ceasefire," Wikipedia, 2026, https://en.wikipedia.org/wiki/2026_Iran_war ; "Iran Ceasefire Status 2026," MilitarySpend tracker, https://militaryspend.org/iran-ceasefire-status ; "Strait of Hormuz FAQ," hormuz.now, https://hormuz.now/faq (accessed 2026-11-27)
13. "Oil price today: Brent edges up after fresh tanker attacks near Strait of Hormuz," Invezz, 2026, https://invezz.com/news/2026/11/26/oil-price-today-hormuz-tanker-attacks-brent/ ; "Oil Prices Face a 2027 Supply Glut Despite Rising Middle East War Risks," Investing.com, 2026, https://www.investing.com/analysis/oil-prices-face-a-2027-supply-glut-despite-rising-middle-east-war-risks-200692469 (accessed 2026-11-27)
14. "China extends pause on rare earth export curbs for two months," The National, 2026, https://www.thenationalnews.com/news/us/2026/11/09/china-extends-pause-on-rare-earth-export-curbs-for-two-months/ ; "Time Bought, Leverage Preserved: Outcomes of the Trump–Xi Summit in Washington," Heritage Foundation, 2026, https://www.heritage.org/china/report/time-bought-leverage-preserved-outcomes-the-trump-xi-summit-washington (accessed 2026-11-27)
15. "Russia and Ukraine agree to a large prisoner exchange as talks end with no major breakthrough," PBS NewsHour, 2026, https://www.pbs.org/newshour/world/russia-and-ukraine-agree-to-a-large-prisoner-exchange-as-talks-end-with-no-major-breakthrough ; "Peskov claims Ukraine-Russia peace negotiations may resume soon," NV, 2026, https://english.nv.ua/nation/kremlin-says-new-ukraine-peace-talks-could-take-place-soon-50661656.html (accessed 2026-11-27)
16. "U.S. managed $12 billion in Venezuelan oil revenue, State Department says," The Washington Post, 2026, https://www.washingtonpost.com/world/2026/11/12/us-managed-12-billion-venezuela-oil-revenue-state-department-says/ ; "Venezuela expects to increase oil production to 2.9 million b/d over the next decade," S&P Global Commodity Insights, 2026, https://spglobal.com/energy/en/news-research/latest-news/crude-oil/112426-venezuela-expects-to-increase-oil-production-to-29-million-bd-over-the-next-decade (accessed 2026-11-27)
17. "Lula's election win leaves Brazil facing a fiscal tightrope," CNBC, 2026, https://www.cnbc.com/2026/10/27/lula-brazil-election-markets-fiscal-policy.html ; "Trading halted in Brazil as stocks sink following Lula reelection," Nikkei Asia, 2026, https://asia.nikkei.com/business/markets/trading-halted-in-brazil-as-stocks-sink-following-lula-reelection (accessed 2026-11-27)
18. "Dólar hoje cai 4%, a R$ 5,51, com anúncio de Trabuco na Fazenda," InfoMoney, 2026, https://www.infomoney.com.br/mercados/dolar-hoje-abertura-fechamento-comercial-turismo-27112026/ (accessed 2026-11-27)
19. "BRICS summit 2026: What are the key takeaways?," Al Jazeera, 2026, https://www.aljazeera.com/news/2026/9/13/brics-summit-2026-what-are-the-key-takeaways (accessed 2026-11-27)
20. "The GDELT Project," GDELT, ongoing, https://www.gdeltproject.org/ (accessed 2026-11-27)
21. "Armed Conflict Location & Event Data (ACLED)," ACLED, ongoing, https://acleddata.com/ (accessed 2026-11-27)
22. Tetlock, P., Gardner, D., *Superforecasting: The Art and Science of Prediction*, Crown, 2015 (book).
