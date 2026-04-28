# HR Analytics — Employee Salary & Attrition Prediction

## Project Overview
This project applies Machine Learning on IBM's HR Analytics dataset to solve two critical business problems faced by organizations:

- **Linear Regression** → Predict how much salary an employee should earn
- **Logistic Regression** → Predict whether an employee is likely to leave the company

Both models are built on the same dataset, creating a dual-lens consulting framework that identifies underpaid, high-risk employees and enables targeted retention strategies.

---

## Dataset
| Attribute | Detail |
|---|---|
| Name | IBM HR Analytics Employee Attrition Dataset |
| Source | Kaggle |
| Rows | 1,470 employees |
| Columns | 35 features |
| Missing Values | 0 (completely clean) |

---

## Problem Statement
An organization is experiencing high employee turnover and suspects pay inequity is a contributing factor. As a data consultant, the goal is to:
1. Quantify how much each employee should be earning
2. Predict which employees are at risk of leaving
3. Combine both insights into an actionable retention strategy

---

## Models Built

| Model | Target Variable | Performance |
|---|---|---|
| Linear Regression | MonthlyIncome (continuous) | R² = 0.8574 |
| Logistic Regression | Attrition — Yes/No (binary) | AUC-ROC = 0.783 |

---

## Key Findings

### Linear Regression — Salary Prediction
- Model explains **85.7% of salary variance**
- **JobLevel** is the strongest salary driver — each level up adds ~43% to salary
- **JobRole** matters more than Department — Sales Reps and Lab Technicians are systematically underpaid
- Performance Rating has almost no impact on salary — compensation is role-driven, not merit-driven

### Logistic Regression — Attrition Prediction
- Model correctly identifies leavers **78.3% of the time (AUC-ROC)**
- Caught **60% of employees** who actually left
- **OverTime** is the single biggest predictor of attrition
- Sales Representatives have a **72.8% average attrition risk**
- Employees with no promotion in 2+ years are significantly more likely to leave

### Combined Risk Analysis
| Risk Category | Count | Description |
|---|---|---|
| Critical (Underpaid + High Risk) | 110 employees | Immediate intervention required |
| High Risk | 231 employees | Non-monetary retention needed |
| Underpaid | 471 employees | 1 in 3 employees earning below predicted salary |

---

## Consulting Recommendation
> Sales Representatives and Laboratory Technicians are simultaneously the most underpaid and the most likely to leave. Immediate salary corrections in these roles, combined with an overtime policy review, represent the highest-ROI retention investment available to this organization.

---

## Project Steps
| Step | Action |
|---|---|
| 1 | Data loading and basic exploration |
| 2 | Exploratory Data Analysis — 5 key visualizations |
| 3 | Preprocessing — encoding, log transformation, scaling |
| 4 | Linear Regression — salary prediction model |
| 5 | Logistic Regression — attrition prediction model |
| 6 | Combined risk table — final consulting output |

---

## Tools & Libraries
| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Jupyter Notebook | Development environment |
| pandas | Data manipulation |
| numpy | Numerical operations |
| scikit-learn | Model building and evaluation |
| matplotlib & seaborn | Data visualization |

---

## Files in This Repository
| File | Description |
|---|---|
| `Logistic_and_Linear_Regression.ipynb` | Complete project notebook with code and outputs |
| `HR_Analytics_Project_Report.docx` | Detailed project report |
| `WA_Fn-UseC_-HR-Employee-Attrition.csv` | IBM HR Analytics dataset |

---

## Results Summary
- **Linear Regression R²:** 0.8574 — Strong salary prediction
- **Logistic Regression AUC-ROC:** 0.783 — Solid attrition discrimination
- **Critical employees identified:** 110 out of 1,470
- **Top attrition driver:** OverTime
- **Top salary driver:** JobLevel
