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

Run on 2026-11-28 by calling `orchestrator` as a subagent from a Claude Code cloud session, using the Example 1 prompt.

**What worked**
- The orchestrator chose the expected experts: macro, FX, Brazil tax, US tax, risk, red team and CIO.
- It returned one combined memo in the standard format: answer first, a key-numbers table, reasoning by expert, dissent, open questions, next steps with owners, sources, and a decision-journal entry.
- It used the docs correctly. It cited the macro snapshot (file 08), the tax rules (file 10) and the stress set (file 07), and it flagged one claim as **Unverified** because it was not in the research base.
- It stayed within its decision rights. It labelled the result a **draft, not a recommendation**, because no real Risk Officer sign-off or Red Team review had taken place.
- Its hand calculations were re-checked with Python afterwards and are correct:
  - the carry cost of about R$164k a year
  - the break-even of about 9.3% a year of BRL depreciation
  - the extra cost of about R$776k if the real falls 30%

**What did not work (known issue)**
- **The orchestrator could not launch the other experts.** When it runs as a subagent of the main session, it was not given the `Agent` tool at run time, even though its file lists it. It therefore wrote each expert's view itself and disclosed this at the top of its answer.
- **It had no code tool**, so it did the arithmetic by hand, which breaks the `tool-based-numbers` skill.
- **Work-around until fixed:** run the orchestrator as the *main* agent of a session, so it can call the experts itself:

  ```bash
  claude --agent orchestrator
  ```

  Or ask the experts one by one (`@agent-macro-economist …`, then `@agent-risk-officer …`) and finish with `@agent-chief-investment-officer` to combine them.

**Retest after a fix (same day).** The orchestrator was changed to match the course tutorial: it now has no `tools:` line, so it inherits all tools, and it has a written fallback for when it cannot call experts. It was then re-run in the same session.
- It reported `Read, Grep, Glob, Write, Edit`: the *old* tool list without `Agent`. This suggests the session was still using the cached definition, and that subagents in this cloud session are not given the `Agent` tool.
- It again disclosed that no experts ran, labelled each section as written by the orchestrator, and kept the memo a draft.
- **Status:** unconfirmed until tested in a **new** Claude Code session, which loads the updated file.

**Excerpt of the answer** (fictional example investor; research and education, not advice):
> **Answer:** Mostly yes, but as a currency match for known US dollar spending, not to earn more. Move about 18–20% (about R$1.8–2.0 million) in 3–4 tranches over 6–12 months into a 1–4 year Treasury ladder that matches the US$600,000 of planned spending, holding the bonds directly rather than through a US-listed ETF. If the real stays stable, the move costs about R$164,000 a year after tax; think of that as an insurance premium against the real falling.
>
> **Dissent (red team):** the cost is certain and the protection is not (CDI wins in about 80% of the macro scenarios). Start smaller: move 10% now to cover 3 years, then fund each year's need about 12 months ahead. **Not resolved:** 10% vs. 20%.
>
> **Open questions:** no Investment Policy Statement yet; where the existing ETFs are domiciled (this decides US estate-tax exposure above US$60,000); the actual dates of the USD needs.
