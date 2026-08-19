# 02 — Finance

> Part of the **Kojiki Decision System**. This repo is the
> **Finance** line. It references the shared ontology in
> [`00-kojiki-ontology`](https://github.com/robfuj/kojiki-ontology) for the
> canonical schemas, taxonomy, decision-rights, and handoff standards.

## Primary question
> Where should resources go and how do we protect economic health?

## Purpose
Economic measurement, planning, capital allocation, liquidity, control, and financial strategy.

## Sub-functions
Accounting, FP&A, Treasury, Tax, Financial Control, Capital Management, Investor Relations, Financial Strategy

## Typical roles
CFO, VP Finance, Controller, FP&A Director, Finance Director, Treasurer, Financial Analyst, Tax Director

## Inputs
Revenue, costs, cash, forecasts, capital requirements, contracts, operating plans.

## Outputs
Budgets, forecasts, financial reports, capital decisions, controls, treasury actions.

## Learning focus
Forecast accuracy; capital efficiency; margin patterns; cash-flow signals; investment outcomes; cost anomalies.

## Operating tree
```text
FINANCIAL STATE →
 OBJECTIVE →
 OPTIONS →
 ECONOMICS →
 ASSUMPTIONS →
 SCENARIOS →
 RISK →
 DECISION →
 ALLOCATION →
 RESULT →
 MODEL UPDATE
```

## Decision states
```text
ASSESSING → MODELING → SCENARIOING → DECIDING → ALLOCATING → MONITORING → REALLOCATING → EXITED
```

## Decision outputs
`Allocate · Hold · Reduce · Increase · Hedge · Reject · Exit`

## Critical prompts (what this function thinks about)
> What are we optimizing?
> What is the expected return?
> What is the downside?
> What assumptions drive the model?
> What happens in the base case?
> What happens in the downside?
> What happens in the upside?
> What is the opportunity cost?
> What is the liquidity impact?
> What risks are we accepting?
> What risks are unacceptable?
> What threshold changes the decision?
> What evidence should trigger reallocation?
> Did the investment produce the expected result?
> What did we learn?

## Canonical record schema (Learning Ledger + Decision Object Fields)
Every decision in this line is recorded as:
- a **Decision Object** — see `schema/decision-object.json`
- a **Learning Ledger** entry — see `schema/learning-ledger.json`

and the agent must run the **Orientation Protocol** first (see `AGENT.md`).

## How this line runs on SYNAPSIS (the cognitive substrate)
Every decision in this line is decomposed through the shared SYNAPSIS transformation
chain ([`00-kojiki-ontology/synapsis`](https://github.com/robfuj/kojiki-ontology/synapsis)):
```
SOURCE → RECORD → EVIDENCE → INTERPRETATION → STRATEGY → INTERACTION → OUTPUT → OUTCOME → LEARNING
```
- **Three steps are dedicated niche bots**: `bots/evidence/` (this line's extraction
 specialist); the shared `synapsis/audit-bot/` (independent audit, org-wide) and
 `synapsis/learning-bot/` (cross-line memory). See `AGENT.md` for the full contract.
- The rest run inline inside this line's agent, each bounded to one authority.
- Meta-rule: *evidence ≠ interpretation ≠ belief ≠ doctrine.* Validate with
 `python3 synapsis/validate.py <record.json>` (in the ontology repo).

## How to use
1. Read `AGENT.md` — the first-run Orientation Protocol.
2. Read `SCHEMA.md` — how this line maps to the universal schema.
3. Read `data/02-finance.json` — the machine-readable spec.
4. See `data/example.json` — one fully worked decision (Decision Object + Ledger).
5. Use `decision-graph.mmd` — agent-decodable operating tree + state model.
6. Validate new records: `python3 tools/validate.py data/<name>.json`
