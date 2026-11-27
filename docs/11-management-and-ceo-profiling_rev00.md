# Management and CEO Profiling

> **Purpose:** Give the agent team an evidence-based, legally safe method to assess the quality, incentives and behavioral tendencies of company leaders from public information. **Primary users:** Equity Research agent, Risk agent, Governance/ESG agent, Brazil Markets agent, Red-Team agent, and the Chief of Staff agent that assembles final briefs.

## Summary

- Individual managers matter: tracking executives who move between firms shows that "manager fixed effects" (a persistent personal style that follows the person from firm to firm) explain a meaningful share of differences in investment, financing and organizational choices [1]. Execution skills predict success better than interpersonal skills in private-equity-backed firms [2].
- Some measurable traits carry risk. CEOs classified as overconfident make more acquisitions, and the market reacts worse to their deals [3][4]. Narcissistic CEOs produce bolder strategies and more extreme, more volatile results, not better average results [5].
- Founder and family leadership is, on average, associated with better performance in large US firms, but the evidence is debated and depends heavily on governance [6][7].
- At-a-distance profiling (judging leaders from transcripts, filings and behavior without meeting them) has real but modest predictive power. Linguistic deception models beat chance by only 6–16% [8]; text-inferred personality scores correlate with self-reports at roughly 0.2–0.5 [9]. Treat all such outputs as weak, probabilistic signals.
- Behavioral evidence (what managers *do* with money, shares and boards) is usually more reliable than linguistic evidence (what they *say*). Opportunistic insider purchases, for example, predict returns while routine trades do not [10].
- Every profile must separate **evidence** from **inference**, attach a confidence level to every claim, cite public sources, and never offer a clinical diagnosis.
- In Brazil, the key questions are who the controlling shareholder is, which B3 listing segment applies, and, for state-owned enterprises, how exposed leadership is to political appointment [13][14][15][16].

## 1. Why management quality matters to returns

### 1.1 The core evidence

| Study | What it found | How to use it |
|---|---|---|
| Bertrand & Schoar (2003), *QJE* [1] | Using a panel that follows top managers across firms, manager fixed effects explain a significant part of the variation in investment, financial and organizational practices. Older-cohort executives look more conservative; MBA holders follow more aggressive strategies. | Look at what a CEO did at previous employers; style tends to travel. |
| Kaplan, Klebanov & Sorensen (2012), *Journal of Finance* [2] | Detailed assessments of 316 CEO candidates in buyout and VC-backed firms. Abilities cluster into general ability and a "team vs. execution" dimension. Success relates more to execution skills than to team skills. | Weight evidence of delivery (on time, on budget, on plan) above charisma. Note the sample is PE/VC-backed firms only. |
| Malmendier & Tate (2005, 2008) [3][4] | Overconfidence, measured by CEOs holding in-the-money options too long and by press portrayal, makes investment more sensitive to internal cash flow. Overconfident CEOs are 65% more likely to make acquisitions; their deal announcements draw about −90 basis points vs. −12 for others. | Check option-exercise behavior and acquisition frequency; raise scrutiny on serial acquirers. |
| Chatterjee & Hambrick (2007), *ASQ* [5] | Narcissism measured unobtrusively (photo prominence in annual reports, prominence in press releases, first-person singular pronouns, and cash and non-cash pay). Higher scores led to more strategic dynamism, more and larger acquisitions, and more extreme and volatile performance, with no better or worse average. | A narcissism signal is a *volatility* signal, not a direction signal. |
| Anderson & Reeb (2003), *Journal of Finance* [6] | Families are present in about one third of the S&P 500. Family firms outperformed non-family firms, and performance was better when a family member was CEO. | Do not discount family control automatically; evaluate the governance around it. |
| Fahlenbrach (2009), *JFQA* [7] | About 11% of large US public firms were run by their founder; founder-CEO firms differ in valuation, investment behavior and stock performance. | Founder status is a positive prior, conditional on board oversight and succession planning. |

### 1.2 Limits of this evidence

