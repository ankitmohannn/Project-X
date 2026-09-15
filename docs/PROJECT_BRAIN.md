# Project Brain

## Why Project X exists
Prior trading work produced useful ideas and some promising tests, but repeated experience showed that a strategy can look strong and later become fragile or suffer unacceptable drawdown. Project X therefore does **not** begin with the assumption that an old strategy only needs optimization.

The goal is a different system architecture that can understand market state, decide when not to trade, govern risk dynamically, test ideas adversarially and remember failures.

## Initial scope
- Primary research market: XAUUSD / Gold.
- Later portability: BTCUSD, crude oil, indices and other liquid markets.
- Development/research first. Live-money execution is outside autonomous authority.

## Existing ecosystem to leverage selectively
### TradingView MCP
Previously used for live chart context, multi-timeframe support/resistance, bias and market analysis. Project X should audit available MCP implementations and use them where they provide reliable market/chart context. Live-chart presentation is preferred for visual TradingView workflows; do not substitute Pine Script unless explicitly required.

Known reference repositories include:
- https://github.com/atilaahmettaner/tradingview-mcp
- https://github.com/tradesdontlie/tradingview-mcp

### Vibe-Trading / multi-agent work
Existing agent/research concepts may be valuable for hypothesis generation, confidence assessment, research orchestration and specialist analysis. Do not assume the entire stack is correct. Audit individual engines/agents and reuse only evidence-backed pieces.

### MT5 / EA ecosystem
Existing EAs and VPS execution experience are valuable for execution constraints, logs, realistic spread behavior and later replication. Existing bots are benchmarks/reference systems, not Project X's inherited alpha.

### NautilusTrader
Reference: https://github.com/nautechsystems/nautilus_trader

Audit it primarily as professional infrastructure: event-driven architecture, data/state/cache patterns, portfolio/risk/execution abstractions, backtesting/simulation and adapters. Prefer integration/dependency over copying the entire repository. NautilusTrader is infrastructure, not proof of trading edge.

## Historical research lessons
Prior tracks included EMA/UT-style systems, SMC liquidity/BOS/CHoCH, FVG/session ORB, ADX trend pullback, pseudo-hedge/basket approaches, SuperTrend/MACD/EMA confluence, momentum research and multi-timeframe EMA systems. Treat these as a library of hypotheses and failure lessons, not as defaults.

Historical benchmark examples (do not treat as verified current edge):
- A momentum M30 research candidate previously reached paper/live-paper metrics around PF 1.34 with controlled observed drawdown in that test phase.
- A prior H1 EMA21/EMA50/SMA150 candidate reported +32.11% return, PF 1.69, 41% win rate, ~12% max drawdown, 78 trades and walk-forward pass.

These benchmarks demonstrate why Project X must test persistence, sample size, regime dependence and execution sensitivity rather than inherit headline metrics.

## Core principles
1. Survival and controlled drawdown before maximum return.
2. Positive expectancy must survive realistic costs and regime change.
3. `NO TRADE` is a valid and important state.
4. Separate signal confidence from permitted exposure.
5. Risk Governor can veto any strategy/agent.
6. Failure memory is mandatory.
7. Research agents propose; deterministic validation decides.
8. Never optimize only for win rate or return.
9. No repainting/lookahead/data leakage.
10. No duplicate exposure caused by orchestration bugs.
11. Market/session/spread/volatility context must be measurable, not storytelling.

## Target system chain
`DATA -> MARKET STATE/REGIME -> SPECIALIST AGENTS -> OPPORTUNITY/CONFIDENCE -> RISK GOVERNOR -> EXECUTION -> TRADE MANAGEMENT -> PORTFOLIO STATE -> FAILURE ANALYSIS -> RESEARCH FEEDBACK`

## Failure memory fields
At minimum capture: experiment/trade ID, timestamp, instrument, timeframe, session, regime, volatility state, spread/cost assumptions, structure/liquidity/momentum context, entry rationale, confidence, risk state, MAE, MFE, exit reason, execution quality, result and post-mortem tags. Cluster repeated losing conditions.

## User workflow expectation
OpenCode/Luna should work autonomously inside this repository. Routine research/build/test/fix/document cycles should not require approval. Human checkpoints are for major architecture changes, credentials, destructive actions or real-money activation.
