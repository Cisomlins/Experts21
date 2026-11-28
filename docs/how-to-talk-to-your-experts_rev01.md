# How to Talk to Your Experts

> **Purpose:** ready-made prompts for the AI Family Office team: how to ask one expert, how to ask the whole team, and four example questions that make several experts work together through the orchestrator.
> **Revision rev01 (2026-11-28):** `/ask-the-team` is now the main way to ask the whole team, because a subagent cannot start other agents in Claude Code cloud sessions (see §6).
> **Date:** 2026-11-28. The "investor" in every example is the **fictional example investor** used throughout this public repo (`CLAUDE.md`, Rule 1). Never paste real personal data into these prompts in this repository.

## 1. Ask one expert

Type `@`, pick the agent from the list, then ask your question:

```
@agent-tax-regulatory-brazil How is a US-listed ETF taxed for a Brazilian resident under Law 14.754?
```

```
@agent-macro-economist Give me this week's macro brief for Brazil and the US.
```

```
@agent-risk-officer Run the standard stress set on the example portfolio and tell me the worst case in BRL and USD.
```

The full list of agents and what each one does is in `CLAUDE.md` ("The team"). You can also ask in plain words ("Ask the risk officer to …"), and Claude will usually pick that agent.

## 2. Ask the whole team

Type `/ask-the-team` followed by your question and the facts:

```
/ask-the-team <your question>. Fictional facts: <facts>.
```

The skill runs in your main session, which is allowed to start agents. It works in three waves:
1. **Specialists, in parallel:** the right experts for the question, each run as a separate agent.
2. **Challenge, in parallel:** `risk-officer` gives APPROVE / APPROVE WITH CONDITIONS / VETO, and `red-team` argues the opposite case.
3. **Synthesis:** `chief-investment-officer` writes one combined memo that keeps the Risk verdict and the Red Team dissent visible.

**Single-agent fallback:** `@agent-orchestrator <question>` gives one agent's answer. In Claude Code cloud sessions it cannot call the other experts, and it says so at the start. In a terminal, `claude --agent orchestrator` makes the orchestrator the main agent, and then it can call the experts itself.

## 3. Four example team prompts

Each prompt uses `/ask-the-team` and gives the facts the team needs; fictional facts are labelled as such. Replace them with your own scenario, but keep real data out of this public repo.

### Example 1: Move cash from CDI to US Treasuries?
```
/ask-the-team Should the example investor move 20% of the liquid portfolio from CDI-linked Brazilian fixed income into US Treasuries? Bring in macro, FX, tax (Brazil and US) and risk, plus the red team, and give me one combined answer.
Fictional facts: Brazil tax resident, US non-resident alien; liquid portfolio about R$10 million (70% CDI-linked, 15% Brazilian equities, 15% USD assets); operating businesses in Brazil worth more than the portfolio; needs about US$150,000 a year in USD for 4 years; no IPS yet, moderate risk profile.
```
**Expected experts:** `macro-economist`, `fx-strategist`, `fixed-income-analyst`, `tax-regulatory-brazil`, `tax-regulatory-us`, `risk-officer`, `red-team`, `chief-investment-officer`.

### Example 2: Dividend tax and a holding company
```
/ask-the-team Under Law 15.270, the example investor's operating company now pays 10% withholding on dividends above R$50,000 a month. Should profits go through a holding company first? Compare options, including succession effects under the new ITCMD rules, and list the questions for a licensed tax lawyer.
Fictional facts: one operating company in Brazil distributing about R$2 million a year; two adult children as future heirs.
```
**Expected experts:** `tax-regulatory-brazil`, `legal-estate-planner`, `operating-businesses-analyst`, `risk-officer`, `red-team`; `br-tax-advisor-prep` for the question pack.

### Example 3: Is this B3 company worth buying, and can we trust its management?
```
/ask-the-team Assess <a listed Brazilian company, e.g., a utility or a bank>: is the price attractive, how good and trustworthy is management, and are there accounting red flags? Give a buy/hold/pass view with probabilities and kill criteria.
```
**Expected experts:** `equities-analyst`, `governance-analyst`, `forensic-analyst`, `macro-economist`, `risk-officer`, `red-team`, `chief-investment-officer`.

### Example 4: A geopolitical shock hits
```
/ask-the-team Oil just jumped 15% after new attacks near the Strait of Hormuz. What does this mean for the example portfolio and for an energy-sector operating business over the next 3 months? Give scenarios with probabilities and what to watch.
```
**Expected experts:** `geopolitical-analyst`, `commodities-energy-analyst`, `macro-economist`, `fx-strategist`, `operating-businesses-analyst`, `risk-officer`, `red-team`.

