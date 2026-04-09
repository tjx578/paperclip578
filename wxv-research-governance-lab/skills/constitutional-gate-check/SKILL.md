---
name: constitutional-gate-check
description: 9-gate constitutional verification for trade theses — all gates must pass before a verdict can proceed
---

Perform the 9-gate constitutional check on a trade thesis. Every gate must pass. A single failure halts the pipeline.

## Gates

1. **Feed Integrity** — Data feeds validated by FEEDGUARD
2. **MTA Completeness** — All 5 timeframes (MN/W1/D1/H4/H1) analyzed top-down
3. **D1 Decision Gate** — D1 directional bias is clear and justified
4. **H4 Body Close** — H4 candle body close confirms intraday direction
5. **Scoring Normalization** — All scores use canonical unified_core_l4_l8 format
6. **No Competing Scores** — Single authoritative final score, no conflicts
7. **Stop-Loss Defined** — Thesis includes a mandatory stop-loss level
8. **No-Trade Zone Check** — If conditions are unclear, "no trade" is the correct output
9. **Trend Alignment** — Higher timeframe bias consistent with thesis direction

## Rules

- Gates are evaluated in order
- A gate failure produces a specific rejection with the gate number and reason
- No gate may be skipped or deferred
- The checker does not modify the thesis — it evaluates and reports
- Gate results are part of the approval packet sent to PROTOKOL
