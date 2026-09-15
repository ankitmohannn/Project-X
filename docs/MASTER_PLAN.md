# Master Plan

Project X progresses through evidence gates, not calendar deadlines.

## Phase 0 — Bootstrap
Create source-of-truth docs, repository rules, safety boundary and experiment/failure schemas.

**Gate:** repository is self-explanatory to a fresh coding agent.

## Phase 1 — Forensic Component Audit
Inventory NautilusTrader, Vibe-Trading/agent resources, TradingView MCP resources, relevant existing MT5/EAs and historical research components. Classify each `REUSE / MODIFY / REJECT / BUILD NEW` with evidence, dependencies, license and integration cost.

**Gate:** no major inherited component enters the core without an audit record.

## Phase 2 — Clean Core Architecture
Define interfaces for data, features/state, specialist intelligence, opportunity, risk permission, execution, portfolio state, telemetry and experiment storage. Decide precisely which responsibilities NautilusTrader owns versus Project X intelligence.

**Gate:** modular interfaces and tests exist; strategy logic is not coupled to broker/execution code.

## Phase 3 — XAUUSD Research/Data Environment
Establish authoritative datasets, timezone/session handling, spread/cost assumptions, data-quality tests, reproducible slices and anti-lookahead controls. Integrate TradingView MCP only for roles it can reliably fulfill.

**Gate:** deterministic research dataset and data-quality report.

## Phase 4 — Agent-Based Strategy Discovery
Run independent hypotheses across regime, trend/continuation, liquidity/structure, momentum, mean reversion, volatility expansion, sessions and multi-timeframe context. Include explicit no-trade hypotheses.

**Gate:** candidate ideas have unique experiment IDs and causal/rule definitions, not vague labels.

## Phase 5 — Deterministic Testing
Use appropriate NautilusTrader infrastructure and/or a justified alternative to test candidates with realistic order/execution assumptions. Confirm reproducibility.

**Gate:** baseline tests reproduce exactly within defined tolerance.

## Phase 6 — Adversarial Testing
Stress spread, slippage, latency, parameter perturbation, session changes, volatility extremes, trend/range transitions, missing/noisy data and execution assumptions.

**Gate:** fragile candidates rejected or returned to research.

## Phase 7 — Out-of-Sample Validation
Walk-forward/OOS validation, Monte Carlo where appropriate, regime segmentation, sample-size review, MAE/MFE analysis and failure clustering.

**Gate:** promotion requires evidence beyond in-sample profitability.

## Phase 8 — Drawdown & Risk Governor
Implement/test stateful risk modes: NORMAL, CAUTION, DEFENSIVE, PROTECTION, HALT. Risk permission considers equity/drawdown state, exposure, confidence quality, correlation, execution conditions and recent failure clusters.

**Gate:** risk layer can independently veto opportunities and has tested recovery behavior.

## Phase 9 — Paper Trading
Run end-to-end paper/simulated execution with telemetry and compare expected vs realized behavior.

**Gate:** no unexplained divergence between research and paper execution.

## Phase 10 — Forward Validation
Accumulate sufficient forward observations across changing conditions. Do not use a fixed trade count as proof by itself; judge statistical and regime coverage.

**Gate:** predefined robustness and drawdown criteria satisfied without post-hoc rule changes.

## Phase 11 — Execution Integration Review
Design live adapter/MT5/broker integration only after previous gates pass. Human approval is mandatory before any real-money activation.

## Permanent loop
Every promoted system remains subject to monitoring, failure-memory analysis and revalidation. A promoted model can be demoted or halted when evidence changes.
