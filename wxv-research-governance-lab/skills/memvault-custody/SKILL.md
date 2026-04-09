---
name: memvault-custody
description: Immutable audit record custody, archival integrity, and retrieval services
---

Maintain the immutable archive of all pipeline decisions, trade journals, and governance records.

## Archive Categories

| Category | Retention | Immutability |
|----------|-----------|-------------|
| Trade journals | Indefinite | Write-once, no delete |
| Pipeline run logs | 90 days hot, indefinite cold | Write-once |
| Governance decisions | Indefinite | Write-once, no delete |
| Risk gate verdicts | Indefinite | Write-once, no delete |
| Feed integrity logs | 30 days hot, 1 year cold | Write-once |
| Weekly plans | Indefinite | Write-once |

## Custody Operations

- **Commit** — Accept a record, assign immutable ID, timestamp, and hash
- **Retrieve** — Fetch record by ID, category, date range, or agent
- **Verify** — Confirm record integrity (hash check)
- **Index** — Maintain searchable index across all categories

## REST Endpoints

- `POST /webhooks/memvault/commit` — Commit a new record
- `GET /webhooks/memvault/retrieve` — Retrieve records by query
- `GET /webhooks/memvault/verify/:id` — Verify record integrity

## Redis Namespaces

- Read: `memvault:index:*`, `memvault:meta:*`
- Write: `memvault:record:*`, `memvault:index:*`, `memvault:hash:*`

## Rules

- Records are write-once — no updates or deletes
- Every commit returns a content hash for verification
- PROTOKOL and ULTRA have read access to all categories
- Individual agents can only read their own submissions
- Bulk exports require ULTRA approval
- Storage integrity is self-audited daily
