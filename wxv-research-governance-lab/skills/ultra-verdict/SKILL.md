---
name: ultra-verdict
description: Final constitutional verdict authority — EXECUTE_BUY, EXECUTE_SELL, HOLD, or NO_TRADE at L12
---

Issue the final constitutional verdict at Layer 12 after all governance and risk packets are complete.

## Verdict Options

- **EXECUTE_BUY** — All gates passed, thesis is bullish, governance approved
- **EXECUTE_SELL** — All gates passed, thesis is bearish, governance approved
- **HOLD** — Existing position maintained, no new action required
- **NO_TRADE** — Conditions unclear or gates failed; correct output is inaction

## Prerequisites

Before issuing any verdict:

1. Governance packet from PROTOKOL must be complete
2. Risk gate from WOLF must show PASS (VETO = automatic NO_TRADE)
3. All 9 constitutional gates must be satisfied
4. Weekly plan must be active and approved

## Rules

- Board approval required for initial strategy and any strategy change
- WOLF veto is absolute and cannot be overridden
- Verdict must reference the specific thesis, session window, and gate results
- NO_TRADE is always a valid and respectable output
