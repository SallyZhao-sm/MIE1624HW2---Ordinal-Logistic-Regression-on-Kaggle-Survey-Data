# MIE1624HW2---Ordinal-Logistic-Regression-on-Kaggle-Survey-Data

This project develops an ordinal classification model to predict salary buckets of data scientists using the 2022 Kaggle Machine Learning & Data Science Survey.

## Methods
- Data Cleaning:
  - Removed irrelevant or high-missing-value features
  - Encoded ordinal/categorical variables
  - Created dummy variables for multi-choice responses
- Feature Engineering:
  - Constructed "LanguageNumber" (count of languages used)
- Feature Selection:
  - Decision Tree feature importance
  - Lasso + RFE selected 10 key predictors
- Modeling:
  - Implemented Ordinal Logistic Regression
  - 10-fold cross-validation (avg accuracy ~40.7%)
  - Bias-variance tradeoff analysis with hyperparameter C
- Model Tuning:
  - Grid Search with F1-score
  - Best hyperparameters: C=10, solver=lbfgs
- Interpretation:
  - Most predictive features: country (esp. USA), ML experience, role type, education

## Results
- Model showed slight overfitting (train > test performance)
- U.S. respondents had the highest weight in predicting salary
- ML experience years and role type strongly correlated with higher salary
- Accuracy unsuitable due to class imbalance; F1-score preferred

## Skills Demonstrated
- Data cleaning, encoding, and feature engineering
- Ordinal classification with logistic regression
- Model evaluation with cross-validation and grid search
- Handling imbalanced data with alternative metrics
