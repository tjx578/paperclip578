---
name: Market Data & Context Layer
assignee: v6-0
project: precision-alpha-engine
---

# Market Data & Context Layer

Build and validate the market data and macro context layer (L1) that forms the foundation for all downstream analysis.

## Scope

1. Establish macro regime classification system (risk-on / risk-off / transitional / event-driven)
2. Integrate central bank calendar, economic data releases, and geopolitical risk signals
3. Build cross-asset correlation framework (DXY, yields, equities, commodities, VIX vs FX)
4. Define per-currency directional bias matrix (strong/moderate/neutral/bearish)
5. Validate data freshness and completeness via FEEDGUARD integration
6. Produce weekly macro brief as input to HYBRID weekly planning

## Integration Points

- **FEEDGUARD** — validates all data feeds before context layer runs (Pre-L1)
- **V7.0** — consumes macro regime output for pair priority and flow context
- **HYBRID** — receives weekly macro brief for master plan compilation
- **Wolf Arsenal API** — provides market data and ML prediction inputs

## Acceptance Criteria

- Regime classification produces consistent output across backtesting periods
- All data sources have defined freshness SLAs
- Macro brief format standardized and consumable by downstream agents
- No-trade event windows correctly identified and enforced
