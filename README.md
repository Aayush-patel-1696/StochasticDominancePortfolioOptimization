# Stochastic Dominance Constraints

## Introduction

Stochastic Dominance (SD) is a key concept in decision-making under uncertainty, particularly in finance, economics, and risk management. It provides a framework for comparing probability distributions of uncertain outcomes, ensuring that one alternative is preferred over another according to rational decision-making criteria.

Stochastic Dominance Constraints (SDCs) are mathematical constraints incorporated into optimization models to enforce dominance relationships between random variables. These constraints are widely used in portfolio optimization, risk-sensitive decision-making.

## Project Description

This project focuses on optimizing investments in a set of securities with random return rates, while comparing the portfolio performance to a benchmark return rate (e.g., an index or existing portfolio). Our decision variables \( x \) represent the fraction of capital allocated to each security, and \( X \) is a polyhedral set defining investment constraints. The portfolio return rate is given by:

\[
R_p = \sum_{i} x_i R_i
\]

### Optimization Problem:

\[
\max_{x \in X} E[R_p]
\]

Subject to:

\[
P(R_p \geq R_b) \geq \alpha
\]

We have demonstrated that the constraint \( P(R_p \geq R_b) \geq \alpha \) is equivalent to:

\[
E[\max(0, R_b - R_p)] \leq \epsilon
\]

This project explores the integration of Stochastic Dominance Constraints into portfolio optimization, ensuring that investment decisions align with rational risk preferences.

## Types of Stochastic Dominance

### First-Order Stochastic Dominance (FSD)
Ensures that one distribution yields higher utility than another for all risk-averse decision-makers. Mathematically, for two cumulative distribution functions (CDFs) \( F_X \) and \( F_Y \), FSD holds if:

\[
F_X(t) \leq F_Y(t), \quad \forall t
\]

This implies that distribution \( X \) is preferred to \( Y \) for all non-decreasing utility functions.

### Second-Order Stochastic Dominance (SSD)
Accounts for risk aversion and ensures that one distribution is preferable for all risk-averse investors. Mathematically, SSD holds if:

\[
\int_{-\infty}^{t} F_X(s) ds \leq \int_{-\infty}^{t} F_Y(s) ds, \quad \forall t
\]

This ensures that \( X \) provides greater expected utility than \( Y \) for concave utility functions.

### Higher-Order Stochastic Dominance (HSD)
Extends the concept to third-order and beyond, considering additional risk preferences such as prudence and temperance.

## Stochastic Dominance Constraints in Optimization

SDCs are implemented in optimization problems to ensure that the chosen decision variables yield outcomes that are stochastically superior. These constraints typically appear in:

- **Portfolio Optimization**: Enforcing SD constraints ensures that an optimal portfolio dominates a benchmark portfolio in terms of risk-return trade-offs.
- **Risk-Aware Decision Making**: Ensures that selected strategies minimize downside risk and align with investor preferences.
- **Insurance and Risk Management**: Helps in selecting policies that offer better probabilistic guarantees against losses.

## Formulating Stochastic Dominance Constraints

In practical optimization models, SD constraints are often formulated using:

- **Linear Programming (LP)** for SSD by integrating over empirical CDFs.
- **Convex Optimization Methods**: Formulating SDCs as convex constraints where possible.

## Applications

- **Financial Portfolio Selection**: Ensuring that an investment portfolio stochastically dominates alternative portfolios.

## Conclusion

- **Risk Averse Preference**: By employing Second order Stochastic Dominace constraints all Risk Averese people will select the obtained portfolio compared to benchmark portfolio
