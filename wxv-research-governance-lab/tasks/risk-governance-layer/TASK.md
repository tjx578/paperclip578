---
name: Risk & Governance Layer
assignee: wolf
project: precision-alpha-engine
---

# Risk & Governance Layer

Build and validate the risk gate and governance enforcement layer (L6, L12) for the Precision Alpha Engine.

## Scope

### Risk Gate (WOLF — L6)

1. Implement PASS / VETO binary gate — no hidden third state
2. Enforce PropFirm compliance rules (drawdown limits, position limits)
3. Validate per-trade risk envelope (RR minimum 1:2)
4. Check correlation exposure limits
5. Verify weekly risk budget allocation
6. Enforce forbidden pair violations and no-trade zones

### Constitutional Verdict (ULTRA — L12)

1. Define constitutional verdict authority flow
2. Implement 3-option verdict: APPROVED, CONDITIONAL, NO-GO
3. Ensure verdict is final and sealed upon issuance

### Integrity Control (QRCE — L8)

1. Validate FTA computation (standard weights, all components present)
2. Detect inter-desk directional conflicts
3. Flag timeframe skips and data staleness
4. Escalate critical integrity issues to PROTOKOL

### Data Gate (FEEDGUARD — Pre-L1)

1. Implement DATA_OK / DEGRADED / BLOCKED feed status
2. Enforce feed freshness SLAs
3. Block pipeline on critical feed failure

## Acceptance Criteria

- WOLF VETO cannot be overridden by any agent
- Constitutional gates produce consistent results across backtest
- QRCE catches planted integrity violations in testing
- FEEDGUARD correctly blocks pipeline on simulated feed failure
