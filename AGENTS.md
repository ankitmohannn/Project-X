# Project X — Agent Operating Contract

This file is the highest-level operating instruction for autonomous coding/research agents working in this repository.

## Objective
Build and validate a modular adaptive trading architecture, initially for XAUUSD, designed around robustness, controlled drawdown, realistic execution and long-term positive expectancy. Do not optimize for impressive backtest return at the expense of fragility.

## Autonomous loop
Repeat:

**DISCOVER -> AUDIT -> RESEARCH -> DESIGN -> BUILD -> TEST -> CHALLENGE -> REVIEW -> FIX -> RETEST -> DOCUMENT -> NEXT TASK**

Do not ask the user about routine development decisions. Continue until a defined checkpoint or stop condition is reached.

## Required behavior
- Read repository state before changing anything.
- Preserve reproducibility: data source/version, parameters, assumptions, costs and experiment ID must be recorded.
- Never fabricate market data, test results, broker behavior or performance metrics.
- Never change code merely to make a test pass. Diagnose the cause.
- Treat `NO TRADE` as a valid output.
- Separate market intelligence, strategy logic, risk permission, execution and validation.
- Prefer deterministic/reproducible infrastructure for judging agent hypotheses.
- Audit before reuse. Classify components: `REUSE`, `MODIFY`, `REJECT`, `BUILD NEW`.
- Do not silently overwrite failed experiments. Failures are project assets.
- Use branches/backups for risky refactors and avoid destructive edits to historical systems.
- Keep interfaces modular so XAUUSD intelligence is not inseparable from execution infrastructure.
- Respect third-party licenses and attribution requirements.

## What can run autonomously
Research; repository/code reading; architecture proposals; coding; unit/integration tests; local dependency installation; non-destructive file creation; data-quality checks; backtests; simulations; walk-forward tests; Monte Carlo; parameter perturbation; spread/slippage/latency stress; refactoring; documentation; experiment logging; failure analysis; paper-trading preparation.

## Mandatory stop conditions
Stop and request explicit human approval before:
1. real-money trading or enabling a live execution route;
2. using/requesting broker, exchange or private API credentials/secrets;
3. irreversible/destructive external actions;
4. a major architecture replacement that invalidates accepted project foundations;
5. any action with material financial consequence.

## Source of truth
Maintain these files after meaningful work:
- `docs/CURRENT_STATE.md`
- `docs/NEXT_ACTIONS.md`
- `docs/DECISIONS.md`
- `docs/EXPERIMENTS.md`
- `docs/FAILURE_MEMORY.md`
- `docs/RESEARCH_LOG.md`
- `docs/COMPONENT_AUDIT.md`

## Experiment discipline
Every strategy/research experiment gets a unique ID. Record hypothesis, market/data range, timeframe, rules, parameters, costs, validation method, metrics, failure modes and final status: `PROMOTE`, `RESEARCH`, or `REJECT`.

A strong in-sample result is never sufficient for promotion. Apply out-of-sample/walk-forward and adversarial validation appropriate to the hypothesis.

## Drawdown-first behavior
Risk is a stateful subsystem, not a position-sizing afterthought. Design for states such as `NORMAL`, `CAUTION`, `DEFENSIVE`, `PROTECTION`, `HALT`. State transitions must be explicit, testable and recoverable. Avoid hard-coding arbitrary thresholds before evidence is collected.

## Agent research arena
Create/merge/remove specialist agents only when useful. Candidate specialties include regime, trend/continuation, liquidity, market structure, momentum, mean reversion, volatility expansion, sessions, multi-timeframe context, risk, drawdown, execution, failure analysis and adversarial validation. Agents propose hypotheses; deterministic tests judge them.

## Checkpoint report
At a phase checkpoint report only:
- Completed
- Created/Modified
- Reused/Rejected
- Tests executed
- Results with evidence
- Problems/failures
- Current architecture/state
- Next recommended step
- Decision needed (only if a stop condition applies)

Then continue automatically if no stop condition applies.

## Git behavior
Make coherent commits with descriptive messages. Do not commit credentials, API keys, account statements containing secrets, private tokens or generated caches/large datasets. Keep `.gitignore` current.
