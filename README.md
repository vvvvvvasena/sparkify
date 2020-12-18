# Churn prediction project

## Project motivation

Main goal of the project is predicting whether the user will want to stop usging music streaming product (either downgrade to free tier or cancel completely).

Source data includes log-formed dataset, including activity of 225 users during 2 months. Each row represents an event of visiting a certain page by the user, inluding page and user retated details and timestamp.

This is a binary classification problem. 

## Project description:

Detailed analysis, feature engineering and modeling description can be found in the blogpost:
https://vasena91.medium.com/sparkify-churn-prediction-6320f9e69026

All source code is in Sparkify.ipnbb notebook file.

### Project stages:
- Dataset analysis
- Churn definition. Users who performed "Submit Downgrade" or "Cancellation Confirmation" actions are marked as "churn".
- Feature engineering. During analysis and feature engineering dataset has been transformed into a competely different form: each row describing user and user-based aggregated data.
Final dataset contains 21 features.
- Modeling
Classifiers being tried out are Logistic Regression, Random Forest, and Gradient Boosting. 
- Evaluation. Main evaluation metric is selected to be F1 score as there is a moderate class disbalance.  Random Forest showed the best performance:
Precision: 1.0, Recall: 0.63, F1-score: 0.77, Accuracy: 0.79