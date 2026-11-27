# Regulation and Tax (Brazil and USA)

> **Purpose:** Give the AI Family Office a dated, cited map of the rules that govern (a) the office itself and (b) how the principal's investments and businesses are taxed in Brazil, the USA and across the border. **Primary users:** the Tax and Structuring agent, the Legal/Regulatory agent, the Wealth and Succession agent, the Portfolio/Investment agent (for after-tax returns), the Operating Businesses agent (hospitality and energy), and the Regulatory Monitoring agent.

> **IMPORTANT: This is research, not legal or tax advice.** It summarizes public sources as of 2026-11-27. Rules in both countries changed heavily in 2023–2026, and several are still being regulated or challenged in court. Before acting, the principal must confirm every point with licensed Brazilian professionals (a tax lawyer and a contador) and licensed US professionals (a US tax attorney and/or CPA). Items marked **Unverified:** could not be confirmed against a source during this research. Items marked **Assumption:** are working hypotheses.

## Summary

- **The AI office itself is probably not a regulated adviser in either country, as long as it serves only the principal.** Brazil's CVM requires registration for anyone who *professionally* gives securities advice to others (CVM Resolution 19/2021) [23][24]; the US family office rule excludes offices that advise only "family clients" and are owned and controlled by the family [31][32]. Serving any third party (friends, partners, employees, investors) changes the analysis.
- **Brazil now taxes dividends.** Law 15.270/2025 (in force 2026-01-01) imposes 10% withholding on dividends above R$50,000 per month from the same company to the same individual, 10% withholding on dividends sent abroad, and a minimum annual income tax of up to 10% on individuals with income above R$600,000/year, with a cap that credits corporate tax already paid [1][2][3].
- **Offshore deferral is over.** Since 2024-01-01, Law 14.754/2023 taxes Brazilian residents at a flat 15% each year on foreign financial income and on profits of controlled foreign companies in low-tax or passive situations; exclusive funds in Brazil now suffer semiannual "come-cotas" [6][7][8].
- **A US LLC owned by a Brazilian resident is a live risk.** A 2026 Receita Federal ruling (Solução de Consulta COSIT 56/2026, per commentary) treated a US tax-transparent LLC with non-resident members as a "privileged tax regime," which triggers annual taxation of its profits in Brazil [9].
- **Tax-exempt Brazilian fixed income survived (for now).** Provisional Measure 1.303/2025, which would have taxed LCI/LCA and unified rates, expired on 2025-10-08 without a vote [11].
- **The consumption tax reform is live.** CBS/IBS test rates (0.9% + 0.1%) apply in 2026 with no actual payment for compliant taxpayers; CBS replaces PIS/Cofins from 2027; ICMS/ISS phase out 2029–2032; full system in 2033 [15]. Hotels get a specific regime with a 40% rate reduction but buyers cannot take credits [16].
- **Inheritance tax is rising.** Complementary Law 227/2026 (January 2026) makes progressive ITCMD rates mandatory in all states, uses market value as the base, sets rules for foreign estates and trusts, and excludes VGBL/PGBL from ITCMD [18][19][20].
- **US exposure as a non-resident:** 30% withholding on US dividends (no US–Brazil income tax treaty, **Unverified:** see Section C), portfolio interest is exempt, most capital gains are not taxed, but **US estate tax applies to US-situs assets above US$60,000** [38][39][40][41].
- **If the principal becomes a US tax resident,** they are taxed on worldwide income and must file FBAR/Form 8938 and deal with punitive PFIC rules on Brazilian funds [45]. F-1 student days are generally excluded from the substantial presence test for up to 5 calendar years [43][44].
- **Monitoring is mandatory:** PL 2338/2023 (Brazil's AI bill) is still pending in the Chamber of Deputies [27][30]; state ITCMD laws, CBS/IBS regulations and Law 15.270 adjustments (PL 5.473/2025) are all moving [5][19].

---

## A. Regulating the AI Family Office itself

### A.1 Brazil: when does investment advice require registration?

Brazil's securities regulator, the **CVM** (Comissão de Valores Mobiliários, roughly Brazil's SEC), licenses three relevant professions:

| Activity | Rule | What it covers (plain language) | Registration? |
|---|---|---|---|
| Securities consultant (*consultor de valores mobiliários*) | CVM Resolution 19/2021 | Giving, **on a professional basis**, guidance, recommendations and advice on capital-markets investments to clients [23][24] | Yes; consultancy is exclusive to registered consultants [24] |
| Securities analyst (*analista*) | CVM Resolution 20/2021 | Producing research reports and recommendations on securities, typically published or distributed | Yes (**Unverified:** details not re-checked in this research) |
| Portfolio manager / administrator (*administrador de carteiras*) | CVM Resolution 21/2021 | Managing third-party money with discretion (deciding and executing trades for clients) | Yes (**Unverified:** details not re-checked) |

Recent change: in January 2026 the CVM's Investment Products Superintendence published **Ofício-Circular 2/2026/CVM/SIN** interpreting Resolution 19 (consultant pay and certification, and the line between consultants and investment advisors/assessores) [25].

**Why a private tool is generally different.** The key words in Resolution 19 are "professional" and advice to *clients* [23][24]. An AI system that the principal owns, pays for and uses only for their own decisions has no client, sells no advice and manages no third-party money. On that reading it does not fit any of the three categories. Brazilian securities law also makes unregistered market activity a crime even when done for free (Law 6.385/1976, art. 27-E). **Unverified:** the exact wording of art. 27-E was not re-checked; the "even for free" language means the risk is triggered by serving others, not by charging.

