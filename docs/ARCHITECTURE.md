# Target Architecture

## Principle
Project X separates **understanding**, **opportunity**, **permission**, and **execution**. A bullish signal is not automatically a trade.

## Layers
### 1. Data & Context
Historical/live market data, session/calendar context, spread/cost observations, TradingView MCP context where validated, and later broker/execution feeds.

### 2. Market State Engine
Produces explicit state features: trend/range/transition, volatility, liquidity/structure context, session, multi-timeframe alignment and data/execution quality. Regime inference must expose confidence/uncertainty.

### 3. Specialist Intelligence
Independent modules/agents evaluate hypotheses: trend, liquidity, structure, momentum, mean reversion, volatility expansion, sessions and MTF context. Outputs are structured evidence, not direct broker orders.

### 4. Opportunity & Confidence
Combines compatible evidence into candidate opportunities. Must support `NO_TRADE`, conflict detection and uncertainty.

### 5. Risk & Drawdown Governor
Independent authority that determines whether an opportunity may be expressed and at what exposure. Stateful modes: NORMAL / CAUTION / DEFENSIVE / PROTECTION / HALT. It owns portfolio-level limits and can veto every strategy.

### 6. Execution & Trade Management
Transforms approved intent into orders using realistic venue rules. Handles idempotency, duplicate prevention, fills, partials, stop/target logic, state reconciliation and later adapter-specific behavior.

### 7. Portfolio State
Canonical positions, exposure, realized/unrealized P&L, drawdown, risk utilization and execution health.

### 8. Telemetry & Failure Memory
Records decisions including rejected/no-trade opportunities, trade lifecycle, MAE/MFE, context, execution quality and post-mortem tags.

### 9. Research/Validation Plane
Experiment registry, deterministic backtests, walk-forward/OOS, Monte Carlo, adversarial stress, parameter sensitivity, failure clustering and promotion gates.

## NautilusTrader boundary
Audit NautilusTrader for event engine/message bus, cache/state, portfolio, order/execution abstractions, simulation/backtesting and adapters. Prefer its proven infrastructure when fit-for-purpose. Keep Project X's proprietary intelligence, research hypotheses, failure memory and risk policy separable so the project is not locked to one framework.

## Integration rules
- TradingView MCP is context/visualization/data tooling only after reliability audit; never silently treat chart UI data as an authoritative execution feed.
- MT5 may become an execution adapter/replication target; strategy research must not depend on MQL-specific behavior.
- Vibe/multi-agent components are hypothesis/orchestration resources, not an authority over deterministic tests.
- All interfaces should be typed/versioned where practical.
