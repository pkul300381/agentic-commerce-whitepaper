# 02. Agentic Commerce

## 2.1 System actors

Agentic commerce markets are composed of interoperating software agents with distinct objectives.

- User agent (UA): selects products and terms that maximize user utility.
- Merchant agent (MA): optimizes margin, conversion quality, and inventory outcomes.
- Bank/payment agent (BA): optimizes routing, risk-adjusted revenue, and compliance outcomes.

These agents are strategic, adaptive, and often trained on different data. Their interaction is therefore economic as much as computational.

## 2.2 Transaction lifecycle

A canonical transaction includes six stages:

1. Discovery: UA gathers offers from multiple MA endpoints.
2. Qualification: UA and BA establish identity and trust level.
3. Negotiation: UA and MA exchange offers on price and terms.
4. Authorization: BA prices risk and approves payment path.
5. Settlement: value is transferred on selected rails.
6. Post-trade: fulfillment, disputes, rewards, and reputation updates.

Each stage introduces strategic choices and constraints that affect final outcomes.

## 2.3 Protocol primitives

A robust agentic protocol exposes machine-readable primitives:

- Offer object: price, quantity, delivery SLA, refund policy, expiry.
- Proof object: identity, compliance attestations, risk flags.
- Payment object: rail, fee schedule, finality profile, FX terms.
- Governance object: dispute process, penalty rules, upgrade policy.

Without standardized primitives, agents optimize locally and create ecosystem-level inefficiency.

## 2.4 Tokenized and programmable transactions

Tokenization enables conditional and composable transaction logic:

- Conditional release (deliver-vs-pay, milestone escrow).
- Programmable incentives (rebates, loyalty, staking-backed guarantees).
- Real-time policy enforcement (geography, risk tier, merchant category).

The key is not tokenization alone, but tokenization linked to explicit incentive design.

## 2.5 Success metrics for agentic markets

Enterprises should track protocol-level metrics, not only model metrics:

- Negotiation acceptance rate
- Median time-to-agreement
- Payment success and fallback rates
- Settlement finality time
- Fraud loss and dispute frequency
- Risk-adjusted contribution margin

These metrics form the bridge between strategic theory and operating performance.
