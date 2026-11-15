# Telco Customer Churn: Mini End-to-End Data Science Project

An end-to-end data science workflow on customer churn: data collection, cleaning, exploratory analysis, feature engineering, modeling, evaluation and business insights.

## Problem
A telecom company loses customers every month. This project asks: **which customers churn, why, and can we flag them early enough to act?**

## Dataset
IBM *Telco Customer Churn* sample dataset (fictional telecom customers): 7,043 customers, 21 columns (demographics, services, contract and billing, charges, tenure) and the target `Churn` (Yes/No).

## Workflow
| Step | What happens |
|---|---|
| 1. Collection | Loads the raw CSV from `data/raw/` (downloads it if missing) |
| 2. Quality checks | Missing and hidden-blank values, duplicates, wrong types, redundant categories |
| 3. Cleaning | Fixes TotalCharges (text to number, fills blanks), recodes SeniorCitizen, collapses redundant categories, validates the result |
| 4. EDA | Churn rate by contract, tenure, internet service, payment method, add-ons and customer traits, plus tenure, charges and correlation charts |
| 5. Feature engineering | `NumAddOns`, `AutoPay`, `HasInternet`; scaling and one-hot encoding inside a leakage-free pipeline |
| 6. Modeling | Logistic Regression, Decision Tree, Random Forest and Gradient Boosting vs a baseline, with stratified 5-fold cross-validation |
| 7. Evaluation | Tuned model on a held-out test set: precision, recall, F1, ROC AUC, confusion matrix; decision threshold chosen on training data |
| 8. Insights | Permutation importance, business recommendations, auto-generated report |

## Deliverables
- **Complete notebook:** [`notebooks/end_to_end_churn_project.ipynb`](notebooks/end_to_end_churn_project.ipynb)
- **Final cleaned dataset:** [`data/processed/telco_churn_cleaned.csv`](data/processed/telco_churn_cleaned.csv)
- **Project report (problem, approach, results, insights):** [`docs/project_report.md`](docs/project_report.md)
- **Charts:** [`images/`](images/)

## How to run
```bash
git clone <this-repo-url>
cd <repo-folder>
pip install -r requirements.txt
jupyter notebook notebooks/end_to_end_churn_project.ipynb     # then Run > Run All
```
In Google Colab: upload the notebook, choose **Runtime > Run all** (the notebook downloads the data itself), then download the new `data/processed`, `docs` and `images` folders.

## Project structure
```
README.md
requirements.txt
data/raw/                 raw data (unchanged)
data/processed/           final cleaned dataset
notebooks/                end-to-end notebook
docs/project_report.md    project report
images/                   charts
```

## Key results
The headline numbers (best model, test metrics, main churn drivers) are in [`docs/project_report.md`](docs/project_report.md); the report is generated from the notebook run, so every figure in it comes from the data.
