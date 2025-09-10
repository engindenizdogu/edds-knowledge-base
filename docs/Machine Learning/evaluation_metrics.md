---
title: Evaluation Metrics
parent: Machine Learning
---
### Common Classification Metrics
**Accuracy**
: The proportion of correct predictions out of all predictions. It's a good starting point but can be misleading with imbalanced datasets.

**Confusion Matrix**
: A table that summarizes the performance of a classifier. It shows the number of True Positives (TP), True Negatives (TN), False Positives (FP), and False Negatives (FN).

 **Precision**
 : The ratio of correctly predicted positive observations to the total predicted positive observations. A high precision means your model has a low number of false positives.

 **Recall (or Sensitivity)**
 : The ratio of correctly predicted positive observations to all observations in the actual class. A high recall means your model has a low number of false negatives.
 
**F1-Score**
: The harmonic mean of Precision and Recall. It provides a single score that balances both metrics, which is especially useful for imbalanced datasets.

 **Classification Report**
 : A convenient summary that shows the precision, recall, and F1-score for each class, along with the overall accuracy.