- Most studies are US-based, use large listed firms, and describe averages, not individual cases. **Assumption:** effect sizes in Brazil may differ because ownership is more concentrated.
- Causality is hard to prove: good firms may attract good CEOs. Several of these papers use statistical designs to address this, but none removes it completely [1][6][7].
- **Recommendation:** use the literature to choose *what to look at*, not to predict a specific CEO's future.

## 2. At-a-distance profiling methods

"At-a-distance" means forming a view of a person without meeting or testing them, using only public material. Each method below lists its scientific support and its main weaknesses.

### 2.1 Linguistic analysis

| Method | Plain-language description | Evidence | Limits |
|---|---|---|---|
| Deception cues in earnings calls (Larcker & Zakolyukina) [8] | A statistical classifier (a model that sorts items into categories) trained on calls later linked to serious restatements. Cues include fewer references to shareholder value, more extreme positive emotion words, and more general-knowledge references. | Built on about 29,663 US call transcripts (2003–2007). Beats random guessing by 6–16%. | Only about 10% of calls were labeled deceptive, so "accuracy" can look high just by saying "truthful" every time [8]. Large profitable US firms only. Many false positives. |
| Dictionary word counts (LIWC) [11] | Linguistic Inquiry and Word Count software counts words in psychologically meaningful categories (emotion, certainty, "I" vs. "we"). | Developers report high reliability for most categories [11]. Widely used in research. | Reliability claims come mainly from the developers; independent critics warn against relying on it without manual checks [12]. Counts words, not meaning or sarcasm. Translated Portuguese dictionaries differ from English. |
| Big Five personality from text [9] | The Big Five are five broad personality traits (openness, conscientiousness, extraversion, agreeableness, neuroticism). Models estimate them from word use in call Q&A sessions. | Gow, Kaplan, Larcker & Zakolyukina scored 4,591 executives across 70,329 calls; out-of-sample correlations were similar to prior research (about 0.21–0.54) [9]. | A correlation of 0.3 means most of the variation is unexplained. Scripted remarks, investor-relations coaching, interpreters and second-language speakers distort results. |
| Large language model (LLM) reading of transcripts [17] | An LLM is an AI system trained on large text collections that can read and score documents. | Jha, Qian, Weber & Yang used an LLM to read 74,586 transcripts and score planned capital-spending changes; the score predicted future capex [17]. | That study measured *corporate plans*, not personality. **Assumption:** LLM personality scoring of CEOs has not been validated to a standard that supports confident individual judgments. LLMs can also be inconsistent between runs and can invent quotes. |

**Recommendation:** use linguistic tools to find *questions to ask* (for example, "Q&A answers became much vaguer this quarter") and to compare a CEO with their own history, rather than with other CEOs.

### 2.2 Behavioral signals

| Signal | What to look at | Evidence / validity |
|---|---|---|
| Insider trading | Opportunistic (non-routine) open-market buys and sells; clustering before news; 10b5-1 plan changes. In Brazil, monthly holdings reports by insiders to the CVM. | Opportunistic trades predict news and returns (about 82 bp/month abnormal return in the original study); routine trades do not [10]. **Strong** signal. |
| Option behavior | Holding deep in-the-money options to expiry. | Used as the main overconfidence proxy [3][4]. **Moderate.** |
| Compensation structure | Pay mix (fixed vs. variable), metrics used (EPS vs. return on capital), vesting horizon, pay relative to peers and the next executive. | CEO cash and non-cash pay are among the narcissism indicators [5]. **Recommendation:** check whether metrics reward value creation or just size. |
| Capital allocation record | Return on invested capital over the cycle, buybacks vs. share price, dividend policy, write-downs of past deals. | **Assumption:** the best single summary of management skill for a long-term investor; supported indirectly by the acquisition evidence [4]. |
| M&A history | Frequency, premiums paid, later impairments, market reaction at announcement. | Overconfident CEOs' deals are received worse [4]; narcissists make more and larger deals [5]. **Strong.** |
| Executive turnover | CFO, general counsel and auditor departures, especially clustered or unexplained. | **Recommendation:** treat as a red flag requiring explanation; no single cited effect size here. |
| Related-party transactions | Contracts with controllers, family members or entities they own. | **Assumption:** especially important in controlled firms (Section 5). Read the Formulário de Referência in Brazil and the proxy statement in the US. |
| Board independence | Share of independent directors, tenure, overboarding, CEO-chair separation, committee composition. | Better-governed firms tend to have higher-performing managers [1]. **Moderate.** |
| Culture signals | Employee review sites, "best places to work" lists, attrition data. | The "100 Best Companies to Work For" earned 2.1–3.5% annual excess returns in 1984–2009 [18]. Individual review sites are noisy and can be manipulated. **Moderate, aggregated only.** |

