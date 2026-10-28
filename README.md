# Trading Desk — APOS Project Profile v1.0

A lightweight **Agentic Project Operating System (APOS)** project profile for an AI-assisted Trading Desk focused on **IDX / Indonesia**.

The profile organizes a trading/investing workflow into project instructions, orchestration, decision gates, and five method-driven specialist skills. It is designed to support analysis and decision-making without pretending that an LLM is a broker, an autonomous trader, or an independent risk authority.

## Status

**Version:** 1.0  
**Profile status:** `NOT_ADOPTED`  
**Host binding:** `NOT_BOUND`  
**Host conformance testing:** `NOT_RUN`

Publishing or uploading this profile does not mean that a host has loaded, enforced, or validated it.

## Files

### APOS project control

| File | Purpose |
|---|---|
| `PROJECT_INSTRUCTIONS.md` | Core mandate, boundaries, evidence discipline, desk rules, output contract |
| `PROJECT_CONFIG.md` | Operating configuration and intentionally unset parameters |
| `ORCHESTRATOR.md` | Selects the smallest sufficient work path and skills |
| `DECISION_GATES.md` | Scope, evidence, readiness, governance, and execution checks |
| `SKILLS.md` | Registry of the five desk skills |
| `HANDOFF.md` | Minimal cross-session continuation state; not a portfolio ledger |

### Trading Desk skills

| File | Function |
|---|---|
| `FUND_MANAGER.md` | Portfolio construction, sleeves, cash, allocation and rotation |
| `EQUITY_ANALYST.md` | Business, financials, valuation, catalysts and investment thesis |
| `TECHNICAL_TRADER.md` | Screening, charts, price/volume, setup, trigger and invalidation |
| `RISK_MANAGER.md` | Downside, exposure, risk limits and position-sizing method |
| `QUANT_RESEARCHER.md` | Hypotheses, backtests, event studies and empirical validation |

## How to use

1. Put the contents of `PROJECT_INSTRUCTIONS.md` into the target project instruction field.
2. Upload the other ten Markdown files as project Sources, excluding `README.md`.
3. Give the desk the data needed for the specific question: instrument, horizon, source, as-of time, price/trigger/invalidation when relevant, and portfolio/risk inputs only when actually available.
4. The orchestrator should load one primary skill and supporting skills only when material.

Do not assume that uploading Sources means the host will automatically use every file. The model must actually have access to and use the relevant method before claiming that the method was applied.

## Core design

The five skills are **interfaces to methods, not simulated employees**. A single model using several skills remains a **single-model synthesis**, not independent review. No skill creates authority merely because it is named Fund Manager, Risk Manager, or Technical Trader.

The profile deliberately separates:

`analysis → recommendation → readiness → human decision/approval → execution authorization → transaction/position`

The profile contains **no executor**. It does not send, change, or cancel orders, move funds, or claim fills/positions without evidence.

## Trading Desk method boundaries

- Primary market: **IDX / Indonesia**. Other markets are secondary context unless requested.
- Default source mode: **CLOSED-BOOK**.
- Market facts, filings, flow, prices, and rules must not be invented from model memory.
- Flow is evidence, not causation. Broker activity is not proof of manipulation or intent.
- Fundamental valuation requires sector/cycle context; low multiples are not automatically cheap.
- A failed trade does not automatically become an investment.
- Backtest results are research evidence, not proof or production authorization.
- Missing risk budget is not zero risk; missing portfolio data is not an empty portfolio.
- A stop is not a guarantee of realized loss.
- `SINGLE-MODEL SYNTHESIS — not independent risk review` is required for outputs materially affecting capital.

## Three important method decisions

### D01 — Position sizing

The profile uses the operational risk relationship:

`q_risk = B / L`

where `B` is an actually provided risk budget and `L` is the estimated loss per unit under the stated invalidation scenario. Applicable position, liquidity, portfolio, and other caps may then reduce the result. No budget or cap is invented.

### D02 — Fund Manager sleeve accounting

Portfolio construction distinguishes trade vs. invest sleeves and reconciles cash/exposure rather than treating each ticker as an isolated opportunity. A sleeve is an accounting/decision method, not an additional role.

### D08 — IDX executability checklist

Technical Trader checks the market mechanics relevant to an intended transaction: instrument/board/session, ARA/ARB, suspension/reopening, UMA, lot/tick/order mechanics, settlement/funding, and liquidity/exit. The profile intentionally does **not** hard-code current market-rule values; each material check requires appropriate evidence and effective-date/as-of context.

## What this repository is not

This repository is not:

- an autonomous trading system;
- a broker or exchange integration;
- a validated investment strategy;
- a guarantee of execution, fill, or risk control;
- an independent risk committee;
- a substitute for applicable law, exchange rules, broker controls, or professional advice.

Prompt and Markdown instructions can shape model behavior, but they do not create authentication, authorization, source isolation, sandboxing, persistence guarantees, or execution enforcement.

## Baseline and authorship

This profile is derived from the Trading Desk v1.1 operating instruction and APOS project-architecture conventions. The profile is intended as a reusable public reference configuration.

**Author:** Rachmat Efendi

**License:** Copyright © 2026 Rachmat Efendi. Licensed under the [MIT License](LICENSE).

The license grants copyright permissions for this profile only. It is not investment advice, does not make this profile a licensed investment adviser, and provides no warranty of trading outcomes.
