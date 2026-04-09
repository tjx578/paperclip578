---
name: feed-integrity
description: Market data feed validation ensuring clean, timely, and trustworthy data enters the analysis pipeline
---

Validate market data feeds before they enter the analysis pipeline.

## Checks

1. **Freshness** — Feed data is current and within acceptable latency
2. **Completeness** — All required instruments and timeframes are present
3. **Consistency** — OHLCV data is internally consistent (no impossible candles)
4. **Anomaly detection** — Flag unusual gaps, spikes, or missing periods
5. **Source verification** — Data comes from an expected provider

## Status Levels

- **Healthy** — All checks pass. Proceed with analysis.
- **Degraded** — Some checks have warnings. Proceed with reduced confidence flagged to analysts.
- **Failed** — Critical checks fail. Halt the pipeline for this instrument and report to HYBRID.

## Output

- Feed status report per instrument per timeframe
- Timestamp of last validated data point
- Any anomalies or warnings
- Readiness confirmation for session window
