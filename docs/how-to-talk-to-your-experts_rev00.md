# How to Talk to Your Experts

> **Purpose:** ready-made prompts for the AI Family Office team: how to ask one expert, how to ask the whole team, and four example questions that make several experts work together through the orchestrator.
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

Start with `@agent-orchestrator`. It decides which experts to bring in, runs them (in parallel when they don't depend on each other), and returns **one combined answer**: the answer first, then each expert's view, risks, dissent, open questions, next steps and sources.

```
@agent-orchestrator <your question>. Bring in the experts and give me one combined answer.
```

For any material investment decision, the orchestrator always includes `chief-investment-officer` (synthesis), `risk-officer` (sign-off or veto) and `red-team` (dissent).

**Make the orchestrator the default for a whole session:**

```bash
claude --agent orchestrator
```

## 3. Four example team prompts

Each prompt gives the facts the team needs; fictional facts are labelled as such. Replace them with your own scenario, but keep real data out of this public repo.

### Example 1: Move cash from CDI to US Treasuries?
```
@agent-orchestrator Should the example investor move 20% of the liquid portfolio from CDI-linked Brazilian fixed income into US Treasuries? Bring in macro, FX, tax (Brazil and US) and risk, plus the red team, and give me one combined answer.
Fictional facts: Brazil tax resident, US non-resident alien; liquid portfolio about R$10 million (70% CDI-linked, 15% Brazilian equities, 15% USD assets); operating businesses in Brazil worth more than the portfolio; needs about US$150,000 a year in USD for 4 years; no IPS yet, moderate risk profile.
```
**Expected experts:** `macro-economist`, `fx-strategist`, `fixed-income-analyst`, `tax-regulatory-brazil`, `tax-regulatory-us`, `risk-officer`, `red-team`, `chief-investment-officer`.

### Example 2: Dividend tax and a holding company
```
@agent-orchestrator Under Law 15.270, the example investor's operating company now pays 10% withholding on dividends above R$50,000 a month. Should profits go through a holding company first? Compare options, including succession effects under the new ITCMD rules, and list the questions for a licensed tax lawyer.
Fictional facts: one operating company in Brazil distributing about R$2 million a year; two adult children as future heirs.
```
**Expected experts:** `tax-regulatory-brazil`, `legal-estate-planner`, `operating-businesses-analyst`, `risk-officer`, `red-team`; `br-tax-advisor-prep` for the question pack.

### Example 3: Is this B3 company worth buying, and can we trust its management?
```
@agent-orchestrator Assess <a listed Brazilian company, e.g., a utility or a bank>: is the price attractive, how good and trustworthy is management, and are there accounting red flags? Give a buy/hold/pass view with probabilities and kill criteria.
```
**Expected experts:** `equities-analyst`, `governance-analyst`, `forensic-analyst`, `macro-economist`, `risk-officer`, `red-team`, `chief-investment-officer`.

### Example 4: A geopolitical shock hits
```
@agent-orchestrator Oil just jumped 15% after new attacks near the Strait of Hormuz. What does this mean for the example portfolio and for an energy-sector operating business over the next 3 months? Give scenarios with probabilities and what to watch.
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

## 6. Test run (Example 1)

*Pending: filled in from a real run of Example 1 through the orchestrator on 2026-11-28.*