## 3. Management assessment framework and scorecard

Score each dimension 1 (poor) to 5 (excellent). Record evidence, sources and a confidence level (High / Medium / Low) next to each score. **Recommendation:** default weights below; the Investment Committee can change them.

| # | Dimension | Weight | Key questions | Typical evidence |
|---|---|---|---|---|
| 1 | Capital allocation | 25% | Has ROIC exceeded the cost of capital through a cycle? Were buybacks done below intrinsic value? Were acquisitions written down? | 10-year financials, deal history, impairments |
| 2 | Integrity and candor | 20% | Does management admit mistakes? Do targets move without explanation? Any restatements, enforcement actions or litigation? | Shareholder letters over time, CVM/SEC actions, restatements |
| 3 | Execution track record | 15% | Hit rate on guidance and stated strategic goals; project delivery | Guidance vs. actuals table, prior-employer results [1][2] |
| 4 | Incentive alignment | 15% | Meaningful personal ownership? Pay tied to per-share value and return on capital over 3+ years? | Proxy / Formulário de Referência, insider filings [10] |
| 5 | Succession and bench depth | 10% | Named successors? Key-person risk? Founder transition plan? | Board disclosures, executive tenure |
| 6 | Board quality and independence | 15% | Independent, skilled, not overboarded; real oversight of controller or CEO | Board bios, attendance, segment rules [14] |

### 3.1 Red flags (each triggers an automatic deep-dive)

| Red flag | Why it matters | Source / basis |
|---|---|---|
| Beneish M-score above the warning threshold | The M-score combines eight accounting ratios (for example receivables growth vs. sales growth, gross-margin deterioration, accruals) into a probability of earnings manipulation. It flagged about half of manipulators before public discovery [19]. Thresholds quoted by secondary sources vary (often −1.78 or −2.22). It excludes financial firms and is probabilistic, not proof. | [19] |
| Aggressive or constantly revised guidance | Signals over-promising or pressure to manage earnings | **Recommendation** |
| CFO or auditor change within 24 months, especially without a clear reason | Possible disagreement over accounting | **Recommendation** |
| Serial acquisitions with rising goodwill | Link to overconfidence and poor deal returns [4] | [4][5] |
| Opportunistic insider selling cluster | Informed selling [10] | [10] |
| Large or growing related-party transactions | Value transfer to controller | **Assumption** |
| Sharp change in Q&A language (vaguer, more extreme positive words) | Weak deception signal [8] | [8] |
| Political appointment of SOE leadership | Policy may override shareholders (Section 5.3) | [15][16][20] |

**Recommendation:** a red flag lowers confidence and triggers human review; it never by itself justifies an accusation.

## 4. Ethical and legal limits

1. **Public sources only.** Use filings, transcripts, published interviews, court and regulator records, and reputable press. Do not use leaked documents, hacked data, private social-media accounts, purchased personal data, or pretexting (pretending to be someone to get information).
2. **No clinical diagnoses.** The American Psychiatric Association's "Goldwater Rule" (Section 7.3 of its ethics principles) says it is unethical for psychiatrists to give a professional opinion about a specific person they have not examined [21]. The agents are not clinicians, but the rule is a useful analogy. Write "communication patterns that the research associates with overconfidence [3]" and never "the CEO is a narcissist" or "has a personality disorder."
3. **Privacy law.** Brazil's LGPD (Lei 13.709/2018) treats health and similar data as sensitive personal data with stricter legal bases [22]; Europe's GDPR is similar [23]. Speculation about a named person's mental health is effectively health data. **Recommendation:** never generate it. Profiles are personal data, so store them securely and limit access (see doc 13). In the US, state privacy laws such as the CCPA give residents rights over personal information held by covered businesses [24]. Cross-reference the regulation doc for details.
4. **Defamation.** **Assumption:** in both the US and Brazil, false factual statements that damage reputation can create liability, while clearly labeled opinions based on disclosed facts carry less risk. Keep profiles internal; label inferences as inferences; cite the facts they rest on.
5. **Separate evidence from inference.** Every line in a profile is tagged as **Fact** (directly from a source), **Inference** (reasoned from facts), or **Hypothesis** (weak signal needing confirmation).
6. **Confidence levels.** High = multiple independent primary sources; Medium = one primary source or consistent secondary sources; Low = a single weak signal, linguistic indicator, or model output.

