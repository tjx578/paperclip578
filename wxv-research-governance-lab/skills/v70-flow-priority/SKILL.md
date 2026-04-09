---
name: v70-flow-priority
description: Cross-asset flow analysis, pair priority ranking, and correlation context
---

Provide L1-L2 layer analysis covering pair priority, institutional flow, and cross-asset correlation.

## Layer Responsibilities

### L1 — Flow Context (shared with V6.0 macro)

- Institutional positioning signals (COT, dealer flow)
- Cross-asset correlation matrix (DXY, yields, equities vs FX)
- Risk sentiment classification (risk-on / risk-off / neutral)
- Intermarket divergence detection

### L2 — Pair Priority

- Weekly pair ranking by tradability score
- Volume and spread analysis per session
- Pair correlation groups (avoid doubling exposure)
- Seasonal and calendar effects

## Priority Output

Weekly pair priority matrix:

| Rank | Pair | Direction Bias | Flow Score | Best Session | Correlation Group |
|------|------|---------------|------------|--------------|-------------------|
| 1 | ... | ... | ... | ... | ... |

## Rules

- Pair priority must be published before weekly plan finalization
- Maximum 6 active pairs per week (focus over breadth)
- Correlated pairs count as single exposure (e.g., EURUSD + GBPUSD)
- Flow context must be updated at least once per session (Asia, London, NY)
- Never recommend pairs with spread > 3 pips during target session
