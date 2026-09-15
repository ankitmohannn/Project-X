# Agent Blueprint

Agents are modular research specialists. They do not directly place live orders.

## Initial roles
- **Regime Agent** — trend/range/transition and uncertainty.
- **Structure Agent** — swing/internal structure hypotheses without repainting/lookahead.
- **Liquidity Agent** — sweep/liquidity-location hypotheses.
- **Momentum Agent** — continuation/exhaustion evidence.
- **Volatility Agent** — compression/expansion and abnormal volatility.
- **Session Agent** — London/NY/other session behavior based on data.
- **MTF Context Agent** — cross-timeframe state without duplicating signals.
- **Mean-Reversion Agent** — conditional reversion hypotheses.
- **Risk Agent** — opportunity risk characteristics; advisory to Governor.
- **Drawdown Governor** — independent permission/exposure authority.
- **Execution Agent** — order-model/execution-quality analysis; no autonomous live activation.
- **Failure Analyst** — cluster losses and state/execution failures.
- **Adversarial Validator** — actively tries to break promoted hypotheses.

## Contract
Each research agent returns structured: `hypothesis`, `inputs`, `state`, `evidence`, `confidence`, `invalidation`, `uncertainty`, `experiment_id`. Confidence must be calibrated by evidence and must not itself determine exposure.

Create/merge/remove roles when tests show redundancy or missing capability. Avoid agent count as a goal; fewer independent useful agents are better than many correlated opinions.
