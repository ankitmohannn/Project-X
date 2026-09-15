# Validation Framework

## Objective
Reject fragile ideas early. Performance is credible only when data, assumptions and execution are credible.

## Minimum validation stack
1. Data-quality and leakage/lookahead checks.
2. Deterministic baseline backtest with recorded costs.
3. In-sample vs out-of-sample separation appropriate to the hypothesis.
4. Walk-forward analysis.
5. Parameter perturbation/sensitivity; avoid single-point optimum dependence.
6. Spread/slippage/commission stress.
7. Latency/order-fill stress where relevant.
8. Session and regime segmentation.
9. Trend/range/transition behavior.
10. Monte Carlo/resampling where statistically appropriate.
11. MAE/MFE and tail-loss analysis.
12. Failure clustering and consecutive-loss/drawdown path analysis.
13. Paper/forward validation before live review.

## Metrics
Record at minimum: net return/P&L, max drawdown and duration, profit factor, expectancy, win rate, payoff ratio, trade count, exposure/time-in-market, average/median trade, tail losses, consecutive losses, costs as share of gross edge, MAE/MFE and regime/session breakdown. Add Sharpe/Sortino/calmar-like metrics only when their assumptions are appropriate.

## Anti-overfit rules
- Never select a strategy solely by maximum return/PF/win rate.
- Never hide rejected parameter sets or failed regimes.
- Do not tune on the final holdout.
- Any rule added after observing a failure becomes a new experiment and requires revalidation.
- Prefer broad stable parameter regions over sharp optima.
- A small sample cannot be rescued by attractive metrics.

## Promotion
Every experiment ends `PROMOTE`, `RESEARCH`, or `REJECT` with rationale. Promotion means eligible for the next validation stage, not permission for live money.
