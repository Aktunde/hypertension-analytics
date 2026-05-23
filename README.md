# Hypertension_Cardiology_Center_Dataset_ Analytics 

A consulting-grade Python analysis of 350 hypertension patients from the Hypertension_Cardiology Data Center, addressing two clinical problem statements using data profiling, cleaning, feature engineering, EDA, statistical testing, logistic regression modelling, and clinical recommendations.

---

### Problem Statements

PS1 — BP Control Failure Prediction**
> "What predicts BP control failure at 3 months, and can we identify high-risk patients at the point of prescription?"

PS2 — Drug Class Effectiveness by Comorbidity Profile**
> "Which antihypertensive drug class delivers the best outcomes for patients with specific comorbidity profiles?"
---

### Key Findings

| Metric | Value |
|---|---|
| Patients analysed | 350 |
| Analysis period | January – December 2024 |
| BP control rate (3 months) | **9.4%** (33/350) — primary challenge |
| Mean SBP reduction | ~14 mmHg across all drug classes |
| Strongest failure predictor | Medication adherence (Poor = 32% of cohort) |
| Most treatment-resistant profile | DM+CKD patients |
| PS1 model | Logistic regression, prescription-time features only |
| PS2 outcome | Drug class effectiveness varies by comorbidity profile |

---
### Recommendations Summary

1. **PS1 — Deploy prescription-time risk screening** (6-point score → Red/Amber/Green protocols)
2. **PS2 — Comorbidity-guided prescribing** (ACE/ARB for DM, CKD, DM+CKD)
3. **Adherence programme** — pharmacist-led intervention for Poor adherence patients
4. **Shorten follow-up** for Very High Risk patients (4–6 weeks vs 3 months)
5. **Data quality improvements** — add smoking, BMI, blood test fields

---
### Notebook Structure

| Phase | Description | Key Output |
|---|---|---|
| 1 | Data Review & Profiling | Column inventory, null check, value distributions |
| 2 | Data Cleaning | Type casting, range validation, cleaned_data.csv |
| 3 | Feature Engineering | Age bands, comorbidity profile, risk score, BP categories |
| 4a | Univariate EDA | Distributions, BP control outcome chart, risk score profile |
| 4b | Bivariate EDA | Correlation heatmap, drug class analysis, comorbidity × drug heatmap |
| 5 | Statistical Analysis | Chi-square, t-tests, ANOVA across PS1 & PS2 dimensions |
| 6a | PS1 Model | Logistic regression, ROC curve, feature importance, risk tiering |
| 6b | PS2 Analysis | Drug class × comorbidity pivot tables, best drug per profile |
| 6c | 4-Layer Insights | Descriptive → Diagnostic → Predictive summary |
| 7 | Recommendations | 5 ranked recommendations + executive summary |

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook hypertension_analysis.ipynb
```

Run all cells from top to bottom. Charts save to `data/processed/`.

---

## Visualisations

| Figure | Description |
|---|---|
| fig01 | Numerical feature distributions |
| fig02 | Categorical feature distributions |
| fig03 | BP control rate by drug class |
| fig04 | Risk score profile |
| fig05 | Correlation heatmap |
| fig06 | Drug class vs adherence analysis |
| fig07 | Comorbidity × drug class heatmap |
| fig08 | PS1 logistic regression coefficients + ROC curve |
| fig09 | PS1 predicted risk tiers |
| fig10 | PS2 drug-comorbidity effectiveness heatmaps |

---

## Tech Stack

Python 3.14 | pandas | numpy | matplotlib | seaborn | scipy | scikit-learn | Jupyter Notebook

---

## Author

**Topaz** — Data & Operations Analyst  
Portfolio: [github.com/Aktunde/hypertension-analytics](https://github.com/Aktunde/hypertension-analytics)  
May 2026

---

*Note: The notebook is fully reproducible when data files are placed in `data/raw/`.*

Dataset link:
https://docs.google.com/spreadsheets/d/1iopUTgsIkg9x8G-4CTSSKj34wMBdjypR/edit?usp=sharing&ouid=112336321426427042959&rtpof=true&sd=true
