# Bank Personal Loan Modeling

A production‑ready, end‑to‑end classification project to predict which customers are likely to accept a Personal Loan.  
This repository is structured for a Data Analyst (4+ yrs) transitioning into Data Science / AI Engineering, with clear business framing, reproducible experiments, and model comparison.

## 🎯 Objective

- **Business Goal:**
Improve loan campaign efficiency by targeting customers with the highest probability of accepting a personal loan while controlling false positives to protect CAC and compliance budgets.
- **ML Task:**
Binary classification (`personal_loan` = 1 if accepted; 0 otherwise)  
- **Primary KPIs:**
Precision, Recall, F1, and Confusion Matrix. Optionally ROC‑AUC/PR‑AUC

- **Why these KPIs?**
Marketing teams typically prefer **high precision** to reduce wasted outreach spend; Risk teams often push for **balanced recall** so we don’t miss too many good customers. Choose the metric that aligns with your stakeholders.

## 📦 Dataset

- File used in notebook: `Bank_Personal_Loan_Modelling.csv`  
- Typical columns in this dataset (common schema):  
  `age, experience, income, family, ccatg/ccavg, education, mortgage, securities_account, cd_account, online, creditcard, personal_loan`  
- **Target:** `personal_loan`

## 🧭 What’s Inside

The notebook **`Bank_Personal_Loan_Modeling.ipynb`** contains:

1. **Data Preprocessing**
   - Null checks, type fixes (e.g., mapping `securities_account`, `online`, `creditcard` to booleans)
   - Train/test split (`test_size=0.2` in the code)
   - Optional scaling with `StandardScaler` for distance‑based models (KNN, SVM)

2. **EDA**
   - **Univariate** distributions
   - **Bivariate** relationships with the target
   - Business takeaways

3. **Feature Selection**
   - **Chi‑Squared** for categorical features  
   - **ANOVA** for numerical features  
   - **One‑Hot Encoding** where needed

4. **Imbalance Handling**
   - **SMOTE** (from `imblearn`) to oversample the minority class

5. **Modeling**
   - Algorithms compared: **Logistic Regression**, **SVC**, **KNN**, **Random Forest**
   - Metrics: `precision`, `recall`, `f1`, *confusion matrix*
   - Choose the best model **based on the KPI that matches your business goal**

6. **Evaluation & Interpretability**
   - Model comparison table (precision/recall/F1)  
   - Feature importance (tree‑based models) or coefficients (logistic regression)
   - Error analysis via confusion matrix

## 🧾 References

- Dataset: *Bank Personal Loan Modelling* (commonly used academic dataset).  
- Libraries: `pandas`, `numpy`, `scikit-learn`, `imbalanced-learn`, `scipy`, `matplotlib`, `seaborn`, `statsmodels`.

## 📣 Author

**Spurthi Patnam** — Data Analyst (4+ yrs) → Aspiring Data Scientist / AI Engineer.  
Open to feedback and collaboration. Connect on LinkedIn and star the repo if this helped you!


