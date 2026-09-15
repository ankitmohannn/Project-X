# Experiment Ledger

Never delete failed experiments. Append or link detailed artifacts.

| ID | Date | Hypothesis | Market/TF | Data | Costs | Validation | Key metrics | Failure modes | Status |
|---|---|---|---|---|---|---|---|---|---|
| PX-BOOT-001 | bootstrap | Project infrastructure only | N/A | N/A | N/A | documentation audit | N/A | N/A | PROMOTE |

## Experiment template
### ID
`PX-<AREA>-<NNN>`

### Hypothesis
A falsifiable statement, not a strategy nickname.

### Setup
Data source/version/range; instrument; timeframe/event model; timezone/session; features/rules; parameters; order model; spread/slippage/commission/latency assumptions; random seeds if any.

### Results
All required metrics plus regime/session breakdown and artifacts.

### Robustness
OOS/walk-forward; perturbation; stress; Monte Carlo if appropriate; failure clusters.

### Decision
`PROMOTE / RESEARCH / REJECT` and why.
