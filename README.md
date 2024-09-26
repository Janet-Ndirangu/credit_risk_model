Credit Risk Prediction Model
Project Overview
This project implements a Credit Risk Prediction Model that predicts the likelihood of a borrower defaulting on a loan. The model leverages machine learning techniques and is built with a Django web interface for user-friendly interaction. Several machine learning models were explored, including Random Forest, XGBoost, LightGBM, and CatBoost, with CatBoost being chosen as the final model due to its superior performance. The project is fully functional locally, but deployment is still in progress.

Features
Data Preprocessing: Handles outliers, encodes categorical variables, and scales numerical features. SMOTE was applied to balance the dataset.
Model Training: Utilizes multiple machine learning models to classify loans as risky or safe, including Random Forest, XGBoost, LightGBM, and CatBoost.
Model Evaluation: Provides key metrics like accuracy, precision, recall, and F1-score for each model.
Web Interface: A Django-based web application that allows users to input loan and borrower data to receive real-time predictions on credit risk.
Models and Performance
Random Forest: Initially used with SMOTE to address class imbalance and hyperparameter tuning via GridSearchCV. However, it was outperformed by other models.

XGBoost: Applied RandomizedSearchCV for hyperparameter tuning, resulting in an accuracy of 93.96% and an F1-score of 84%.

LightGBM: Provided slightly better results than XGBoost, with an accuracy of 94.05% and a precision of 98%. Despite faster training times, CatBoost outperformed LightGBM.

CatBoost: The final model after hyperparameter tuning. CatBoost showed excellent performance with minimal preprocessing, achieving:

Accuracy: 94.28%
Precision (Class 1): 97%
Recall (Class 1): 76%
F1-score (Class 1): 85%
Dataset
The dataset used in this project contains the following features:

person_age: Age of the borrower.
person_income: Annual income of the borrower.
person_home_ownership: Type of home ownership (RENT, OWN, MORTGAGE).
person_emp_length: Length of employment in years.
loan_intent: Purpose of the loan (PERSONAL, EDUCATION, etc.).
loan_grade: Loan quality grade.
loan_amnt: Loan amount requested.
loan_int_rate: Interest rate on the loan.
loan_status: The target variable indicating whether the loan is in default.
loan_percent_income: Percentage of income used to repay the loan.
cb_person_default_on_file: Whether the borrower has a default history on file (Y/N).
cb_person_cred_hist_length: Length of the borrower’s credit history in years.
Model Performance
After comparing various models, CatBoost was chosen as the final model due to its balanced performance between precision and recall. The CatBoost model achieved an accuracy of 94.28% with minimal data preprocessing, and it outperformed XGBoost and LightGBM in terms of recall and F1-score.

Current Status
This project is currently in development and has not been deployed yet. Users can run the model locally by following the installation instructions provided above. Deployment to a cloud platform is the next major step.

Future Work
Deployment: The next phase involves deploying the Django web app to a cloud service for broader access.
Model Optimization: Additional hyperparameter tuning for the CatBoost model to further improve performance.
Explainability: Integrating explainability tools like SHAP or LIME to provide insights into model predictions and feature importance.
Contributing
Contributions are welcome! Feel free to open issues or pull requests to suggest improvements.
