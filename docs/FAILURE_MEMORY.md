# Failure Memory

Failures are evidence. Do not remove them because a later version performs better.

| Failure ID | Experiment/Trade | Market state | Session | Volatility | Spread/cost | Entry reason | Risk state | MAE/MFE | Exit/result | Root-cause tags | Action |
|---|---|---|---|---|---|---|---|---|---|---|---|

## Root-cause tag examples
`REGIME_MISMATCH`, `TRANSITION`, `FALSE_BREAK`, `LIQUIDITY_REVERSAL`, `MOMENTUM_DECAY`, `VOLATILITY_SHOCK`, `SPREAD_SPIKE`, `SLIPPAGE`, `SESSION_EDGE_DECAY`, `DATA_QUALITY`, `LOOKAHEAD_BUG`, `DUPLICATE_ORDER`, `STATE_DESYNC`, `OVERFIT`, `UNKNOWN`.

## Rule
A repeated failure cluster should trigger a research hypothesis, not an automatic filter. New filters/rules require a new experiment and full revalidation.