## 4. Other useful requests

| You want to… | Ask |
|---|---|
| Add or change an expert | `@agent-agent-builder Add an agent for agribusiness land, reusing existing skills.` |
| Check a recommendation's quality later | `@agent-prompt-eval-engineer Score last quarter's forecasts in the decision journal.` |
| Prepare for a meeting with your accountant | `@agent-br-tax-advisor-prep Build the question pack for my contador on Law 15.270.` |
| Check the repo before publishing | `@agent-security-privacy-engineer Scan the repo for secrets and personal data.` |

## 5. Tips

- **Give the facts.** The team has no real portfolio data (public repo). State the scenario in the prompt, or the experts will say what is missing.
- **Ask for a format and length** ("one page", "a table", "about 700 words"). It keeps the cost down.
- **Dated data:** the macro and geopolitics snapshots in `docs/` are as of 2026-11-27. Experts are told to refresh them, but say "use today's data" if timing matters.
- **Nothing is executed.** The team never moves money, places orders or signs anything. Its tax and legal answers end with questions for a licensed professional.

## 6. Test runs (Example 1)

### Runs 1–3: `@agent-orchestrator` cannot call the experts in cloud sessions
- **Runs 1 and 2 (this session):** the orchestrator returned a well-formed combined memo, but it had no `Agent` tool, so it wrote every expert's view itself. It disclosed this at the start each time and kept the memo a draft.
- **Change made between runs 1 and 2:** the orchestrator now has no `tools:` line, so it inherits all tools (as in the course tutorial), and it has a written fallback for when it cannot call experts.
- **Run 3 (a new Claude Code session):** the orchestrator now had the inherited tools (shell, web search), which confirms the change loaded. It still had no `Agent` tool.
- **Conclusion:** in Claude Code cloud sessions, a subagent is not allowed to start other agents. Only the main session can. Hence the `/ask-the-team` skill (§2).

### Run 4: `/ask-the-team` works
Run on 2026-11-28 in a cloud session. Eight experts ran as **separate agents** in three waves, about 3½ minutes of agent time:

| Wave | Agents (in parallel) | Key finding |
|---|---|---|
| 1 | `macro-economist` | CDI beats unhedged Treasuries in all three 24-month scenarios on rates alone (probability-weighted +27.7% vs. +14.5% in BRL) |
| 1 | `fx-strategist` | Current USD covers 1.8 years of needs. Break-even BRL depreciation is about 10.5% in year 1. Recommends 10% in tranches |
| 1 | `fixed-income-analyst` | A direct T-bill/note ladder matched to the needs. Sell CDBs above the FGC limit first and LCI/LCA last |
| 1 | `tax-regulatory-brazil` | IOF 1.1% if declared as investment. Law 14.754 taxes interest and FX gains at 15%, with FX gains taxed at each roll |
| 1 | `tax-regulatory-us` | Treasury interest is exempt for a non-resident. The real US estate-tax exposure is the existing ETFs, if they are US-domiciled (about US$64.6k) |
| 2 | `risk-officer` | **APPROVE WITH CONDITIONS** for +10% in tranches; no approval yet for +20% (interim limits) |
| 2 | `red-team` | **Dissent:** 10% leaves the US$600k liability about US$149k short, and an unhedged known USD expense is itself a bet. It re-checked the key numbers in Python |
| 3 | `chief-investment-officer` | Combined memo: 10% now, plus a written plan to fund the remaining gap before month 36 |

**Excerpt of the CIO memo** (fictional example investor; research and education, not advice):
> **Recommendation:** move 10% of the liquid portfolio now (R$1.0 million, about US$179k after IOF) in 4 monthly tranches into a T-bill/note ladder timed to months 12, 24, 36 and 48. The second 10% is not approved yet.
>
> **Resolving 10% vs. 20%:** the Red Team is right that this is a liability to hedge, not a bet. The Risk Officer is right that +20% sits at the interim ceiling and there is no IPS yet. So: 10% now, and fund the remaining gap of about US$149k before month 36. That happens through either a pre-set FX trigger or a Risk-reviewed proposal at the 6-month review, which may use B3 dollar futures.
>
> **Decision needed from the principal:** approve or reject +10%; choose how the gap is funded; commission a draft IPS; confirm the existing ETFs' domicile.

**Issues found in run 4 (for a later fix)**
- Some primary data sites (treasury.gov, api.bcb.gov.br, irs.gov) were blocked by the session's network settings. The experts used the dated snapshot in `docs/` and labelled live yields as estimates.
- The CIO memo said its decisions were "logged in the decision journal", but no journal file exists yet and nothing was written. A journal location is still to be set up.
