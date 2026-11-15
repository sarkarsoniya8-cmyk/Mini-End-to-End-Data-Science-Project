# Customer Churn Prediction — Mini End-to-End Data Science Project

## Overview
This repository contains a complete end-to-end data science workflow analyzing and predicting customer churn. It covers data collection, data cleaning, exploratory data analysis (EDA), machine learning modeling, evaluation, and business insight generation.

## Repository Structure
```text
├── data/
│   ├── raw/
│   │   └── raw_churn_data.csv        # Original uncleaned dataset
│   └── processed/
│       └── cleaned_churn_data.csv    # Final cleaned dataset (Deliverable 2)
├── notebooks/
│   └── churn_end_to_end.ipynb        # End-to-end Jupyter Notebook (Deliverable 1)
├── reports/
│   └── project_report.md             # Project report: problem -> approach -> results -> insights (Deliverable 3)
├── README.md                         # Project documentation
└── requirements.txt                  # Python dependencies
```

## Model Evaluation Summary
- **Logistic Regression:** 74.00% Accuracy
- **Random Forest:** 75.00% Accuracy
- **Decision Tree:** 74.00% Accuracy

## Key Insights
1. **Month-to-Month Contracts Drive Churn:** Customers on flexible monthly plans leave at a substantially higher rate than annual contract holders.
2. **Early Tenure Vulnerability:** Churn concentration is highest during the first year of subscription.
3. **High Monthly Charges:** Subscribers paying higher monthly rates require bundled value-added services to improve retention.

## How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook notebooks/churn_end_to_end.ipynb
   ```
