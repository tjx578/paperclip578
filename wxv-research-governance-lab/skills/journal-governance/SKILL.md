---
name: journal-governance
description: Immutable trade journal management following WOLF_JOURNAL_SYSTEM_v3.2 — append-only, no edits, no deletions
---

Manage the immutable trade journal following the WOLF_JOURNAL_SYSTEM_v3.2 framework.

## Journal Rules

- **Append-only.** No edits, no deletions.
- **Every session must produce a journal entry.** This is mandatory per operating cadence.
- **Entry completeness required.** Each entry must include: thesis summary, risk score, all 9 gate results, operating context, session window, and timestamp.
- **Unique reference ID** assigned to every entry.
- **Integrity verification** on demand for audits.

## Entry Format

Each journal entry must contain:
1. Session date and window (Asia/London/NY)
2. Instruments analyzed
3. Trade thesis summary
4. Normalized risk score (Wolf Points)
5. Constitutional gate results (9/9 summary)
6. QRCE compliance status
7. Operating plan reference
8. PROTOKOL sign-off status
9. Outcome (if applicable, added in review)

## Custody

- MEMVAULT is the custodian
- PROTOKOL is the governance owner
- Custody confirmation receipts include entry ID, timestamp, and integrity hash