## 5. Brazilian specifics

### 5.1 Controlling shareholders and family companies

**Assumption:** many B3-listed companies have a defined controlling shareholder or family group, so the main agency conflict is controller vs. minority shareholders, not managers vs. dispersed shareholders. Key checks: shareholder agreements (acordos de acionistas), control holding structures, dual-class shares in non-Novo Mercado firms, related-party transactions, whether the CEO is a family member, and the tag-along right (the right of minority holders to sell on the same terms when control is sold).

### 5.2 B3 listing segments

| Feature | Novo Mercado | Nível 2 | Nível 1 / Básico |
|---|---|---|---|
| Share classes | Only voting common shares [14] | Common and preferred allowed | Common and preferred allowed |
| Tag-along | 100% for common shares [14] | 100% for common and preferred [14] | Legal minimum |
| Independent directors | At least 2 or 20%, whichever is greater [13] | Lighter requirements | Lighter requirements |

B3 ran public consultations in 2024 and a restricted hearing in 2025 on a reform proposing a higher independence floor (30%), term limits for "independent" status, overboarding limits, and a "Novo Mercado Alerta" label [13]. **Open item:** the final adopted rules could not be confirmed; check the current Regulamento and the B3 Guia das Companhias before relying on thresholds.

### 5.3 State-owned enterprises and political-appointment risk

- The State-Owned Enterprises Law (Lei 13.303/2016) sets governance rules for SOEs and, in Article 17 §2, bars certain people from board and executive posts, including ministers and senior officials, party leaders, recent campaign participants (36-month quarantine), and union leaders [15].
- In 2023 a preliminary court order suspended those bans; in May 2024 the Supreme Court (STF, ADI 7331) upheld them as constitutional, while keeping appointments already made under the suspension until their terms end [16].
- Political risk is concrete. After the President announced in February 2021 that Petrobras' CEO would be replaced amid a fuel-price dispute, the shares fell about 21% in one session, erasing roughly R$70 billion in market value [20].
- **Recommendation:** for any SOE (Petrobras, Banco do Brasil, Eletrobras-related entities, state utilities), add a "political-appointment risk" line to the profile covering appointment route, the appointee's political ties, fuel or tariff pricing policy, election calendar, and board independence.

## 6. Profile template (the agent's required output)

```
# Management Profile: <Name>, <Role>, <Company> (<ticker>)
Prepared: <date> | Analyst agent: <role> | Review status: Draft / Reviewed by <agent> / Approved by principal
Overall confidence: High / Medium / Low

## 1. Snapshot
| Item | Value | Type (Fact/Inference) | Confidence | Source |
| Tenure, prior roles, education | ... | Fact | High | [n] |
| Founder / family member / professional / political appointee | ... | Fact | High | [n] |
| Ownership (% shares, $/R$ value) and recent insider trades | ... | Fact | High | [n] |

## 2. Scorecard (1–5, with weights)
| Dimension | Score | Key evidence | Confidence | Sources |
| Capital allocation | | | | |
| Integrity & candor | | | | |
| Execution | | | | |
| Incentive alignment | | | | |
| Succession | | | | |
| Board quality | | | | |
| Weighted total | | | | |

## 3. Behavioral tendencies (research-linked, non-clinical)
| Observed pattern | Research link | Type | Confidence | Source |
| e.g., holds deep in-the-money options to expiry | Overconfidence proxy [3] | Inference | Medium | [n] |

## 4. Red flags checklist
| Flag | Present? | Detail | Source |
| Beneish M-score | | | |
| Auditor/CFO change <24m | | | |
| Related-party transactions | | | |
| Opportunistic insider selling | | | |
| SOE / political-appointment risk | | | |

## 5. What would change our view
- Evidence that would raise / lower the score.

## 6. Limitations
- Data gaps, language/translation issues, model outputs used, date of last data.

## 7. Sources
1. ...
```

