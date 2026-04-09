---
name: wolf-journal-review
description: Trade journal review and lesson extraction for continuous pipeline improvement
---

Review completed trade journals and extract actionable lessons for pipeline refinement.

## Journal Entry Requirements

Each completed trade must include:

1. **Setup ID** — Unique identifier linking to the pipeline run
2. **Thesis Summary** — Original thesis from V8.0
3. **Layer Scores** — Per-layer confidence at time of execution
4. **Entry/Exit Details** — Price, time, session, slippage
5. **Outcome** — P&L, RR achieved, drawdown contribution
6. **Post-Mortem** — What worked, what failed, which layer was weakest

## Review Process

- MEMVAULT stores the immutable journal record
- PROTOKOL audits journal completeness
- V8.0 extracts pattern insights for future research
- WOLF reviews risk adherence in hindsight

## Lesson Categories

- **Process** — Hierarchy violation, timing error, skipped gate
- **Model** — Incorrect regime classification, structural misread
- **Execution** — Slippage, session timing, position sizing
- **Governance** — Override misuse, approval gap

## Rules

- Journals are immutable once committed to MEMVAULT
- Lessons must reference specific pipeline layer and gate
- No blame assignment to individual agents — focus on process improvement