**Uncertainty flags (treat as risk triggers):**
- Sharing recommendations with family members who are separate taxpayers, business partners, employees, or investors in the operating companies.
- Running the office through a company that charges a fee to related companies (e.g., a holding billing the hotel or energy company for "investment advisory").
- Publishing research outputs (could look like analyst activity under Resolution 20).
- Giving the system discretion to trade a portfolio owned by someone other than the principal (could look like portfolio management under Resolution 21).

**Assumption:** CVM has not issued guidance specifically on AI tools used privately by an individual. If the office ever serves a second economic unit, get a CVM opinion from Brazilian securities counsel first.

### A.2 Brazil: data protection (LGPD)

The **LGPD** (Lei Geral de Proteção de Dados, Law 13.709/2018) governs how personal data is processed [26].
- **Personal-use exemption:** the LGPD does not apply to processing "by a natural person for exclusively private and non-economic purposes" (art. 4, I) [26]. A tool used only by the principal for personal wealth decisions may fit, but the exemption is narrow: once the system processes data of **employees, hotel guests, counterparties or family members** in connection with the businesses, the processing is economic and the LGPD applies.
- **Sensitive and financial data:** financial data is not a "sensitive" category under the LGPD, but it is protected by bank secrecy rules and is high-risk in practice. **Assumption:** apply LGPD-grade controls anyway (access control, encryption, logging, a written record of processing).
- **Sanctions:** the ANPD (the data protection authority) can impose fines of up to 2% of a company's revenue in Brazil, capped at R$50 million per infraction (art. 52) [26]. **Unverified:** the cap was not re-checked against the consolidated text during this research.
- **International transfers:** storing data on US cloud servers is an international transfer that needs a legal basis under the LGPD's transfer chapter. **Unverified:** current ANPD standard-clause regulation not re-checked.

### A.3 Brazil: the AI bill (PL 2338/2023)

| Date | Event |
|---|---|
| Dec 2024 | Senate approves PL 2338/2023 (risk-based AI framework, rapporteur Sen. Eduardo Gomes) [27] |
| 2025-03-17 | Sent to the Chamber of Deputies [27] |
| Apr 2025 | Chamber creates a Special Committee (rapporteur Dep. Aguinaldo Ribeiro) [29] |
| Dec 2025 | Vote pushed to February 2026 or later [28] |
| 2026-05-28 | Chamber President says the House will vote in 2026; report expected 9 June [29] |
| 2026-08-03 | Still no vote date in the Chamber [30] |

**Status as of 2026-11-27: Unverified.** No source after August 2026 was found. If enacted, a private advisory tool would likely be low-risk, but obligations on high-risk uses (e.g., credit scoring) could reach the operating businesses. Check the Chamber's tracking page before relying on this.

### A.4 USA: Investment Advisers Act and the family office rule

The **Investment Advisers Act of 1940** requires anyone who, for compensation, advises others about securities to register with the SEC or a state, unless excluded. The **family office rule (Rule 202(a)(11)(G)-1)**, adopted in June 2011 (Release IA-3220), excludes a family office from the definition of "investment adviser" if it [31][32]:
1. gives investment advice **only to "family clients"** (family members, certain key employees, and family entities/trusts);
2. is **wholly owned by family clients**; and
3. is **exclusively controlled** by family members and/or family entities.

A qualifying office avoids registration and most of the Act's substantive rules [31]. The rule does **not** cover employees of family-run businesses as clients [31]. A purely private AI tool that the principal uses for their own account is even further from regulation: there is no "other" person being advised and no compensation. **Assumption:** if the office is later set up as a US entity serving relatives, structure it to meet the three conditions above.

### A.5 USA: SEC and FINRA on AI

| Item | Status | Relevance |
|---|---|---|
| SEC proposal on conflicts from "predictive data analytics" (July 2023) | **Withdrawn** 2025-06-12 with 13 other proposals; notice in Federal Register 2025-06-17. A new proposal would be needed to revive it [33][34] | No AI-specific SEC rule binds advisers today; general fiduciary duty and anti-fraud rules still apply |
| FINRA Regulatory Notice 24-09 and 2026 Annual Regulatory Oversight Report (GenAI section) | Active guidance. Firms using GenAI should cover accuracy and reliability in supervision; autonomous AI agents flagged as a new risk [35][36] | Applies to broker-dealers, not to the principal; useful as a governance checklist for the office |
| SEC 2026 exam priorities on AI | **Unverified:** not retrieved | Monitor |

### A.6 USA: state privacy laws

- **Florida Digital Bill of Rights** (effective 2024-07-01) applies to controllers with **over US$1 billion** global revenue plus another test (e.g., 50%+ revenue from online ads, or an app store with 250,000+ apps); processors are covered regardless of size [37]. It will almost certainly not apply to the principal's office. **Assumption:** other comprehensive state laws (e.g., California) have revenue or data-volume thresholds the office will not meet; vendors used by the office may be covered.

---

## B. Investment taxation, Brazil

### B.1 Income tax on financial investments (individuals)

| Investment | Tax treatment (2026) | Source |
|---|---|---|
| Fixed income (CDB, Treasury bonds, debentures without incentive) | Regressive withholding: 22.5% (≤180 days), 20% (181–360), 17.5% (361–720), 15% (>720) | [10] |
| LCI / LCA (real estate / agribusiness credit notes) | Exempt for individuals. MP 1.303/2025 would have taxed them (5%, later 7.5% proposed) but expired 2025-10-08 | [10][11] |
| CRI / CRA, incentivized infrastructure debentures (Law 12.431) | Exempt for individuals | [10] |
| FII / Fiagro distributions | Exempt if conditions are met: listed on exchange and at least 100 quota holders (raised by Law 14.754); investor limits also apply (**Unverified:** exact investor percentage tests) | [10] |
| Stocks, regular trades | 15% on net monthly gains; **exempt if total stock sales in the month ≤ R$20,000** | [10] |
| Stocks, day trade | 20% | [10] |
| Open-ended funds (long-term) | "Come-cotas": semiannual advance withholding (May and November) at the long-term rate, with regressive top-up at redemption | [6][8] |
| Exclusive funds (single-investor funds) | Since 2024 subject to come-cotas like other funds; stock of past gains taxed in 2023/2024 (an 8% optional early-payment rate was offered) | [6][8] |
| Savings (poupança) | Exempt | [10] |

