---
name: wolf-arsenal-toolkit
description: Wolf Arsenal capability plane providing the indicator and computation toolkit for FX multi-timeframe analysis
---

Shared indicator and computation toolkit available to research agents (V8.0, V7.4, V7.2, V7.0) and governance agents (WOLF, QRCE).

## Arsenal Components

- Multi-timeframe trend indicators (EMA, SMA, RSI, ADX)
- Structure mapping tools (swing highs/lows, order blocks, FVG detection)
- Liquidity analysis (session sweeps, equal highs/lows, stop clusters)
- Flow context signals (institutional positioning, commitment of traders)
- Volatility regime classification
- Correlation matrix computation
- Session overlap timing engine

## Usage Rules

- Arsenal is a toolkit, not a decision-maker
- Agents consume arsenal outputs as inputs to their own layer logic
- Arsenal does not produce trade signals directly
- All outputs must be timestamped and session-tagged
- Indicator parameters are standardized across the pipeline (no per-agent tuning)

## Access Pattern

Research agents (V-series) read arsenal outputs for their layer analysis.
WOLF reads arsenal outputs only for risk-gate validation.
No agent may modify arsenal parameters without ULTRA approval.
