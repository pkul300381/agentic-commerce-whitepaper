# 03. Game-Theory Model

## 3.1 Strategic setting

We model agentic commerce as a repeated non-cooperative game among three agent populations:

- U: user agents
- M: merchant agents
- B: bank/payment agents

At each round t = 1..T, each agent chooses an action from its strategy space.

- user action: a_u(t) in A_u
- merchant action: a_m(t) in A_m
- bank action: a_b(t) in A_b

Actions include offer generation, counter-offer policy, identity proof level, payment rail selection, and settlement timing.

## 3.2 Assumptions

We make explicit assumptions to ground economic claims:

1. Bounded rationality: agents learn online and are not globally optimal each round.
2. Asymmetric information: willingness-to-pay, marginal cost, and risk model internals are private.
3. Feasibility constraints: latency, solvency, and compliance constraints must hold.
4. Rail optionality: agents can choose fiat rails or tokenized rails with different costs and finality.

This is a repeated Bayesian game with protocol constraints.

## 3.3 Stage payoff definitions

For one transaction opportunity:

User payoff

    U = value_of_match - price - delay_cost - data_exposure_cost - execution_failure_cost

Merchant payoff

    P = price - production_cost - payment_fee - inventory_risk_cost - chargeback_risk_cost

Bank/payment payoff

    B = fee_revenue - capital_cost - default_risk_cost - compliance_penalty_cost

A transaction occurs when all participating agents satisfy participation and feasibility conditions.

## 3.4 Negotiation game

We represent negotiation as a finite alternating-offer game.

1. Merchant proposes offer o1 = (price, terms).
2. User accepts, rejects, or counters with o2.
3. Bank/payment agent can reprice, approve, or veto based on risk and policy.

Acceptance requires:

- user payoff at accepted offer >= user reservation payoff
- merchant payoff at accepted offer >= merchant reservation payoff
- bank risk and compliance checks pass

## 3.5 Nash equilibrium condition

Let s = (s_u, s_m, s_b) be a strategy profile and J_n be expected utility for role n.

A Nash equilibrium s* satisfies:

    For each role n in {u, m, b}:
    J_n(s*_n, s*_-n) >= J_n(s_n, s*_-n) for all feasible deviations s_n.

Operational interpretation:

- users stop searching when expected surplus gain is below search cost,
- merchants stop discounting when marginal conversion gain equals margin loss,
- banks stop relaxing constraints when incremental fee gain equals tail-risk increase.

## 3.6 Mechanism-design layer

Protocol designers choose parameters theta (fees, rebates, staking rules, dispute windows, trust weights) to maximize social objective W(theta):

    W(theta) = sum(user payoffs) + sum(merchant payoffs) + sum(bank payoffs)

subject to:

- incentive compatibility,
- individual rationality,
- risk-budget sustainability,
- regulatory admissibility.

Therefore, market quality is a design problem, not only an inference problem.

## 3.7 Repeated-game and reputation effects

Let R_n(t) be reputation state for role n at time t.

Cooperation is sustainable when the discounted expected future penalty from defection exceeds short-term gain.

Practical implication: verifiable logs, portable reputation, and transparent policy enforcement increase long-run cooperation and lower equilibrium friction.

## 3.8 Why this matters to industry

For fintech operators and CTOs, equilibrium thinking changes implementation priorities:

- optimize protocol incentives, not just model accuracy,
- monitor equilibrium KPIs (spread, latency, finality, risk-adjusted conversion),
- treat governance controls as payoff-shaping infrastructure.

For regulators, the model supports ex-ante and ongoing stress tests of strategic failure modes.