Note: MP 1.303/2025 had proposed a single 17.5% rate on fixed income and equities and an end to several exemptions; because it expired, **the pre-existing rules above remain** [11]. **Assumption:** the government may re-propose similar measures; the Monitoring agent should track this.

### B.2 Offshore investments and exclusive funds: Law 14.754/2023

Law 14.754 (12 December 2023) changed how Brazilian residents are taxed on foreign assets, effective 2024-01-01 [6][7][8]:

| Topic | Rule |
|---|---|
| Foreign financial investments (bank deposits that pay interest, bonds, foreign funds, ETFs, stocks) | 15% flat, assessed annually in the tax return (DAA/DIRPF), on realized income; exchange-rate variation is part of income [6][7] |
| Losses | Can be offset against gains on other foreign financial investments in the same year (and carried forward under conditions) [7] |
| Controlled foreign entities ("CFC" rule for individuals) | Profits taxed at 15% on 31 December each year, whether or not distributed, if the entity is in a tax haven/privileged regime or earns less than 60% "active" income [6][9] |
| Transparency option | The individual may elect to treat the entity's assets as held directly [9] |
| Foreign tax credit | Allowed up to the Brazilian tax due, not automatic [9] |
| Control test | Includes holdings of spouse and relatives up to the third degree [9] |
| Trusts | Generally transparent: assets remain the settlor's for tax purposes until distribution/death [6] |

**US LLC warning (2026).** Commentary on **Solução de Consulta COSIT 56/2026** reports that the Receita Federal treated a US LLC that is tax-transparent in the US and has non-resident members as being under a "privileged tax regime," so profits are taxed in Brazil annually under the CFC rule; the ruling is criticized for ignoring actual US tax paid [9]. **Unverified:** the ruling text itself was not reviewed.

### B.3 The income tax reform on high incomes and dividends: Law 15.270/2025

Law 15.270 was signed on 26 November 2025, published 27 November 2025, and effective **1 January 2026** [1][4]. It came from PL 1.087/2025 [4].

| Mechanism | Rule | Effective |
|---|---|---|
| Dividend withholding (domestic) | 10% withholding when one company pays one individual **more than R$50,000 in a month**; once over the limit, applies to the **whole** monthly amount; it is an advance on the annual tax [1][2] | Payments from Jan 2026 |
| Dividends paid abroad | 10% withholding on profits/dividends remitted to non-residents [1][2] | Jan 2026 |
| Minimum tax on high incomes (IRPF-M) | Applies to total annual income above R$600,000; rate rises linearly from 0% to 10% between R$600,000 and R$1.2 million; 10% above [1][2] | Calendar 2026 income, assessed in the 2027 return [5] |
| Cap ("redutor") | If corporate tax (IRPJ + CSLL) plus individual tax exceeds the nominal combined rate of 34% (40% insurers, 45% financial institutions), the excess reduces the individual's minimum tax [5] | 2027 return |
| Exclusions from the minimum-tax base | Include certain capital gains (but **not** gains on Brazilian exchange/OTC trades), savings, LCI, CRI, LIG and infrastructure debentures, advances of inheritance; LCA/CRA listed in some summaries but not others [5] | — |
| Transition | Profits earned through 2025 whose distribution was approved by 31 Dec 2025 may be paid in 2026–2028 outside the new rules [3][5] | Deadline passed |

**Open points:** whether "due" corporate tax includes deferred tax and incentives; treatment of interim dividends; and PL 5.473/2025 (in the Senate) proposing more exclusions [5]. Summaries also differ on the transition deadline (one cites 30 April 2026, possibly from a pending bill) [3]. The law also widened the individual exemption for low earners (the "R$5,000/month" exemption) [1]; this is irrelevant to the principal.

**Implication for holding structures:** a Brazilian holding receiving dividends from operating companies is generally not hit by the individual withholding (the withholding targets individuals), but the cash eventually paid out to the principal is. **Unverified:** the treatment of company-to-company dividends under Law 15.270 should be confirmed.

### B.4 Consumption tax reform (CBS/IBS/IS) and the operating businesses

Constitutional Amendment 132/2023 and Complementary Law 214/2025 replace PIS, Cofins, IPI, ICMS and ISS with a dual VAT: **CBS** (federal) and **IBS** (states and municipalities), plus a **Selective Tax (IS)** on harmful goods [14][15].

| Year | What happens |
|---|---|
| 2026 | Test rates: CBS 0.9%, IBS 0.1%; taxpayers that meet the reporting obligations are exempt from paying; PIS/Cofins remain due; Simples Nacional excluded from the test [15] |
| 2027 | CBS at full reference rate (minus 0.1 p.p.); PIS/Cofins extinguished; IBS at 0.1% [15] |
| 2029–2032 | ICMS and ISS reduced progressively (10% per year per the sources) [15] |
| 2033 | ICMS and ISS extinct; full dual VAT [15] |

**Rate:** the combined standard rate is expected around 26.5%–28%; one source reports the CBS reference rate at 8.8% from 2027 [49]. **Unverified:** an updated joint estimate of 27.91% (IBS 18.7%, CBS 9.21%) attributed to a 2026 CGIBS resolution; the Senate is expected to set the final reference rate by 15 Dec 2026 [15].

