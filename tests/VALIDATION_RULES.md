# Test & Validation Rules

## Code
- Unit-test deterministic feature/state/risk logic.
- Integration-test event/state boundaries.
- Test idempotency and duplicate-order prevention.
- Test restart/reconciliation behavior before any execution integration.
- Keep regression fixtures for discovered bugs.

## Trading research
- Reproduce every promoted baseline from a clean run.
- Assert no future-bar access/lookahead.
- Verify session/timezone boundaries.
- Stress costs, spread, slippage and fills.
- Test missing/duplicate/out-of-order data behavior.
- Validate regime transitions and drawdown-state transitions.
- Compare expected order intent with simulated fills and portfolio state.

## Failure policy
A failed test is evidence. Fix root cause; do not weaken assertions without documenting why the original requirement was invalid.
