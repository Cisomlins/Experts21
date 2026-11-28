---
name: ask-the-team
description: "Ask the whole AI Family Office team one question: pick the experts, run them as separate agents in parallel, get Risk Officer sign-off and Red Team dissent, and return one combined memo from the CIO. Use when the user types /ask-the-team or asks to 'ask the whole team' or 'bring in the experts'."
argument-hint: "[question, plus any fictional facts]"
---

# ask-the-team

Runs in the **main session** (not as a subagent), because only the main session can start other agents in Claude Code cloud sessions. This does the orchestrator's job with real, separately-run experts. `@agent-orchestrator` remains the single-agent fallback.

**Question:** $ARGUMENTS

## Rules
- Follow `CLAUDE.md`: the principal is a **fictional example investor**, and the decision-rights table applies. Nothing is executed and nothing is final without the principal's approval.
- Start every expert with the Agent tool, using the expert's name as `subagent_type`. Don't pass `model`; each agent file sets its own.
- Each expert starts with no memory of this conversation. Every brief must contain the full question, the facts given, the assumptions, and exactly what to return.
- Cap: at most 2 rounds and about 10 expert runs per question, unless the user asks for more.
- Never write an expert's view yourself and present it as theirs. If an expert run fails, say so and mark what you filled in.

## Steps

### 1. Frame
Restate the question in one line. List the facts given and the facts missing. If a missing fact is essential, state a labelled **Assumption** and carry on. You can't ask the user mid-run.

### 2. Route (skill `task-routing`)
Pick the fewest experts that cover the question, usually 3–6, from the table in `CLAUDE.md`. Typical routes:

| Question type | Wave 1 experts |
|---|---|
| Allocation, currency, cash | `macro-economist`, `fx-strategist`, `fixed-income-analyst`, `tax-regulatory-brazil`, `tax-regulatory-us` |
| A listed company | `equities-analyst`, `governance-analyst`, `forensic-analyst`, `macro-economist` |
| Structure, succession, dividends | `tax-regulatory-brazil`, `legal-estate-planner`, `operating-businesses-analyst` (+ `tax-regulatory-us` if US assets) |
| Political or geopolitical shock | `geopolitical-analyst`, `macro-economist`, `commodities-energy-analyst`, `fx-strategist` |
| Property, private deals, crypto | `real-estate-analyst` / `private-markets-analyst` / `digital-assets-analyst` + the tax agents |

### 3. Wave 1: specialists in parallel
Launch all wave-1 experts **in one message with several Agent calls**. Brief template:

```
Question: <full question>
Facts (fictional example investor): <facts>
Assumptions: <labelled assumptions>
Your task: <the narrow part for this expert>
Return (max ~350 words): your view with probabilities where relevant, key numbers computed with a tool, top risks, what would change your view, sources with dates, and any "HANDOFF → <agent>: <question>" lines.
```

### 4. Wave 2: challenge in parallel
For any material decision (an allocation change, a purchase, a structure, anything hard to undo), send the wave-1 findings to these two together, in one message:
- `risk-officer`: risk measures, IPS limits, stress result; **APPROVE / APPROVE WITH CONDITIONS / VETO** with reasons.
- `red-team`: pre-mortem, the opposite case, ranked objections, kill criteria.

Route any important HANDOFF lines to their named expert in this wave.

### 5. Wave 3: synthesis
Send everything to `chief-investment-officer` to write the memo (skill `memo-writing`, file 06 §6.5). The memo must keep the Risk Officer's verdict and the Red Team's dissent visible.

### 6. Deliver
Return the CIO's memo, followed by:
- **Experts consulted:** each agent name, the wave it ran in, and a one-line finding.
- **Process notes:** anything that failed or was filled in.
- **Decision needed from the principal**, and the questions for licensed professionals.

Do not save a decision-journal entry unless the user asks. In this public repo, entries may only use the fictional investor.
