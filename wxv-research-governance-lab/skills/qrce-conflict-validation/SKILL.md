---
name: qrce-conflict-validation
description: Inter-desk conflict detection, integrity divergence analysis, and FTA computation validation
---

Validate research pipeline integrity by detecting conflicts between desk outputs and verifying FTA computation.

## Conflict Detection

Scan for:

1. **Directional conflict** — Two desks disagree on bias for the same pair
2. **Timeframe skip** — Layer analysis missing an intermediate timeframe
3. **Data staleness** — Layer output older than current session
4. **Weight manipulation** — FTA component weights deviate from standard
5. **Hierarchy violation** — Lower timeframe overriding higher timeframe

## Integrity Divergence

Flag when:

- V6.0 macro says risk-off but V7.0 flow says risk-on
- V7.2 structure breaks but V8.0 thesis still bullish
- FTA score ≥ 72% but 2+ component scores below 50%
- Challenger (V7.4) DOWNGRADE ignored by V8.0

## FTA Validation

- Verify all 6 component scores are present
- Verify standard weights applied (15/15/20/20/20/10)
- Recalculate FTA independently and compare
- Flag any deviation > 1%

## Output

- **CLEAN** — No conflicts or divergences detected
- **FLAGGED** — Specific conflicts identified; includes list and severity
- **ESCALATE** — Critical integrity issue; pipeline must halt

## Rules

- QRCE is reactive only — activated on-demand or by pipeline trigger
- QRCE never produces trade theses or directional opinions
- QRCE findings go to PROTOKOL for governance action
- QRCE cannot override WOLF risk gate — separate domains
