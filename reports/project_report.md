# Project Report: Customer Churn Prediction & Retention Analysis

## 1. Problem Statement
Customer churn directly impacts recurring revenue in subscription businesses. The goal of this project is to analyze customer behavior, identify the primary drivers of churn, and build a classification model to predict high-risk customers so retention teams can intervene proactively.

## 2. Approach
1. **Data Collection & Cleaning:** Loaded raw customer data (`raw_churn_data.csv`), converted `TotalCharges` to numeric format, imputed missing values using the median, removed non-predictive identifiers (`customerID`), and exported the final cleaned dataset (`cleaned_churn_data.csv`).
2. **Exploratory Data Analysis (EDA):** Examined churn distribution across contract types, customer tenure, internet service tiers, and monthly charges.
3. **Feature Engineering & Preprocessing:** Label-encoded categorical variables and standardized numerical features using `StandardScaler`.
4. **Machine Learning Modeling:** Trained and evaluated three classification algorithms (`Logistic Regression`, `Decision Tree`, and `Random Forest`) using an 80/20 train-test split.

## 3. Results
* **Logistic Regression:** 74.00% Accuracy — Strong baseline performance with clear feature interpretability.
* **Random Forest:** 75.00% Accuracy — Robust ensemble performance capturing non-linear relationships.
* **Decision Tree:** 74.00% Accuracy — Good rule-based interpretability with depth control (`max_depth=5`).

## 4. Key Insights & Recommendations
* **Contract Type:** Customers on month-to-month contracts exhibit the highest churn rate compared to 1-year and 2-year contracts. *Recommendation:* Offer promotional discounts to transition month-to-month customers onto annual contracts.
* **Early Tenure Risk:** Customers in their first 6–12 months are significantly more likely to leave. *Recommendation:* Introduce dedicated onboarding check-ins during the first 90 days.
* **Fiber Optic & High Monthly Charges:** Users with higher monthly bills ($75+) churn at higher rates. *Recommendation:* Bundle complimentary tech support or loyalty perks for high-tier subscribers.
