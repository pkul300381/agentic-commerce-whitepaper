# 06. Risks and Governance

## 6.1 Strategic and technical risks

Agentic markets introduce concentrated strategic risks:

- collusion among merchant agents,
- adversarial prompt or policy manipulation,
- information asymmetry exploitation,
- reputation gaming and sybil behavior,
- cascading failures across payment rails.

These are equilibrium risks, not isolated model bugs.

## 6.2 Regulatory and policy risks

Core obligations include:

- AML/KYC and sanctions controls,
- consumer disclosure and recourse rights,
- fair-lending and anti-discrimination standards,
- data governance and cross-border transfer compliance,
- model accountability and auditability.

If these controls are external to protocol logic, enforcement cost and failure probability rise.

## 6.3 Governance architecture

A production-grade governance stack should include:

1. Policy-as-code constraints enforced at decision time.
2. Real-time risk scoring with hard stop thresholds.
3. Immutable or tamper-evident decision logs.
4. Tiered intervention rights (automated, operator, regulator).
5. Versioned upgrade and rollback mechanisms.

## 6.4 Incentive-compatible controls

Governance should modify payoffs directly:

- staking or bonding to deter abuse,
- slashing or penalty functions for verified misconduct,
- reputation decay for unresolved disputes,
- rewards for compliant and reliable behavior.

When controls alter expected utility, they become strategically effective.

## 6.5 Monitoring and stress testing

Recommended control metrics:

- anomaly rate in negotiation trajectories,
- concentration of counterparties and rail dependency,
- fraud-loss tail percentiles,
- dispute resolution time and reversal frequency,
- protocol rule-breach frequency by jurisdiction.

Stress tests should simulate strategic attacks, liquidity shocks, and policy changes to validate that equilibria remain stable.

## 6.6 Governance principle

The design objective is not maximum automation; it is bounded autonomy with accountable escalation. Durable adoption requires systems that are explainable, testable, and governable by design.
