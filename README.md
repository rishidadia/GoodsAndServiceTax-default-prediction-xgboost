GST Compliance Classification using XGBoost

This project implements a machine learning pipeline to classify GST compliance outcomes using structured GST transaction data. The focus is on handling class imbalance, model optimization, and interpretability, rather than naive accuracy-based prediction.

Problem Statement

GST datasets are often highly imbalanced, where non-compliance or abnormal outcomes form a minority class.
Traditional accuracy-based models fail to capture these critical cases.

The objective of this project is to:

Build a robust classification model on GST data

Improve minority-class detection using threshold optimization

Provide interpretability into model decisions

Approach

Performed data cleaning, preprocessing, and feature handling on structured GST data

Trained an XGBoost classifier suitable for tabular and imbalanced datasets

Used Optuna for automated hyperparameter optimization targeting F1-score

Applied decision threshold tuning to improve minority-class recall

Interpreted model predictions using SHAP for feature-level explainability

Technologies Used

Python

XGBoost

Scikit-learn

Optuna

SHAP

Pandas, NumPy, Matplotlib

Evaluation Metrics

Given the imbalanced nature of the data, model performance was evaluated using:

F1-score

ROC-AUC

Confusion Matrix

Accuracy was intentionally de-emphasized in favor of metrics that better reflect real-world classification performance.

Key Results

Optuna-based tuning significantly improved model generalization

Decision threshold optimization improved minority-class F1 score by ~18%

SHAP analysis provided clear insights into the most influential GST features

Key Takeaways

Metric selection is critical for imbalanced classification problems

Threshold tuning can be as impactful as model tuning

Explainability tools like SHAP are essential for trust in financial/compliance models