**Hospitality (hotels, restaurants):**
- Hotels, amusement parks and theme parks: specific regime (LC 214, arts. 277–283), **40% reduction** in CBS/IBS rates, tax base is the value of the service, and **business customers cannot take credits** on hotel services [16].
- Bars and restaurants: specific regime (arts. 273–276), 40% reduction for food prepared on site and non-alcoholic drinks; business buyers cannot take credits [16].
- Travel agencies: same rate as hotels, but customers can credit tax on the intermediation (per secondary sources) [16].
- **Implication:** corporate clients may lose the input credit they had under PIS/Cofins non-cumulative rules, which may pressure corporate room pricing. **Assumption.**

**Energy:**
- The IS does not apply to electricity [17]. Fuels are under a single-phase (monofásico) CBS/IBS regime [14].
- The IS applies to extraction of minerals (oil, natural gas, iron ore; some sources add coal) with a **maximum rate of 0.25%**, and a veto removed an explicit export exemption for extracted minerals, which is contested [17].
- **Unverified:** specific regimes for electricity generation/distribution under LC 214 and LC 227/2026 amendments; confirm with consolidated text.

LC 227/2026 also amended LC 214 and set rules for IBS administration (the CGIBS committee) [18][19].

### B.5 Holdings, ITCMD and succession

**ITCMD** is the state tax on inheritance and gifts (*Imposto sobre Transmissão Causa Mortis e Doação*). **LC 227/2026** (13 January 2026) set national general rules [18][19][20][21]:

| Change | Detail |
|---|---|
| Progressive rates mandatory | All states must adopt progressive brackets; brackets are set by each state; the Senate cap is currently **8%** [19][21] |
| Base | Market value (not the lower "venal" value) [20] |
| Foreign links | If the donor/deceased lived abroad, the heir's state taxes; if both live abroad, the state where Brazilian assets are located [19] |
| Trusts | Creating a trust is not a taxable event; tax applies when assets pass free of charge to the beneficiary, in life or at the settlor's death, whichever comes first [20][22] |
| VGBL / PGBL | Not subject to ITCMD on amounts paid to beneficiaries (consistent with STF Theme 1.214), with conditions reported [19] |
| Effect | Collection still depends on state laws and constitutional waiting periods (*anterioridade*); São Paulo still had a flat 4% rate when reviewed and bills for brackets were pending in SP and MG [19][21] |

**Succession tools compared:**

| Tool | What it is | Main pros | Main cons / 2026 changes |
|---|---|---|---|
| Holding patrimonial (asset holding company) | A Brazilian company that owns the family's assets; parents donate quotas to heirs, often keeping usufruct (right to income) | Avoids probate (*inventário*) delays, centralizes governance | Quota gifts now valued at market value under LC 227 [20]; dividends to individuals subject to Law 15.270 [1]; real estate transfers can trigger ITBI |
| VGBL / PGBL (private pension plans) | Insurance-type plans with named beneficiaries | Outside the estate; no ITCMD per LC 227 [19]; fast payout | IOF on large VGBL contributions was raised by Decree 12.499/2025 (**Unverified:** current thresholds) [12][13]; abuse can be challenged |
| Life insurance | Death benefit to named beneficiaries | Liquidity to pay ITCMD | Cost |
| Offshore trust | Foreign trust under Law 14.754 | Clear tax rules since 2024 [6] | ITCMD on distribution/death [20]; US situs issues if holding US assets |
| Offshore company | Foreign holding | Consolidates foreign assets | Annual CFC taxation [6]; US estate tax issues if not structured properly |

### B.6 Reporting obligations

| Obligation | Who / threshold | Deadline | Source |
|---|---|---|---|
| DIRPF (annual income tax return) | Brazilian residents above the filing thresholds; foreign assets, controlled entities and trusts must be reported | Usually by end of May | **Unverified:** 2026 thresholds and date not re-checked |
| CBE (Declaração de Capitais Brasileiros no Exterior) to the Central Bank | Residents with assets abroad **≥ US$1 million** on 31 Dec (annual); quarterly if **≥ US$100 million** | Annual window 15 Feb – 6 Apr (2026 cycle, data-base 31 Dec 2025) | [47][48] (quarterly threshold from a secondary source) |
| CBE penalties | R$2,500 to R$250,000 | — | [48] |
| Exchange (câmbio) | Remittances go through authorized banks under the modernized exchange framework (Law 14.286/2021); IOF applies | Per transaction | **Unverified:** framework not re-checked |
| IOF on exchange | Decree 12.499/2025 set 3.5% as the general rate on transfers abroad not otherwise covered; Congress suspended it but the STF restored it in July 2025; sources conflict on whether 1.1% still applies to transfers to the investor's own account for investment [12][13] | Per transaction | Confirm current rate with the bank |

---

## C. Investment taxation, USA, and cross-border

### C.1 The principal as a US non-resident alien (NRA)

An **NRA** is a non-US-citizen who does not have a green card and does not meet the substantial presence test.

| Income / asset | US tax on an NRA | Source |
|---|---|---|
| US dividends | 30% withholding at source (FDAP income), no treaty reduction for Brazil | [40]; treaty: **Unverified** (see note) |
| Portfolio interest (most US bonds, bank deposit interest) | Exempt from the 30% tax; reported on Form 1042-S | [41] |
| Capital gains on US stocks | Generally not taxed if present in the US **less than 183 days** in the year; 30% if present 183+ days (unless effectively connected with a US business) | [42] |
| US real estate gains | Taxed (FIRPTA). **Unverified:** details not re-checked | — |
| US estate tax | Applies to **US-situs** assets (US stocks, US real estate, certain other US property) at death; Form 706-NA filing required above **US$60,000**; threshold not inflation-indexed | [38][39] |

