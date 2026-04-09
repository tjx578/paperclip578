---
name: v72-structure-liquidity
description: Technical structure mapping, liquidity analysis, and entry geometry computation
---

Provide L10-L11 layer analysis covering market structure, liquidity zones, and precision entry geometry.

## Layer Responsibilities

### L10 — Structure Mapping

- Swing high/low identification (H4, H1)
- Order block detection and classification
- Fair value gap (FVG) mapping
- Break of structure (BOS) and change of character (CHoCH) detection
- Premium/discount zone calculation

### L11 — Liquidity Analysis

- Equal highs/lows identification (liquidity targets)
- Stop-loss cluster estimation
- Session sweep analysis (Asia, London, NY)
- Institutional order flow inference
- Liquidity void mapping

## Entry Geometry Output

For each viable entry zone:

1. Entry price range (zone, not point)
2. Invalidation level (structure break)
3. Nearest liquidity target
4. Session timing preference
5. Confluence count within the zone

## Rules

- Structure analysis must respect MTA hierarchy (D1 structure > H4 structure > H1 structure)
- Liquidity analysis requires minimum 2 session sweeps for confirmation
- Entry geometry is advisory — WOLF risk gate makes the final pass/veto
- Never produce entry geometry without V7.0 flow context and V6.0 macro alignment
