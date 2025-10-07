---
title: Probability
parent: Math for ML
---
* $Var(X) = E(X - E(X))^2 = E(X^2) - E(X)^2 = M2 - M1$ (moments)

- $Cov(X,Y) = E ((X −E(X))(Y −E(Y))) = E(XY)−E(X)E(Y)$
	- $Var(X) = Cov(X,X)$

* Standard Deviation = $\sqrt{Var(x)}$

- $P(A \cup B) = P (A) + P(B) - P(A \cap B)$

* Marginal distribution: $P(X = x) = \sum_y P(X = x, Y = y)$

- If A and B are independent events: $P(A \vert B) = P(A)$ and $P(A ∩ B) = P(A) . P(B)$
	- If A and B are independent: $Cov(A,B) = 0$

- $P(A \vert B) = {P(A \cap B) \over P(B)}$ or $P(A ∩ B) = P(A \vert B) . P(B) = P(B \vert A) . P(A)$

- Bayes' Formula:
	- $P(A \vert B) = P(B \vert A)P(A) / P(B)$

- A and B are *conditionally independent* if: $P((A ∩ B)/C) = P(A \vert C) . P(B \vert C)$

- Law of total probability
	- $P(A) = P(A \vert B1).P(B1) + P(A \vert B2).P(B2) + ... + P(A \vert Bn).P(Bn)$

**TODO:**
- *Distributions*
- *Maximum Likelihood Estimator*
- *Maximum a posteriori probability (MAP) estimator*

