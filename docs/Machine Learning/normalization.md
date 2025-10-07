---
title: Normalization
parent: Machine Learning
---
### Cases where normalization _is important_
- **Gradient-based methods** (where optimization depends on scale):
    - **Linear/Logistic Regression (with gradient descent)**
    - **Neural Networks / Deep Learning**
    - **Support Vector Machines (SVMs)**
    - **k-Nearest Neighbors (kNN)**
    - **Principal Component Analysis (PCA), LDA**

**Reason:** If features are on very different scales (e.g., "age in years" vs. "income in dollars"), the algorithm may:
- converge slower (or get stuck in poor minima),
- assign disproportionate importance to larger-scaled features.

**Example:** In kNN, distance metrics (Euclidean, Manhattan) are directly scale-sensitive.

### Cases where normalization _is not strictly necessary_
- **Tree-based methods** (scale-invariant algorithms):
    - **Decision Trees**
    - **Random Forests**
    - **Gradient Boosted Trees (XGBoost, LightGBM, CatBoost)**

**Reason:** Trees split data by thresholds ("is feature > X?"), which are not affected by whether the feature is in cm or m. Scaling won’t change the splits.

- **Naïve Bayes (with categorical data)**: Works with probability distributions, not distances.

### Borderline cases
- **Naïve Bayes with continuous features (Gaussian NB)** → Standardization can help, since the algorithm assumes normally distributed features.
- **Linear models with regularization (Lasso, Ridge, ElasticNet)** → Strongly recommended, because the penalty is scale-dependent.

### Rule of thumb
- If the model uses **distances, gradients, or variance-based decomposition**, normalize or standardize.
- If it uses **rules, counts, or thresholds**, scaling usually doesn’t matter.