Rules: no diagnoses; every row has a source and confidence; every model-generated score is labeled "model output, Low confidence unless corroborated."

## Implications for the agent team

- **Equity Research agent:** completes the scorecard for every holding and candidate above a size threshold the principal sets; refreshes after each annual report, CEO change or major deal.
- **Forensic/Risk agent:** computes the Beneish M-score, tracks insider filings (SEC Form 4; CVM insider reports) and auditor/CFO changes; raises red flags automatically.
- **Linguistic analysis:** runs only as a supporting signal; compares a CEO with their own history; outputs are always Low confidence unless corroborated by behavior.
- **Brazil Markets agent:** adds controller structure, listing segment and SOE political-risk lines.
- **Red-Team agent:** challenges every profile with "what is the innocent explanation?" and checks that no clinical language or unsourced claim survived.
- **Compliance gate:** profiles are internal, stored as personal data under doc 13 controls, and never published.

## Open questions and assumptions

- Final content of the 2024–2025 Novo Mercado reform (independence floor, term limits) is unconfirmed [13].
- Malmendier & Tate (2005) is cited from the NBER working-paper version; the published *Journal of Finance* version (vol. 60, 2005) was not opened directly [3].
- Beneish M-score thresholds vary across secondary sources; the 1999 paper was not accessible in full [19].
- No peer-reviewed validation was found for LLM-based inference of individual CEO personality; treat it as experimental.
- Effect sizes from US studies are assumed to apply only directionally in Brazil.
- Defamation and privacy statements are general and must be checked by counsel for any external use.

## Sources

