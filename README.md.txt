# HR Analytics — Salary & Attrition Prediction

## Project Overview
A dual-model machine learning project using IBM HR Analytics data to answer 
two strategic business questions:
- **Linear Regression** → How much should an employee earn?
- **Logistic Regression** → Will this employee leave the company?

## Dataset
- Source: IBM HR Analytics Employee Attrition Dataset (Kaggle)
- 1,470 employees | 35 features | 0 missing values

## Models Built
| Model | Target | Performance |
|---|---|---|
| Linear Regression | MonthlyIncome | R² = 0.8574 |
| Logistic Regression | Attrition (Yes/No) | AUC-ROC = 0.783 |

## Key Findings
- 110 employees identified as Critical — underpaid AND high attrition risk
- Sales Representatives have 72.8% average attrition risk
- OverTime is the single biggest driver of attrition
- JobLevel explains the most salary variance

## Tools Used
- Python, Jupyter Notebook
- pandas, numpy, scikit-learn, matplotlib, seaborn

## Files
- `Logistic_and_Linear_Regression.ipynb` — Full project notebook
- `HR_Analytics_Project_Report.docx` — Detailed project report