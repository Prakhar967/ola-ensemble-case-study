# ola-ensemble-case-study

-- Project Overview

This project focuses on driver churn prediction for Ola using ensemble learning techniques. The business challenge is to predict whether a driver is likely to leave the company, based on demographic, performance, and financial attributes.
Driver attrition (churn) is a significant challenge in the ride-hailing industry. High churn rates increase recruitment costs, reduce service reliability, and affect overall profitability. By leveraging Bagging and Boosting techniques, this project builds predictive models to identify at-risk drivers and provide actionable recommendations for retention.

-- Problem Statement

Ola is facing high churn rates among drivers. Losing drivers frequently disrupts operations and increases costs for acquiring replacements. The Analytics Department is tasked with predicting whether a driver will leave the company or continue, based on:
  1. Demographics (City, Age, Gender, Education).
  2. Tenure Information (Joining Date, Last Working Date).
  3. Performance Data (Quarterly rating, Grade, Total business value, Monthly income).

-- Dataset and Column Profiling
  1. MMMM-YY: Reporting date (monthly).
  2. Driver_ID: Unique ID for drivers.
  3. Age: Age of the driver.
  4. Gender: Male = 0, Female = 1.
  5. City: City code of the driver.
  6. Education_Level: 0 = 10+, 1 = 12+, 2 = Graduate.
  7. Income: Monthly average income.
  8. DateOfJoining: Date of joining.
  9. LastWorkingDate: Last date of working (if driver left).
  10. JoiningDesignation: Designation at joining.
  11. Grade: Driver grade at reporting time.
  12. Total_Business_Value: Monthly total business acquired (negative = cancellation/refund/EMI adjustment).
  13. Quarterly_Rating: Rating scale (1–5).

-- Step Performed

1. Exploratory Data Analysis (EDA)
     1. Data shape, distributions, and data type conversions.
     2. Handling missing values with KNN imputation.
     3. Detecting duplicate entries & cleaning dataset.
     4. Correlation analysis between features (numeric and categorical).

2. Feature Engineering
     1. Target Variable Creation: Binary column indicating if the driver churned (last working date present = churn).
     2. Quarterly Rating Trend: Flag if driver’s rating improved.
     3. Income Trend: Flag if driver’s monthly income improved.
     4. One-hot encoding of categorical variables.

3. Class Imbalance Handling

      Resampling techniques to balance churn vs non-churn drivers.

4. Model Building

  1. Ensemble methods:
       1. Bagging (Random Forest)
       2. Boosting (XGBoost, Gradient Boosting)
  2. Hyperparameter tuning for optimized performance.

5. Results Evaluation

  1. Classification Report (Precision, Recall, F1-score).
  2. ROC-AUC Curve for model performance comparison.
  3. Feature importance analysis to identify top churn indicators.

6. Insights & Recommendations

    Business-oriented strategies to reduce churn and retain high-performing drivers.

-- Tech stack

  1. Python: pandas, numpy, matplotlib, seaborn, scikit-learn, XGBoost
  2. Colab Notebook for implementation