1. Bertrand, M. & Schoar, A., "Managing with Style: The Effect of Managers on Firm Policies," *Quarterly Journal of Economics* 118(4), 2003, https://web.mit.edu/aschoar/www/ceostyle.pdf (accessed 2026-11-27)
2. Kaplan, S., Klebanov, M. & Sorensen, M., "Which CEO Characteristics and Abilities Matter?," *Journal of Finance* 67(3), 2012; NBER WP 14195, https://www.nber.org/papers/w14195 (accessed 2026-11-27)
3. Malmendier, U. & Tate, G., "CEO Overconfidence and Corporate Investment," NBER WP 10807 (published *Journal of Finance*, 2005); NBER Digest summary, https://www.nber.org/digest/may05/ceo-overconfidence-corporate-investment-and-markets-reaction (accessed 2026-11-27)
4. Malmendier, U. & Tate, G., "Who Makes Acquisitions? CEO Overconfidence and the Market's Reaction," *Journal of Financial Economics* 89(1), 2008; NBER WP 10813, https://www.nber.org/papers/w10813 (accessed 2026-11-27)
5. Chatterjee, A. & Hambrick, D., "It's All about Me: Narcissistic Chief Executive Officers and Their Effects on Company Strategy and Performance," *Administrative Science Quarterly* 52(3), 2007, https://pure.psu.edu/en/publications/its-all-about-me-narcissistic-chief-executive-officers-and-their-/ (accessed 2026-11-27)
6. Anderson, R. & Reeb, D., "Founding-Family Ownership and Firm Performance: Evidence from the S&P 500," *Journal of Finance* 58(3), 2003, https://ideas.repec.org/a/bla/jfinan/v58y2003i3p1301-1328.html (accessed 2026-11-27)
7. Fahlenbrach, R., "Founder-CEOs, Investment Decisions, and Stock Market Performance," *Journal of Financial and Quantitative Analysis*, 2009, https://gwern.net/doc/economics/2009-fahlenbrach.pdf (accessed 2026-11-27)
8. Larcker, D. & Zakolyukina, A., "Detecting Deceptive Discussions in Conference Calls," *Journal of Accounting Research* 50(2), 2012, https://ideas.repec.org/a/bla/joares/v50y2012i2p495-540.html ; base-rate critique: Language Log, "Linguistic Deception Detection: Part 1," https://languagelog.ldc.upenn.edu/nll/?p=3608 (accessed 2026-11-27)
9. Gow, I., Kaplan, S., Larcker, D. & Zakolyukina, A., "CEO Personality and Firm Policies," NBER WP 22435, 2016, https://www.nber.org/papers/w22435 (accessed 2026-11-27)
10. Cohen, L., Malloy, C. & Pomorski, L., "Decoding Inside Information," *Journal of Finance* 67(3), 2012; NBER WP 16454, https://www.nber.org/papers/w16454 (accessed 2026-11-27)
11. Boyd, R., Ashokkumar, A., Seraj, S. & Pennebaker, J., "The Development and Psychometric Properties of LIWC-22," University of Texas at Austin, 2022, https://www.liwc.app/static/documents/LIWC-22%20Manual%20-%20Development%20and%20Psychometrics.pdf (accessed 2026-11-27)
12. Hunter, S. & Grant, T., "Is LIWC reliable, efficient and effective for the analysis of large online datasets?," Aston University, https://research.aston.ac.uk/en/publications/is-linguistic-inquiry-and-word-count-liwc-reliable-efficient-and-/ (accessed 2026-11-27)
13. B3, "Segunda Consulta Pública – Evolução do Novo Mercado," 2024, https://b3.com.br/data/files/B7/61/A1/EA/508729106EEC8429AC094EA8/Segunda%20Consulta%20Publica%20-%20Evolucao%20Novo%20Mercado.pdf (accessed 2026-11-27)
14. B3, "Listing segments – Novo Mercado" and "About listing segments," https://b3.com.br/en_us/products-and-services/solutions-for-issuers/listing-segments/novo-mercado/ ; https://www.b3.com.br/en_us/products-and-services/solutions-for-issuers/listing-segments/about-listing-segments (accessed 2026-11-27)
15. Brasil, Lei nº 13.303, de 30 de junho de 2016 (Lei das Estatais), Planalto, https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2016/lei/l13303.htm (accessed 2026-11-27)
16. STF, "STF mantém válidas restrições a indicações políticas para o comando de estatais" (ADI 7331), 2024, https://noticias.stf.jus.br/?p=91460 ; Acórdão ADI 7.331, https://legis.senado.leg.br/norma/38524047 (accessed 2026-11-27)
17. Jha, M., Qian, J., Weber, M. & Yang, B., "ChatGPT and Corporate Policies," NBER WP 32161, 2024, https://www.nber.org/papers/w32161 (accessed 2026-11-27)
18. Edmans, A., "Does the Stock Market Fully Value Intangibles? Employee Satisfaction and Equity Prices," *Journal of Financial Economics* 101(3), 2011, https://repository.upenn.edu/fnce_papers/373 (accessed 2026-11-27)
19. Beneish, M., "The Detection of Earnings Manipulation," *Financial Analysts Journal* 55(5), 1999, https://rpc.cfainstitute.org/research/financial-analysts-journal/1999/the-detection-of-earnings-manipulation (accessed 2026-11-27)
20. Al Jazeera, "Petrobras shares drop as Brazil's Bolsonaro slams pricing policy," 22 Feb 2021, https://www.aljazeera.com/economy/2021/2/22/petrobras-shares-drop-as-brazils-bolsonaro-slams-pricing-policy (accessed 2026-11-27)
21. American Psychiatric Association, Ethics Committee opinion on Section 7.3 ("Goldwater Rule"), 2017, https://www.psychiatry.org/File%20Library/Psychiatrists/Practice/Ethics/APA-Ethics-Committee-Goldwater-Opinion.pdf (accessed 2026-11-27)
22. Brasil, Lei nº 13.709, de 14 de agosto de 2018 (LGPD), Planalto, https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm (accessed 2026-11-27)
23. European Union, Regulation (EU) 2016/679 (GDPR), EUR-Lex, https://eur-lex.europa.eu/eli/reg/2016/679/oj (accessed 2026-11-27)
24. State of California Department of Justice, "California Consumer Privacy Act (CCPA)," https://oag.ca.gov/privacy/ccpa (accessed 2026-11-27)
