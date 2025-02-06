## Credit Decisioning Model 
This project develops a credit decisioning model to predict whether a credit card applicant will default on their card, aiding the bank in making informed credit approval decisions. The model aims to balance predictive accuracy with explainability to ensure real-world practicality.
# Overview
The goal is to predict loan defaults based on applicant data, using machine learning techniques to provide actionable insights. The model will help the bank assess credit risk and decide whether to approve applicants for credit cards.
# Data Preprocessing
The dataset consists of two files: File A (application data) and File B (demographic and credit history data). Key preprocessing steps include:
<br />•	Handling missing data with KNN imputation.
<br />•	Feature engineering (e.g., calculating AGE_AT_APP, MTH_SINCE_APP).
<br />•	Data merging to combine both files on the ID column.
# Exploratory Data Analysis (EDA)
EDA identified:
<br />•	Class imbalance: Only 7.4% of applicants defaulted.
<br />•	Important features: Key predictors of default included SPENDING, ACADMOS, and ANNUAL_INCOME.
# Modeling Approach
Two models were evaluated:
<br />•	Random Forest: A tree-based ensemble model known for robustness.
<br />•	XGBoost: A gradient-boosting model that performed better in terms of AUC and F1 score.
SMOTEENN was used to handle class imbalance by resampling the minority class.
# Hyperparameter Tuning
GridSearchCV was employed to tune hyperparameters:
<br />•	XGBoost: Best parameters were learning_rate=0.1, max_depth=7, n_estimators=300.
<br />•	Random Forest: Best parameters were determined based on n_estimators, max_depth, and min_samples_split.
# Evaluation
<br />•	XGBoost: Achieved an AUC of 0.9758 and F1 score of 0.9758 during cross-validation.
<br />•	Random Forest: Achieved an AUC of 0.8661 and F1 score of 0.8661.
XGBoost outperformed Random Forest, making it the preferred model.
# Business Insights & Conclusion
<br />•	Key features influencing defaults include SPENDING, ACADMOS, and ANNUAL_INCOME.
<br />•	XGBoost showed superior performance in predicting defaults and is recommended for deployment to guide credit card approval decisions.

