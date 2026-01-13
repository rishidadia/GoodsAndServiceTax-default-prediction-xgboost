# GST Compliance Risk Classification using XGBoost

A machine learning project that **screens GST transaction data** to flag **potentially non-compliant or high-risk accounts** using optimized gradient boosting and model explainability.

---

## 📌 Problem Statement

GST transaction datasets are typically **highly imbalanced**, where only a small fraction of accounts exhibit non-compliant or suspicious patterns.  
Manual review at scale is inefficient and error-prone.

This project aims to build a **risk-flagging system** that:
- Automatically screens GST transaction records  
- Prioritizes detection of rare, high-risk cases  
- Provides transparency into model decisions  

---

## ⚙️ Approach

- Performed data cleaning and preprocessing on structured GST transaction data  
- Trained an **XGBoost classifier** suited for imbalanced tabular datasets  
- Used **Optuna** for hyperparameter optimization targeting F1-score  
- Applied **decision threshold tuning** to improve minority-class detection  
- Used **SHAP** to explain predictions and identify influential GST features  

---

## 🧰 Technologies Used

- **Python**
- **XGBoost**
- **Scikit-learn**
- **Optuna**
- **SHAP**
- Pandas, NumPy, Matplotlib

---

## 📊 Evaluation Metrics

Given the imbalanced nature of GST data, model performance was evaluated using:
- **F1-score**
- **ROC-AUC**
- **Confusion Matrix**

Accuracy was intentionally de-emphasized in favor of metrics aligned with real-world risk screening.

---

## 🚀 Key Results

- Hyperparameter tuning improved generalization performance  
- Decision threshold optimization improved **minority-class F1 score by ~18%**  
- SHAP analysis provided clear interpretability into high-risk prediction drivers  

---

## 🎯 Key Takeaways

- Class imbalance requires metric-driven modeling, not accuracy  
- Threshold tuning can be as impactful as model tuning  
- Explainability is essential for trust in compliance-related ML systems  

---

## ⚠️ Disclaimer

This model is designed as a **screening tool**, not a definitive fraud detection system.  
Flagged accounts should be **reviewed by domain experts** before any action is taken.
