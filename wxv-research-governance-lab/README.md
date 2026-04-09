# WXV Technologies Research & Governance Lab

An FX research governance control plane built on the [Agent Companies](https://docs.paperclip.dev/companies) specification.

## Goal

Produce audited, risk-scored FX trade theses with full traceability, strict 9-gate constitutional checks, and zero unauthorized live execution. Every session must generate a board-ready approval packet signed off by PROTOKOL before any verdict is published.

## Org Chart

```text
ULTRA (CEO)
├── HYBRID (COO — Weekly Operations)
│   ├── FEEDGUARD (Data Integrity Lead)
│   └── V8.0 (Lead Research Analyst)
│       ├── V7.4 (Senior Analyst — Arsenal)
│       ├── V7.2 (Analyst — SMC Precision)
│       ├── V7.0 (Analyst — Core Backbone)
│       └── V6.0 (Analyst — Baseline)
├── WOLF (Chief Risk Officer)
│   └── QRCE (Quality & Compliance Engine)
└── PROTOKOL (Chief Governance Officer)
    └── MEMVAULT (Journal Custody)
```

## Teams

| Team | Manager | Members |
| ------ | --------- | --------- |
| Research & Analysis | V8.0 | V7.4, V7.2, V7.0, V6.0 |
| Risk & Constitutional | WOLF | QRCE |
| Governance & Records | PROTOKOL | MEMVAULT |

## Pipeline (15 Layers)

1. Feed Integrity Verification (FEEDGUARD)
2. MN Timeframe Scan (Research Team)
3. W1 Timeframe Analysis (Research Team)
4. D1 Decision Gate — mandatory (Research Team)
5. H4 Body Close Confirmation — mandatory (Research Team)
6. H1 Entry Precision (Research Team)
7. Multi-Version Synthesis (V8.0)
8. Wolf Arsenal Overlay (V7.4, V8.0)
9. Unified L4–L8 Scoring — 30 Wolf Points (WOLF)
10. Constitutional Gate Sweep — 9 gates (WOLF, QRCE)
11. Risk Assessment & Stop-Loss Validation (WOLF)
12. Operating Plan Clearance (HYBRID)
13. Strategic Oversight Review (ULTRA)
14. Journal Entry & Immutable Record (MEMVAULT)
15. Board-Ready Approval Packet & Sign-Off (PROTOKOL)

## 9 Constitutional Gates

1. **Feed Integrity** — All data sources verified fresh and consistent
2. **MTA Completeness** — All required timeframes analyzed
3. **D1 Decision Gate** — Daily chart must confirm or deny before proceeding
4. **H4 Body Close** — H4 candle body close required (no wick-only signals)
5. **Scoring Normalization** — All scores normalized to 30-point Wolf scale
6. **No Competing Scores** — No conflicting trade theses active simultaneously
7. **Stop-Loss Defined** — Every thesis must have a defined stop-loss level
8. **No-Trade Zone Check** — High-impact news and illiquid periods excluded
9. **Trend Alignment** — Higher timeframe trend must align with entry direction

## Session Windows

| Session | Time (SGT) | Frequency |
| --------- | ------------ | ----------- |
| Weekly Planning | Sunday 8 PM | Weekly |
| Asia Confirmation | 10 AM | Weekdays |
| Trade Journal | 10 PM | Weekdays |
| Weekly Review | Friday 6 PM | Weekly |

## External Dependencies

- **Tuyul Kartel Wolf Arsenal API v4.0** — Capability plane for advanced technical analysis. Requires `WOLF_ARSENAL_API_KEY` (X-API-Key auth).

## Getting Started

```sh
# Import into a running Paperclip instance
paperclipai company import --from wxv-research-governance-lab

# Or specify a remote Paperclip server
paperclipai company import --from wxv-research-governance-lab --server http://localhost:3100
```

## Budget

Monthly budget: **$150** (15,000 cents)

## License

MIT — Copyright TJX
