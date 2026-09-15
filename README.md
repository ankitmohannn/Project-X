# Project X

Trade2Options adaptive trading research and execution architecture.

## Mission
Build a robust, regime-aware trading system that prioritizes survival, controlled drawdown, realistic execution and repeatable positive expectancy over spectacular backtests.

Initial research market: **XAUUSD**. Architecture must remain portable to BTCUSD, oil, indices and other markets.

## Operating principle
Project X is not a single strategy and not a blind merger of old bots. Existing code, engines and ideas are evidence sources. Every component is classified **REUSE / MODIFY / REJECT / BUILD NEW** after audit.

`NO TRADE` is a valid system decision.

## Start here (OpenCode / coding agents)
1. Read `AGENTS.md` completely.
2. Read every file in `docs/`, especially `PROJECT_BRAIN.md`, `CURRENT_STATE.md`, and `NEXT_ACTIONS.md`.
3. Execute the current phase autonomously under the gates in `AGENTS.md`.
4. Keep experiments, failures, decisions and state synchronized in this repository.

## Target chain
Data -> Market State/Regime -> Specialist Intelligence -> Opportunity/Confidence -> Risk & Drawdown Governor -> Execution -> Trade Management -> Portfolio State -> Failure Learning -> Validation -> Continuous Research.

## External systems to audit/integrate
- NautilusTrader: https://github.com/nautechsystems/nautilus_trader
- TradingView MCP resources already used by Trade2Options
- Vibe-Trading / existing multi-agent research components
- Existing MT5/EA work as execution references and benchmarks

External repositories are dependencies/research sources unless there is a documented reason to vendor code. Respect upstream licenses.

## Safety boundary
Research, coding, local testing, backtesting, simulation and paper-trading preparation may be automated. **No real-money trading, credential handling, live-account activation, or irreversible external action without explicit human approval.**
