# Risk & Drawdown Governor Plan

The Governor is independent of strategy agents and has final veto authority.

## Proposed states
`NORMAL -> CAUTION -> DEFENSIVE -> PROTECTION -> HALT`

Exact transition thresholds must be researched and validated; do not invent permanent percentages at bootstrap.

## Inputs
Equity/drawdown path, realized/unrealized risk, recent expectancy, loss clustering, strategy/regime confidence, open exposure, correlated exposure, volatility, spread/liquidity/execution quality, model/data health and abnormal behavior flags.

## Possible actions
Allow; reduce risk; reduce concurrent exposure; raise opportunity-quality threshold; disable a failing strategy/regime; tighten daily/rolling risk budget; flatten in explicitly tested emergency conditions; halt new entries; require human review before recovery from critical states.

## Requirements
- State transitions are deterministic and logged.
- Recovery/hysteresis is designed to avoid rapid risk-mode flipping.
- Governor behavior is tested against both real losing periods and synthetic/adversarial sequences.
- Strategy confidence cannot override portfolio safety.
- Risk sizing must use actual instrument/venue contract specifications when execution integration begins.
- Avoid martingale, uncontrolled averaging, or exposure escalation intended only to recover losses.

## Research question
The Governor should answer: **Given current evidence and portfolio state, how much risk—if any—is justified now?**
