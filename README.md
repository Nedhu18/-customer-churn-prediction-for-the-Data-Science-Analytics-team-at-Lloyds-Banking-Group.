# -customer-churn-prediction-for-the-Data-Science-Analytics-team-at-Lloyds-Banking-Group.
Overview

This project builds a complete end-to-end customer churn prediction pipeline using demographic data. It includes:

Data preprocessing
Exploratory Data Analysis (EDA)
Feature engineering
Machine learning model development
Model evaluation with visualizations
🎯 Objectives
Understand customer behavior using data
Identify patterns influencing churn
Build predictive models
Evaluate model performance using metrics and charts
📁 Dataset

📄 File: Customer_Churn_Data_Large.xlsx
👥 Records: 1000 customers

Features:
Age
Gender
Marital Status
Income Level

⚠️ Note:
The dataset did not include a churn column, so a synthetic churn variable was created using business logic.

🧠 Churn Logic (Synthetic)
if Age < 30 and IncomeLevel == 'Low':
    churn = 1
elif MaritalStatus == 'Single' and IncomeLevel == 'Low':
    churn = 1
elif IncomeLevel == 'High' and MaritalStatus == 'Married':
    churn = 0
else:
    churn = probabilistic
🔍 Exploratory Data Analysis (EDA)
📊 Visualizations
Chart	Description
Age Distribution	Customer age spread
Gender Distribution	Male vs Female
Income Distribution	Low / Medium / High
Churn Distribution	Churn vs Non-churn

Data Preprocessing
✔ No missing values
✔ One-hot encoding for categorical variables
✔ Standardization of numerical features
✔ Removed unnecessary columns (CustomerID)
🤖 Machine Learning Models
Model	Purpose
Logistic Regression	Baseline model
Random Forest	Handles non-linear patterns
XGBoost	High-performance model
📈 Model Evaluation
Metrics Used:
Accuracy Score
Confusion Matrix
ROC Curve
📊 Model Comparison
Model	Accuracy
Logistic Regression	~78%
Random Forest	~88%
XGBoost	~91%

📊 Visualization included in report.

🔑 Feature Importance

Top features influencing churn:

Age
Income Level
Marital Status
Future Improvements
Use real-world churn dataset
Add behavioral & transactional data
Deploy model (Flask / Streamlit)
Build dashboard (Power BI / Tableau)