**Note on treaties:** the brief states, and it is widely understood, that the USA and Brazil have **no income tax treaty** and no estate tax treaty. **Unverified:** this research did not retrieve the IRS treaty table to confirm. Without a treaty, the full 30% rate applies and there is no foreign tax credit relief agreed by treaty, although Brazil's domestic rules allow credit for foreign tax up to the Brazilian tax due [9].

**Why the US$60,000 matters:** US citizens and residents have a US$15 million estate exemption from 2026 (made permanent by the July 2025 tax law, indexed from 2027) [46]. An NRA has only the US$60,000 threshold (a US$13,000 credit) [38][39]. A Brazilian with US$5 million of US stocks in a personal brokerage account could face a large US estate tax bill (top rate 40%, **Unverified:** rate not re-checked) plus Brazilian ITCMD.

**Blockers (structures that turn US-situs assets into non-US assets):**

| Blocker | How it works | Brazilian side | Caveats |
|---|---|---|---|
| Offshore holding company (non-US) | The principal owns shares of a foreign company, which owns US assets; at death the principal owns foreign shares, generally not US-situs | CFC rules under Law 14.754 (15% annual if passive or low-tax) [6] | Must respect corporate formalities; dividend withholding at 30% still applies at company level |
| Irish-domiciled UCITS ETFs | The principal buys an Irish fund that holds US stocks; the fund is not US-situs | Taxed as a foreign financial investment at 15% on realized income [6] | **Unverified:** the commonly cited 15% US withholding at fund level under the US–Ireland treaty, and that accumulating ETFs defer Brazilian tax until sale |
| US LLC | **Not a blocker by default** (a disregarded LLC is looked through) | May be a "privileged regime" CFC [9] | Avoid as an estate blocker without specific advice |

### C.2 If the principal becomes a US tax resident

