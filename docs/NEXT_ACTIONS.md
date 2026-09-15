# Next Actions

## Active phase: Phase 1 — Forensic Component Audit

Execute autonomously in this order:

1. Audit upstream NautilusTrader architecture and current version relevant to Project X. Identify exact modules/interfaces for event processing, data/state/cache, backtesting/simulation, portfolio/risk, execution/order model and adapters. Record license/dependency implications. Do not copy the repository wholesale.
2. Locate/audit the Vibe-Trading resources available to the workspace. Identify genuinely useful agents/engines/orchestration. If source is unavailable, document that fact instead of guessing.
3. Audit TradingView MCP implementations/resources, including their actual read/write/chart capabilities and reliability limits. Separate visualization/context from execution-grade data.
4. Inventory relevant existing MT5/EA assets if available to the workspace. Preserve them; extract execution lessons and benchmarks without inheriting strategy logic.
5. Produce a proposed `REUSE / MODIFY / REJECT / BUILD NEW` matrix.
6. Define the minimum clean Project X core needed for Phase 2.
7. Update all source-of-truth docs and commit a Phase 1 checkpoint.

Do not begin live execution. Do not request credentials.
