---
name: wolf-ultra-precision-mta
description: Ultra-precision multi-timeframe analysis with strict quantitative confirmation gates
---

Extension of wolf-mta-topdown adding quantitative precision gates to each timeframe layer.

## Precision Gates

| Timeframe | Gate | Threshold |
|-----------|------|-----------|
| MN | Trend score | 60+ for valid bias |
| W1 | Structure clarity | Clear swing H/L required |
| D1 | Trend alignment | Must match W1 direction |
| H4 | Body close | Full candle close required |
| H1 | Confluence count | Minimum 3 confluences |

## Confluence Requirements (H1 Entry)

At least 3 of the following must align:

1. Order block or FVG in discount/premium zone
2. Liquidity sweep confirmed
3. Session timing (London/NY overlap preferred)
4. RSI divergence or momentum shift
5. Volume spike or institutional flow signal

## Rules

- No "close enough" — thresholds are hard boundaries
- Precision gates are validated by QRCE before final submission
- Failed precision gates produce VETO with specific gate ID
- All agents sharing this skill must use identical parameters
