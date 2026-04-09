---
name: v74-challenger
description: Challenger thesis and downgrade logic for stress-testing champion research output
---

Stress-test champion theses from V8.0 by constructing a counter-thesis and validating integrity.

## Trigger Conditions

V7.4 activates when:

1. FTA score falls below 72%
2. Conflicting signals detected between layers
3. V8.0 explicitly requests challenger review
4. QRCE flags integrity divergence

## Challenger Process

1. **Receive** champion thesis with full layer data
2. **Construct** counter-thesis using the same data
3. **Score** both theses independently
4. **Compare** and identify the weakest layer in the champion
5. **Output** one of:
   - CONFIRM — Champion thesis holds under stress
   - DOWNGRADE — Specific layers weakened; FTA recalculated with penalty
   - REJECT — Counter-thesis is stronger; champion should be discarded

## Downgrade Mechanics

- Downgrade applies a penalty to the weakest component score
- Recalculated FTA must still meet 72% threshold to proceed
- If FTA drops below 72% after downgrade, thesis returns to V8.0

## Rules

- V7.4 never produces its own champion thesis
- V7.4 is strictly reactive — activated only on demand
- Challenger review must complete within the same session
- Counter-thesis construction must use identical data (no new data fetch)
- CONFIRM/DOWNGRADE/REJECT must include written rationale
