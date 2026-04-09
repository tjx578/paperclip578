---
name: wolf-fta-runtime
description: Final Trade Assessment runtime computation producing the go/no-go FTA score
---

Compute the Final Trade Assessment (FTA) score that determines whether a thesis proceeds to risk gate.

## FTA Score Components

| Component | Weight | Source Agent |
|-----------|--------|-------------|
| Macro regime alignment | 15% | V6.0 |
| Flow and pair priority | 15% | V7.0 |
| Structure and liquidity | 20% | V7.2 |
| MTA hierarchy compliance | 20% | V8.0 |
| Confluence count | 20% | V8.0 |
| Challenger adjustment | 10% | V7.4 |

## Thresholds

- **FTA ≥ 72%** — Proceeds to WOLF risk gate
- **FTA 60-71%** — Flagged for V7.4 challenger review
- **FTA < 60%** — Automatic rejection, no risk gate

## Special Cases

- If V7.4 challenger downgrades a thesis, FTA is recalculated with penalty
- FTA < 72% after challenger review triggers delegation back to V8.0 for revision or discard
- Emergency override by ULTRA can bypass FTA threshold (logged and audited)

## Rules

- FTA is computed by V8.0 as the pipeline aggregator
- All component scores must be present — no partial FTA
- FTA score is immutable once submitted to risk gate
- QRCE validates that FTA computation followed standard weights
