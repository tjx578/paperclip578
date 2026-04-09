---
name: v60-macro-regime
description: Macro context analysis, event risk assessment, and regime baseline classification
---

Provide L1 macro context establishing the baseline regime for all downstream research.

## Regime Classifications

| Regime | Description | Trading Implication |
|--------|-------------|---------------------|
| Risk-On | Broad risk appetite, carry trades favored | Trade with momentum |
| Risk-Off | Flight to safety, JPY/CHF strength | Reduce exposure, defensive pairs |
| Transitional | Regime shift in progress | Reduce size, wait for confirmation |
| Event-Driven | High-impact data/CB decision imminent | Pre-position or stand aside |

## Macro Inputs

1. Central bank policy stance and calendar
2. Key economic data releases (NFP, CPI, GDP, PMI)
3. Geopolitical risk assessment
4. Cross-asset regime signals (yields, equities, commodities, VIX)
5. Seasonal patterns and end-of-month/quarter flows

## Output Format

Weekly macro brief:

1. **Current Regime** — Classification with confidence
2. **Key Events** — Calendar for the week with expected impact
3. **Bias Matrix** — Per-currency directional bias (strong/moderate/neutral/bearish)
4. **Risk Flags** — Events or conditions that could invalidate the regime
5. **Carry-Forward** — Unresolved macro themes from prior week

## Rules

- Regime classification must be published before weekly plan
- Regime changes mid-week require immediate notification to HYBRID
- Event risk windows (30 min before/after high-impact data) are no-trade by default
- Never forecast specific price levels — provide directional context only
- Macro analysis must be currency-pair agnostic (analyze currencies, not pairs)
