# Customer Churn Prediction

An end-to-end machine learning project that predicts whether a telecom customer is likely to leave the company.

## Project Overview

The project analyzes customer information, trains multiple classification models, and produces a churn probability and risk level for each customer.

## Workflow

- Data cleaning and exploratory data analysis
- Feature preprocessing using a Scikit-learn Pipeline
- Missing-value handling, scaling, and one-hot encoding
- Stratified train/test split
- Model training and cross-validation
- Hyperparameter tuning
- Threshold evaluation
- Model explainability using SHAP
- Pipeline testing and model saving

## Models

- Logistic Regression
- Random Forest
- XGBoost

## Cross-Validation Results

| Metric | Logistic Regression | Tuned Random Forest | XGBoost |
|---|---:|---:|---:|
| Accuracy | 0.7485 | 0.7593 | 0.7600 |
| Precision | 0.5169 | 0.5316 | 0.5331 |
| Recall | 0.8013 | 0.7933 | 0.7726 |
| F1-score | 0.6283 | **0.6363** | 0.6308 |
| ROC-AUC | 0.8460 | **0.8470** | 0.8436 |

## Final Model

The Tuned Random Forest was selected because it achieved the best F1-score and ROC-AUC while maintaining strong churn recall.

The selected classification threshold is `0.50`.

## Risk Levels

- Low Risk: probability below `0.30`
- Medium Risk: probability from `0.30` to below `0.60`
- High Risk: probability of `0.60` or higher

## Explainability

SHAP was used to explain the model globally and for individual customers. Important features included contract type, tenure, internet service, technical support, and total charges.

## Technologies

Python, Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost, SHAP, Joblib, and Jupyter Notebook.

## Future Improvements

- Deploy the model using Streamlit or FastAPI
- Build a customer-retention dashboard
- Add model monitoring and automated testing
