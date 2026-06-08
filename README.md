# fraud-detection-fintech
# Credit Card Fraud Detection — FinTech Analysis

## Project Overview
An end-to-end fraud detection project applying 
logistic regression to identify fraudulent credit 
card transactions from a dataset of 284,807 
real anonymised European transactions.

This project goes beyond model building to analyse 
the **business impact** of different detection 
thresholds — the core decision every FinTech 
fraud team faces daily.

---

## Key Findings

- Only 0.17% of transactions are fraudulent — 
  extreme class imbalance is the core technical 
  challenge
- Fraudsters deliberately keep amounts small — 
  median fraud amount is €9.25 vs €22.00 for 
  legitimate transactions
- Model achieves 97.22% ROC AUC score — 
  strong discriminative ability
- At default 0.5 threshold the model catches 
  90/98 fraud cases but wrongly blocks 1,389 
  legitimate customers — costing €122,635 in 
  lost revenue vs €10,999 in fraud prevented
- Raising threshold to 0.9 reduces false blocks 
  to 266 and cuts net cost to €12,853 — 
  an 89% improvement in commercial outcome
- True solution requires additional features 
  (device fingerprinting, location data, 
  behavioural signals) to improve precision 
  without sacrificing recall

---

## The Business Problem

| Threshold | Fraud Caught | False Blocks | Net Benefit |
|---|---|---|---|
| 0.1 | 93 | 11,360 | -€991,609 |
| 0.5 | 90 | 1,389 | -€111,636 |
| 0.9 | 87 | 266 | -€12,853 |

A technically excellent model can still be 
commercially harmful. This analysis demonstrates 
why threshold tuning and business context are 
as important as model accuracy in real 
FinTech environments.

---

## Model Performance

| Metric | Value |
|---|---|
| ROC AUC Score | 0.9722 |
| Recall (Fraud) | 92% |
| Precision (Fraud) | 6% |
| Overall Accuracy | 98% |

---

## Tools Used
- **Python** — data analysis and modelling
- **Pandas & NumPy** — data manipulation
- **Scikit-learn** — logistic regression model
- **Matplotlib & Seaborn** — visualisations
- **Power BI** — business dashboard

---

## Libraries Required
```bash
pip install pandas numpy scikit-learn 
matplotlib seaborn imbalanced-learn
