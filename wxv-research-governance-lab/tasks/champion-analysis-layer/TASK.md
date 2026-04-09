---
name: Champion Analysis Layer
assignee: v8-0
project: precision-alpha-engine
---

# Champion Analysis Layer

Build and validate the champion analysis pipeline (L3-L4, L7, L9) that produces validated alpha theses.

## Scope

1. Implement multi-timeframe structure analysis (L3) — MN → W1 → D1 → H4 → H1
2. Build key levels and liquidity mapping (L4) — order blocks, FVGs, session sweeps
3. Develop confluence and entry model (L7) — minimum 3 confluences required
4. Assemble champion thesis output (L9) — pair, direction, entry zone, invalidation, targets, RR, FTA score, confidence class
5. Integrate FTA runtime computation with standard weights (15/15/20/20/20/10)
6. Implement delegation logic to V7.2 (entry geometry), V7.0 (flow), V6.0 (macro), V7.4 (challenger)

## Quality Gates

- Only A+ and A setups proceed to WOLF risk gate
- B setups logged but not submitted
- FTA ≥ 72% required to proceed; FTA < 72% triggers V7.4 challenger review
- All delegated layer outputs must be received before thesis assembly
- MTA hierarchy strictly enforced (no timeframe skipping)

## Acceptance Criteria

- Champion thesis format fully specified and validated against schema
- FTA computation reproducible and independently verifiable by QRCE
- Delegation round-trips complete within session window
- Backtest shows thesis generation consistent with historical setups
