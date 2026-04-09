---
name: protokol-governance
description: Governance completeness verification, board-ready packet assembly, and publish readiness control
---

Verify constitutional completeness and assemble the board-ready approval packet.

## Packet Requirements

Every approval packet must contain:

1. Thesis summary with directional bias and pair
2. Risk score (Wolf Points normalized)
3. All 9 constitutional gate results (pass/fail with evidence)
4. WOLF risk gate output (PASS/VETO)
5. QRCE compliance status (if triggered)
6. Operating plan reference from the active weekly plan
7. Journal entry reference from MEMVAULT
8. Session window and timestamp
9. PROTOKOL sign-off status

## Verification Rules

- Verify the complete traceability chain: feed integrity → analysis → scoring → constitutional gates → compliance → operating plan → journal
- If any link is missing or inconsistent, reject and request rerun
- Audit is mandatory even on NO_TRADE sessions
- Analysis-layer sizing claims must never pass as final authority
- Rejected packets return to HYBRID with specific remediation requirements
