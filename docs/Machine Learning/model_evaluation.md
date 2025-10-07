---
title: Model Evaluation
parent: Machine Learning
---
#### Common Classification Metrics

| Pred/Actual | 0                   | 1                   |
| ----------- | ------------------- | ------------------- |
| **0**       | True Negative (TN)  | False Negative (FN) |
| **1**       | False Positive (FP) | True Positive (TP)  |

**Accuracy:** The proportion of correct predictions out of all predictions. It's a good starting point but can be misleading with imbalanced datasets.

$$(TP + TN) \over (TP + TN + FP + FN)$$

**Precision:** The ratio of correctly predicted positive observations to the total predicted positive observations. A high precision means your model has a low number of false positives.

$$TP \over (TP + FP)$$

**Recall (or Sensitivity):** The ratio of correctly predicted positive observations to all observations in the actual class. A high recall means your model has a low number of false negatives.

$$TP \over (TP + FN)$$

**F1-Score:** The harmonic mean of Precision and Recall. It provides a single score that balances both metrics, which is especially useful for imbalanced datasets.

$$\text{F1} = {(2 * Precision * Recall)  \over (Precision + Recall)}$$

#### Bias and Variance

$$\text{Total Error}=Bias^2+Variance+\text{Irreducible Error}$$

#### Underfitting and Overfitting
**Underfitting:** 
- Low-dimensional
- Heavily regularized 
- Bad modeling assumption

> **Note:** High bias = Model consistently misses relevant patterns (underfitting)

**Overfitting:**
- High dimensional or non-parametric
- Weakly regularized
- Not enough data

> **Note:** High variance = Model is overly sensitive to training data (overfitting)

#### Regularization
Core idea: $\text{J}=\text{Loss Function}+\text{Regularization Penalty}$
For any model with parameters $\theta$:
- **L2 Regularization**: Add $\lambda \sum \theta_j^2$​
- **L1 Regularization**: Add $\lambda \sum \vert \theta_j \vert$
