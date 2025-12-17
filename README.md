# GST-Based Loan Default Prediction using XGBoost

This repository presents a practical machine learning case study for predicting loan defaults using GST-linked transactional and behavioral features. The focus is on handling class imbalance and evaluating models using appropriate metrics rather than accuracy.

---

## Problem Statement

Predict whether a customer will default on a loan based on GST-related financial behavior and categorical attributes.

Key challenges addressed:
- Severe class imbalance
- Misleading nature of accuracy in imbalanced datasets
- Metric-driven model evaluation

---

## Dataset Overview

- Binary classification problem (Default / No Default)
- Heavily imbalanced target variable
- Mix of numerical and categorical features

> The full dataset is not included due to GitHub file size limits.  
> This repository focuses on modeling decisions and evaluation methodology.

---

## Evaluation Metrics

Accuracy was intentionally avoided for model selection.

Metrics used:
- Precision
- Recall
- F1 Score
- ROC-AUC

Primary optimization metric: **F1 Score**

---

## Modeling Approach

Models explored:
- Logistic Regression (baseline)
- Random Forest
- XGBoost (final model)

XGBoost was selected due to strong performance on structured tabular data and robustness under class imbalance.

---

## Handling Class Imbalance

Approaches considered:
- Metric-aware optimization
- Class weighting
- Sampling strategies

Final choice: **RandomOverSampler**

Why RandomOverSampler:
- Preserves all majority-class information
- Improves minority-class signal
- Empirically improved recall and F1 score

Over-sampling was applied only on training data to prevent leakage.

---

## Validation Strategy

- Stratified cross-validation
- Sampling performed on training folds only
- Hyperparameter tuning using Optuna
- Model selection based on mean F1 score

---

## Final Pipeline

Target Encoding
→ RandomOverSampler
→ XGBoost Classifier


---

## Key Takeaways

- Accuracy is unreliable for imbalanced classification
- F1 score provides a better optimization objective
- Over-sampling can improve minority-class detection
- Validation-driven decisions are critical

---

## Tech Stack

- Python
- XGBoost
- scikit-learn
- imbalanced-learn
- category-encoders
- Optuna

---

## Notes

GitHub renders Jupyter notebooks in light mode by default.  
For best viewing experience, open the notebook locally or in VS Code.

---

## Author

Built as a focused case study in imbalanced classification and metric-driven machine learning.
