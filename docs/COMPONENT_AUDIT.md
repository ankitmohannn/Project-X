# Component Audit

Do not merge components before completing this record.

| Component | Source/version | Role | Evidence | Risks/debt | License | Integration cost | Decision | Notes |
|---|---|---|---|---|---|---|---|---|
| NautilusTrader | upstream audit pending | infrastructure | pending | pending | verify | pending | AUDIT | event/sim/portfolio/execution first |
| TradingView MCP | implementations pending | context/chart integration | pending | pending | verify | pending | AUDIT | audit reliability and exact capabilities |
| Vibe-Trading components | source to locate/audit | agent/research | pending | pending | verify | pending | AUDIT | reuse engines, not assumptions |
| Existing MT5/EAs | existing project assets | execution/benchmarks | historical only | strategy fragility/implementation coupling | internal/varies | pending | AUDIT | isolate from new core |

## Decision meanings
- **REUSE** — strong fit with evidence; integrate with minimal change.
- **MODIFY** — useful core but requires bounded changes.
- **REJECT** — risk/debt/weak evidence outweighs value.
- **BUILD NEW** — missing capability or existing alternatives are unsuitable.

## Audit questions
1. What exact problem does it solve?
2. Is it infrastructure or alpha/decision logic?
3. What tests/evidence support it?
4. Does it introduce lookahead, repainting, hidden state or unrealistic execution?
5. Is behavior deterministic/reproducible?
6. How does it fail?
7. What maintenance/dependency/license cost does it add?
8. Can it be replaced without rewriting Project X?
9. Does it improve robustness or only convenience?
10. Final decision and evidence.
