# Integration Plan

## NautilusTrader
Upstream: https://github.com/nautechsystems/nautilus_trader

Audit before choosing integration method. Likely candidate responsibilities: event-driven runtime, simulation/backtesting, order/execution abstractions, portfolio/cache/state and adapters. Prefer dependency/submodule/reference over vendoring entire upstream source unless a documented technical reason exists.

## TradingView MCP
Reference implementations:
- https://github.com/atilaahmettaner/tradingview-mcp
- https://github.com/tradesdontlie/tradingview-mcp

Audit exact capabilities first. Desired role: live chart/context integration and visualization for S/R, bias, structure and other validated state. Do not assume MCP can provide execution-grade feed or persistent chart drawing until verified.

## Vibe-Trading / Agent Engines
Locate exact repository/version from workspace/user resources. Audit at component level. Candidate roles: research orchestration, specialist agents, confidence/evidence aggregation, experiment generation. Do not import unverified strategy logic.

## MT5
Later candidate execution/replication adapter. Requirements: deterministic intent mapping, symbol/contract normalization, spread/slippage handling, duplicate-order prevention, state reconciliation, VPS resilience and complete logs. Live route remains disabled until human approval.

## Integration rule
Every external system gets an adapter boundary. Project X core should remain testable when that external system is unavailable.
