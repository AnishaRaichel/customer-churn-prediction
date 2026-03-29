# Customer Churn Prediction

## Objective
This project predicts customer churn using machine learning and compares multiple algorithms.

## Dataset
IBM Telco Customer Churn Dataset

## Field Mapping
Since the dataset does not contain the exact required fields, proxy features were used:

Age → tenure  
Income → MonthlyCharges  
Purchases → TotalCharges  
Membership → Contract  
Churn → Churn  

## Models Used
- Logistic Regression
- Random Forest
- XGBoost

## Rule-Based Logic
A simple churn rule was implemented based on:
- low purchase value
- month-to-month membership
- low tenure

## Results

| Model | Accuracy |
|------|------|
| Logistic Regression | 0.779 |
| Random Forest | 0.764 |
| XGBoost | 0.7818 |
| Rule-Based Logic | 0.7178 |

## Best Model
XGBoost performed best because boosting methods capture nonlinear patterns effectively.

## Files Included
- Customer_Churn_Prediction.ipynb
- cleaned_churn_data.csv
- model_comparison_summary.txt
- WA_Fn-UseC_-Telco-Customer-Churn.csv