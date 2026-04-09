---
name: wolf-mta-topdown
description: Top-down multi-timeframe analysis hierarchy enforcement — Monthly → Weekly → Daily → H4 → H1
---

Enforce the MTA (Multi-Timeframe Analysis) top-down hierarchy for all research output.

## Hierarchy

1. **Monthly (MN)** — Macro bias and trend direction
2. **Weekly (W1)** — Swing structure and key levels
3. **Daily (D1)** — Active trend and session bias
4. **H4** — Trigger timeframe for entry validation
5. **H1** — Precision entry and confirmation

## Rules

- Analysis must flow strictly top-down: higher timeframe sets the context, lower timeframe confirms
- No H1 trigger is valid without H4 body-close validation
- No H4 setup is valid without D1 trend alignment
- Conflicting timeframes must be flagged — no averaging or blending
- Each timeframe layer has one owner agent (see pipeline L-numbers)

## Validation

- WOLF validates MTA hierarchy compliance before PASS/VETO
- QRCE validates that no agent skipped a timeframe layer
- Hierarchy violations are automatic VETO triggers
