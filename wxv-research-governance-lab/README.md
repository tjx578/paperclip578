# WXV Technologies Research & Governance Lab

An FX research governance control plane built on the [Agent Companies](https://docs.paperclip.dev/companies) specification.

## Goal

Produce audited, risk-scored FX trade theses with full traceability, strict 9-gate constitutional checks, and zero unauthorized live execution. Every session must generate a board-ready approval packet signed off by PROTOKOL before any verdict is published.

## Org Chart

```text
ULTRA (CEO / Constitutional Verdict Authority)
├── HYBRID (COO / Goal Steward — Weekly Planning & Session Coordination)
│   └── V8.0 (Head of Market Intelligence / Champion Research Engine)
│       ├── V7.4 (Senior Challenger Analyst — on-demand)
│       ├── V7.2 (Technical Structure & Liquidity Desk)
│       ├── V7.0 (Cross-Asset Flow & Relative Strength Desk)
│       └── V6.0 (Macro / Regime Baseline Desk)
└── PROTOKOL (Protocol Auditor / Governance PMO)
    ├── WOLF (Capital & Risk Governance — PASS/VETO gate)
    ├── QRCE (Model Risk & Conflict Validator — on-demand)
    ├── FEEDGUARD (Data Feed Integrity — external-http)
    └── MEMVAULT (Immutable Audit Custodian — external-http)
```

## Teams

| Team | Manager | Members |
| ------ | --------- | --------- |
| Research & Analysis | V8.0 | V7.4, V7.2, V7.0, V6.0 |
| Governance & Compliance | PROTOKOL | WOLF, QRCE, FEEDGUARD, MEMVAULT |

## Pipeline (15 Layers)

| Layer | Name | Primary Owner |
| ----- | ---- | ------------- |
| Pre-L1 | Data Feed Integrity | FEEDGUARD |
| L1 | Macro Context & Flow | V6.0, V7.0 |
| L2 | Pair Priority & Ranking | V7.0 |
| L3 | Multi-Timeframe Structure | V8.0 |
| L4 | Key Levels & Liquidity | V8.0 |
| L5 | Session Windows | HYBRID |
| L6 | Risk Gate (PASS / VETO) | WOLF |
| L7 | Confluence & Entry Model | V8.0 |
| L8 | Challenger Review & Conflict Validation | V7.4, QRCE |
| L9 | Champion Thesis Assembly | V8.0 |
| L10 | Structure Mapping (H4/H1) | V7.2 |
| L11 | Liquidity Analysis | V7.2 |
| L12 | Constitutional Verdict | ULTRA |
| L13 | Journal Commit | MEMVAULT |
| L14 | Governance Packet & Audit | PROTOKOL, MEMVAULT |
| L15 | Cross-Desk Synthesis & Planning | HYBRID |

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

Monthly budget: **$167** (16,700 cents)

| Agent | Budget/month |
| ----- | ------------ |
| ULTRA | $25 |
| PROTOKOL | $15 |
| HYBRID | $20 |
| WOLF | $14 |
| QRCE | $10 |
| FEEDGUARD | $9 |
| MEMVAULT | $8 |
| V8.0 | $20 |
| V7.4 | $12 |
| V7.2 | $12 |
| V7.0 | $12 |
| V6.0 | $10 |

## License

MIT — Copyright TJX
