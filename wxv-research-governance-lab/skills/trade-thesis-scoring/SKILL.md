---
name: trade-thesis-scoring
description: Canonical unified scoring (L4-L8) with 30 Wolf Points normalization — no competing final scores
---

Score trade theses using the canonical unified_core_l4_l8 scoring pipeline with 30 Wolf Points normalization.

## Scoring Rules

- **Canonical owner**: unified_core_l4_l8 pipeline
- **Normalization**: All sub-scores must be normalized to the 30 Wolf Point scale
- **No competing final scores**: There is one authoritative final score per thesis
- **Toolkit scores feed in**: Arsenal toolkit, SMC overlay, and other layer scores contribute to the unified score but do not compete with it

## Score Components

Scores aggregate across the 15-layer pipeline:
- Baseline structural assessment (V6.0)
- Core backbone analysis (V7.0)
- SMC precision overlay (V7.2)
- Arsenal toolkit depth (V7.4)
- Ultra precision MTA synthesis (V8.0)

## Output

- Final normalized score (0-30 Wolf Points)
- Component breakdown by layer
- Confidence level
- Score justification referencing specific timeframe assessments