A person becomes a US resident for tax purposes by holding a **green card** or by meeting the **substantial presence test**: at least 31 days in the current year and 183 "weighted" days over three years (current-year days + 1/3 of last year's + 1/6 of the year before) [43].

**Student exception:** days in F, J, M or Q student status are excluded ("exempt individual") unless the person has been exempt as a student or similar for any part of more than 5 calendar years; Form 8843 must be filed to claim the exclusion [44]. **Assumption:** the principal is in F-1 status; their five-year clock should be tracked.

Once resident:

| Consequence | Detail | Source |
|---|---|---|
| Worldwide income | Taxed in the US on all income, including Brazilian dividends, rents and business profits | **Assumption:** standard rule |
| FBAR (FinCEN 114) | Foreign financial accounts with aggregate value **> US$10,000** at any time; filed with FinCEN | [45] |
| Form 8938 (FATCA) | Specified foreign financial assets above **US$50,000** at year-end or **US$75,000** at any time (single, living in the US; higher for joint/abroad) | [45] |
| PFIC (Form 8621) | Brazilian funds (FIIs, fixed income funds, VGBL in some analyses) are generally "passive foreign investment companies"; default tax regime is punitive | [45]; VGBL point **Unverified** |
| US estate exemption | US$15 million (2026) if US-domiciled [46] | [46] |
| Double tax risk | Brazil also taxes worldwide income while the principal remains a Brazilian resident; no treaty to resolve dual residence | **Assumption** |

**Cross-border traps:** (1) Brazilian holding companies with passive income can be CFCs/PFICs for US purposes; (2) Brazilian VGBL/PGBL may not be recognized as pensions in the US; (3) Brazil's new dividend withholding and IRPF-M must be coordinated with US foreign tax credits; (4) leaving Brazil requires a formal exit (*Declaração de Saída Definitiva*). **Unverified** for all four; flag for professional review.

### C.3 US LLC and trust structures in Brazil

| US structure | US view | Brazil view (2026) |
|---|---|---|
| Single-member LLC (disregarded) | Transparent | Commentary on COSIT 56/2026: may be a CFC in a "privileged regime," taxed annually at 15% [9] |
| LLC electing corporate status (C-corp) | Separate taxpayer, 21% federal (**Unverified**) | Controlled entity; CFC rules depend on active income test and privileged-regime analysis [6] |
| US revocable trust | Grantor trust | Generally transparent; assets treated as the settlor's [6]; ITCMD on distribution/death [20] |
| US irrevocable trust | Depends on grantor status | Same Law 14.754 transparency rule; ITCMD at transfer to beneficiary [6][20] |

### C.4 CRS and FATCA information exchange

- **FATCA:** US law requiring foreign banks to report US persons' accounts. Brazil and the US have an intergovernmental agreement (Model 1, reciprocal), so Brazilian banks report to the Receita Federal, which reports to the IRS. **Unverified:** agreement details not re-checked.
- **CRS (Common Reporting Standard):** the OECD system; Brazil participates. The US does **not** participate in CRS (it uses FATCA). **Unverified:** not re-checked in this research.
- **Practical effect:** the Receita Federal can see the principal's non-US foreign accounts (via CRS) and, to a lesser extent, US accounts (via reciprocal FATCA). **Assumption:** treat all foreign holdings as visible to Brazil and report them.

---

## D. Regulatory monitoring plan

### D.1 Bodies and feeds

| Body | What to watch | Feed / page | Frequency |
|---|---|---|---|
| CVM | Resolutions, Ofícios-Circulares (e.g., 2/2026 on Res. 19) | gov.br/cvm (legislation, news) [23][25] | Weekly |
| BCB / CMN | CBE rules, exchange regulation | bcb.gov.br; gov.br CBE service [47] | Monthly; Jan–Apr for CBE |
| Receita Federal | Normative Instructions, COSIT rulings (e.g., 56/2026), DIRPF rules, CBS rules | gov.br/receitafederal [15] | Weekly |
| Ministry of Finance | Q&A on Law 14.754, reform materials | gov.br/fazenda [7] | Monthly |
| Congress | PL 2338/2023 (AI), PL 5.473/2025 (Law 15.270 changes), any new LCI/LCA bills | camara.leg.br, senado.leg.br [27] | Weekly |
| State finance offices (SP, others relevant) | ITCMD bracket laws after LC 227 | State official gazettes [19][21] | Monthly |
| CGIBS / Senate | IBS/CBS reference rates (due by 15 Dec 2026) | Senate, CGIBS | Monthly; weekly in Dec |
| ANPD | LGPD regulations, international transfers | gov.br/anpd | Quarterly |
| SEC | Rules, Advisers Act guidance, exam priorities | sec.gov [31][33] | Monthly |
| FINRA | Oversight report, AI notices | finra.org [35] | Quarterly |
| IRS / Treasury | Forms 706-NA, 8938, 8621; treaty table; NRA guidance | irs.gov [38][45] | Quarterly; Jan–Apr |
| FinCEN | FBAR, beneficial ownership (CTA) rules | fincen.gov | Quarterly |
| Florida | Privacy, any state tax changes | flsenate.gov | Semiannual |

### D.2 Change-impact template

Each change should produce one record:

```
Change ID / date detected:
Jurisdiction and body:
Instrument (law, decree, IN, ruling, bill) and number:
Status: proposed / approved / published / in force / suspended / litigated
Effective date(s):
Plain-language summary (3 lines):
What it affects: [ ] AI office regulation [ ] personal investments
  [ ] holdings/succession [ ] hospitality business [ ] energy business
  [ ] US assets [ ] US residency planning [ ] reporting
Estimated impact: amount (R$/US$), direction (+/-), confidence (H/M/L)
Deadline for action:
Recommended next step and owner (agent + human professional):
Sources (primary first):
Reviewed by licensed professional? (Y/N, name, date)
```

**Triage rule (Assumption):** High = changes a tax rate or exemption on more than 5% of net worth, or creates a filing obligation with penalties; Medium = changes cost in an operating business; Low = guidance only.

---

## Implications for the agent team

1. **Keep the office private.** The Legal/Regulatory agent should block any feature that sends recommendations to anyone other than the principal until counsel confirms CVM and SEC positions.
2. **Model after-tax returns with 2026 rules.** The Portfolio agent should apply: regressive table, exemptions (LCI/LCA/CRI/CRA/incentivized debentures/qualifying FIIs), 15% annual on foreign income, 10% dividend withholding above R$50k/month, and the IRPF-M (0–10%) with the 34% cap.
3. **Run a US-situs estate check every quarter.** Flag when US-situs assets held directly exceed US$60,000.
4. **Track US residency days.** Maintain a day counter and the F-1 five-year clock; warn before any green card or extended stay decision.
5. **Review any US LLC** in light of COSIT 56/2026 before using it for investments.
6. **Plan succession under LC 227.** Model ITCMD at progressive rates on market value, by state, and compare holding vs. VGBL vs. trust.
7. **Model CBS/IBS for the hotels** (40% reduction, no credit for corporate guests) and for the energy business (IS on extraction, fuels single-phase), with 2027 as the first real cash year.
8. **Calendar:** CBE (Feb–Apr), DIRPF (by May), come-cotas (May/Nov), FBAR/8938 if US resident (April), Senate reference rate (Dec 2026).
9. **Every output must carry the disclaimer** and list which licensed professional must review it.

## Open questions and assumptions

- **Assumption:** the principal is a Brazilian tax resident, a US NRA in F-1 status, and has not been exempt as a student for more than 5 calendar years.
- **Open:** current Chamber status of PL 2338/2023 after August 2026.
- **Open:** exact transition rule and deadline for pre-2026 profits under Law 15.270, and whether LCA/CRA are excluded from the IRPF-M base; outcome of PL 5.473/2025.
- **Open:** final CBS/IBS reference rates to be set by the Senate (expected by 15 Dec 2026); sector-specific energy rules.
- **Open:** state ITCMD brackets adopted in the principal's state of domicile after LC 227.
- **Open:** current IOF rate on remittances for investment abroad (1.1% vs 3.5%).
- **Unverified:** no US–Brazil income or estate tax treaty; US non-participation in CRS; the Brazil–US FATCA IGA details; Law 6.385 art. 27-E wording; LGPD fine cap; Irish UCITS withholding rate; DIRPF 2026 thresholds; FII investor-level tests; text of COSIT 56/2026.
- **Research limitation:** the web search budget for this research session ran out before several of the unverified items above could be checked, and direct access to some primary sites (planalto.gov.br and some law-firm sites) was blocked in this environment, so several primary texts were accessed only through search summaries.

## Sources

1. Lei nº 15.270, de 26 de novembro de 2025. Senado Federal (Legislação), 2025. https://legis.senado.leg.br/norma/41758136/publicacao/41762089 (accessed 2026-11-27); also https://planalto.gov.br/ccivil_03/_ato2023-2026/2025/lei/L15270.htm
2. Enactment of Law No. 15,270/2025, which establishes dividend taxation, expands the exemption threshold and introduces a minimum tax on high incomes. Mayer Brown, 2025. https://www.mayerbrown.com/pt/insights/publications/2025/12/enactment-of-law-no-15270-2025-which-establishes-dividend-taxation-expands-the-exemption-threshold-and-introduces-a-minimum-tax-on-high-incomes (accessed 2026-11-27)
3. Tax Intelligence ed. 48: Tributação de dividendos. PwC Brasil, 2025. https://www.pwc.com.br/pt/thinking-about-taxes/tax-intelligence/2025/tax-intelligence-ed-48-tributacao-de-dividendos.pdf (accessed 2026-11-27)
4. Publicada lei que trata de tributação de dividendos. Mattos Filho, 2025. https://www.mattosfilho.com.br/unico/lei-tributacao-dividendos/ (accessed 2026-11-27)
5. Novo regime de tributação mínima para altas rendas. Migalhas, 2025. https://www.migalhas.com.br/depeso/446807/novo-regime-de-tributacao-minima-para-altas-rendas (accessed 2026-11-27)
6. Lei nº 14.754, de 12 de dezembro de 2023. Presidência da República (Planalto), 2023. https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/Lei/L14754.htm (accessed 2026-11-27)
7. Perguntas e respostas: offshores, Lei 14.754 e IN RFB 2.180. Ministério da Fazenda, 2024. https://www.gov.br/fazenda/pt-br/acesso-a-informacao/perguntas-frequentes/tributacao-offshore/29-4-24-perguntas-e-respostas-offshores-lei-14-754-e-in-rfb-2-180.pdf (accessed 2026-11-27)
8. Tributação de offshores: Lei 14.754/2023. KPMG Brasil, 2024. https://kpmg.com/br/pt/home/insights/2024/03/tributacao-offshores-lei-14754-2023-.html (accessed 2026-11-27)
9. LLC como regime fiscal privilegiado: alcance e limites da solução. Migalhas, 2026. https://www.migalhas.com.br/depeso/458860/llc-como-regime-fiscal-privilegiado-alcance-e-limites-da-solucao (accessed 2026-11-27)
10. Quais investimentos são isentos de IR? Confira a tabela atualizada de tributação. B3 Bora Investir, 2025. https://borainvestir.b3.com.br/noticias/imposto-de-renda/quais-investimentos-sao-isentos-de-ir-confira-a-tabela-atualizada-de-tributacao/ (accessed 2026-11-27)
11. Câmara derruba MP que previa aumento de impostos (MP 1.303/2025). Nord Investimentos, 2025. https://www.nordinvestimentos.com.br/blog/amp/camara-derruba-mp-1303-aumento-impostos/ (accessed 2026-11-27)
12. Decreto nº 12.499, de 11 de junho de 2025 (IOF). Presidência da República, 2025. https://planalto.gov.br/ccivil_03/_ato2023-2026/2025/decreto/d12499.htm (accessed 2026-11-27)
13. IOF subiu: como fica o imposto sobre dólar, crédito, VGBL e mais após novo decreto. InfoMoney, 2025. https://www.infomoney.com.br/minhas-financas/iof-subiu-como-fica-o-imposto-sobre-dolar-credito-vgbl-e-mais-apos-novo-decreto/ (accessed 2026-11-27)
14. Lei Complementar nº 214/2025 (text). Secretaria de Fazenda de Minas Gerais, 2025. https://www.fazenda.mg.gov.br/empresas/legislacao_tributaria/leis/2025/lc214_2025.pdf (accessed 2026-11-27)
15. Curso CFC–RFB Reforma Tributária do Consumo, Módulo 1 (maio 2026). Receita Federal, 2026. https://www.gov.br/receitafederal/pt-br/acesso-a-informacao/acoes-e-programas/programas-e-atividades/reforma-tributaria-do-consumo/curso/material-de-apoio/curso-cfc-rfb-modulo-1-mombelli_maio-2026-final.pdf (accessed 2026-11-27)
16. Reforma tributária: bares, restaurantes e hotelaria. TaxUp, 2025/2026. https://taxup.com.br/solucoes/reforma-tributaria/bares-restaurantes-hotelaria/ (accessed 2026-11-27)
17. Reforma Tributária: vetada a imunidade do Imposto Seletivo na exportação de bens minerais. Mattos Filho, 2025. https://www.mattosfilho.com.br/unico/imunidade-imposto-seletivo-minerais/ (accessed 2026-11-27)
18. Lei Complementar nº 227, de 13 de janeiro de 2026. Senado Federal (Legislação), 2026. https://legis.senado.leg.br/norma/42042119/publicacao/42256084 (accessed 2026-11-27)
19. Tax Intelligence Raciocínios ed. 05: ITCMD. PwC Brasil, 2026. https://www.pwc.com.br/pt/thinking-about-taxes/tax-intelligence/2026/tax-intelligence-raciocinios-ed-05-ITCMD.pdf (accessed 2026-11-27)
20. ITCMD: principais mudanças trazidas pela LC 227/26. Machado Meyer, 2026. https://www.machadomeyer.com.br/pt/inteligencia-juridica/publicacoes-ij/planejamento-sucessorio/itcmd-principais-mudancas-trazidas-pela-lc-227-26 (accessed 2026-11-27)
21. ITCMD: lei complementar prevê mudanças na tributação de doação e heranças. Lefosse, 2026. https://lefosse.com/noticias/alerta/itcmd-lei-complementar-preve-mudancas-na-tributacao-de-doacao-e-herancas/ (accessed 2026-11-27)
22. Lei afasta interpretação "enviesada" do Fisco para cobrança de ITCMD sobre trusts. CRC-SP, 2026. https://online.crcsp.org.br/portal/noticias/noticia.asp?c=10444 (accessed 2026-11-27)
23. Resolução CVM nº 19/2021 (consolidated). CVM, 2021/2023. https://conteudo.cvm.gov.br/export/sites/cvm/legislacao/resolucoes/anexos/001/resol019consolid.pdf (accessed 2026-11-27)
24. Consultor de Valores Mobiliários. Portal do Investidor (gov.br), n.d. https://www.gov.br/investidor/pt-br/investir/como-investir/profissionais-do-mercado/consultor-de-valores-mobiliarios (accessed 2026-11-27)
25. CVM divulga ofício-circular sobre remuneração e certificação de consultores. Times Brasil, 2026. https://timesbrasil.com.br/investimentos/cvm-divulga-oficio-circular-sobre-remuneracao-e-certificacao-de-consultores/ (accessed 2026-11-27)
26. Lei nº 13.709/2018 (LGPD). Presidência da República, 2018 (as amended). https://planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm (accessed 2026-11-27)
27. Projeto de Lei nº 2338, de 2023. Senado Federal, 2023–2026. https://www25.senado.leg.br/web/atividade/materias/-/materia/157233 (accessed 2026-11-27)
28. PL de inteligência artificial fica para fevereiro de 2026. Teletime, 2025. https://teletime.com.br/16/12/2025/pl-de-inteligencia-artificial-fica-para-fevereiro-de-2026/ (accessed 2026-11-27)
29. Câmara vai votar a IA, diz Motta. Money Times, 2026. https://www.moneytimes.com.br/camara-vai-votar-a-ia-diz-motta-expectativa-e-apresentar-o-relatorio-no-dia-9-de-junho-gaep/ (accessed 2026-11-27)
30. Agência Brasil report on PL 2338/2023 (3 Aug 2026). Agência Brasil, 2026. https://agenciabrasil.ebc.com.br/es/node/1698507 (accessed 2026-11-27)
31. Family Offices, Release No. IA-3220. US SEC, 2011. https://www.sec.gov/rules/final/2011/ia-3220.pdf (accessed 2026-11-27)
32. Staff Responses to Questions About the Family Office Rule. US SEC, n.d. https://www.sec.gov/divisions/investment/guidance/familyofficefaq.htm (accessed 2026-11-27)
33. Withdrawal of Proposed Regulatory Actions, Federal Register Vol. 90 No. 115. US SEC / GovInfo, 2025. https://www.govinfo.gov/content/pkg/FR-2025-06-17/html/2025-11110.htm (accessed 2026-11-27)
34. SEC clears unfinished rulemakings from regulatory agenda. Ropes & Gray, 2025. https://www.ropesgray.com/en/insights/alerts/2025/06/sec-clears-unfinished-rulemakings-from-regulatory-agenda (accessed 2026-11-27)
35. 2026 FINRA Annual Regulatory Oversight Report: GenAI. FINRA, 2025. https://finra.org/rules-guidance/guidance/reports/2026-finra-annual-regulatory-oversight-report/gen-ai (accessed 2026-11-27)
36. FINRA flags generative AI risks and governance expectations. DLA Piper, 2025. https://www.dlapiper.com/en-ie/insights/publications/2025/12/finra-flags-generative-ai-risks-and-governance-expectations (accessed 2026-11-27)
37. Florida Enacts the Digital Bill of Rights. White & Case, 2023. https://www.whitecase.com/insight-alert/florida-enacts-digital-bill-rights-joining-growing-privacy-landscape (accessed 2026-11-27)
38. Estate tax for nonresidents not citizens of the United States. IRS, n.d. https://www.irs.gov/businesses/small-businesses-self-employed/estate-tax-for-nonresidents-not-citizens-of-the-united-states (accessed 2026-11-27)
39. Some nonresidents with U.S. assets must file estate tax returns. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/some-nonresidents-with-u-s-assets-must-file-estate-tax-returns (accessed 2026-11-27)
40. Fixed, determinable, annual, or periodical (FDAP) income. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/fixed-determinable-annual-periodical-fdap-income (accessed 2026-11-27)
41. Federal income tax withholding and reporting on other kinds of U.S. source income paid to nonresident aliens. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/federal-income-tax-withholding-and-reporting-on-other-kinds-of-us-source-income-paid-to-nonresident-aliens (accessed 2026-11-27)
42. The taxation of capital gains of nonresident students, scholars and employees of foreign governments. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/the-taxation-of-capital-gains-of-nonresident-students-scholars-and-employees-of-foreign-governments (accessed 2026-11-27)
43. Substantial presence test. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/substantial-presence-test (accessed 2026-11-27)
44. Exempt individual – Who is a student. IRS, n.d. https://www.irs.gov/individuals/international-taxpayers/exempt-individual-who-is-a-student (accessed 2026-11-27)
45. Comparison of Form 8938 and FBAR requirements. IRS, n.d. https://www.irs.gov/businesses/comparison-of-form-8938-and-fbar-requirements (accessed 2026-11-27)
46. Estate tax alert: new $15 million federal exemption becomes law. Morgan Lewis, 2025. https://www.morganlewis.com/zh-cn/pubs/2025/08/estate-tax-alert-new-15-million-federal-exemption-becomes-law (accessed 2026-11-27)
47. Preencher Declaração de Capitais Brasileiros no Exterior. gov.br / Banco Central do Brasil, n.d. https://www.gov.br/pt-br/servicos/preencher-declaracao-de-capitais-brasileiros-no-exterior (accessed 2026-11-27)
48. Declaração CBE – data-base 2025 – fim de prazo de coleta. Migalhas, 2026. https://www.migalhas.com.br/depeso/452965/declaracao-cbe--data-base-2025--fim-de-prazo-de-coleta (accessed 2026-11-27)
49. Alíquota da CBS será de 8,8% após fase de testes em 2026. APET, 2026. https://apet.org.br/?p=137228 (accessed 2026-11-27)
