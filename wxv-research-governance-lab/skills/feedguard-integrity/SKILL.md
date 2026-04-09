---
name: feedguard-integrity
description: Data feed freshness monitoring, completeness validation, and integrity scoring
---

Monitor and validate all data feeds entering the research pipeline.

## Feed Categories

| Category | Sources | Freshness SLA |
|----------|---------|---------------|
| Price data | Broker API, backup feed | < 5 seconds |
| Economic calendar | ForexFactory, Investing.com | Daily refresh |
| COT / positioning | CFTC, broker sentiment | Weekly (Friday) |
| News / geopolitical | RSS feeds, news API | < 15 minutes |
| Cross-asset | Yields, VIX, DXY | < 30 seconds |

## Validation Checks

1. **Freshness** — Data within SLA window
2. **Completeness** — All required fields present
3. **Consistency** — No contradictory values across sources
4. **Range** — Values within plausible bounds (spike detection)
5. **Source diversity** — Minimum 2 independent sources for critical data

## Output States

- **DATA_OK** — All feeds nominal; pipeline may proceed
- **DEGRADED** — Some feeds stale or incomplete; pipeline proceeds with warning
- **BLOCKED** — Critical feed failure; pipeline must halt until resolved

## REST Endpoints

- `POST /webhooks/feedguard/check` — Trigger integrity check
- `GET /webhooks/feedguard/status` — Current feed status summary

## Redis Namespaces

- Read: `feed:raw:*`, `feed:meta:*`
- Write: `feedguard:status:*`, `feedguard:alert:*`

## Rules

- FEEDGUARD never interprets data — only validates integrity
- BLOCKED status requires PROTOKOL notification within 60 seconds
- Feed status is checked before every pipeline run
- Historical feed quality is logged for MEMVAULT archival
