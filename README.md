# Customer-Churn-Prediction-using-Python
Project focuses on building a robust ML model to predict customer churn by identifying risky customers. The steps include EDA and Feature Engineering, Model Training, Hyperparameter Tuning &amp; providing actionable insights. 
 ## The Business Problem

Customer attrition (churn) is a silent profitability killer. Acquiring a new customer is up to 25 times more expensive than retaining an existing one. 
Our goal is to shift from a reactive stance to a proactive intervention strategy.

This model provides the business with a crucial early warning system, allowing marketing, sales, and support teams to prioritize resources and save the most valuable customers with a high propensity to leave.

### Project Goals

Prediction: Develop a classification model that accurately predicts customer churn.

Driver Identification: Analyse feature importance to uncover the true behavioral and demographic drivers of churn.

Actionable Strategy: Translate model insights into clear, quantifiable business recommendations for customer retention.

### Methodology & Pipeline

The entire process is documented step-by-step within the FINAL CUSTOMER CHURN ipynb Jupyter notebook.

##### 1. Data Processing & EDA

Initial Audit: Assessed dataset size, missing values, and data types.

Visual Analysis: Used distribution plots and correlation matrices to understand the relationship between various features (e.g., Monthly_Spend, Support_Calls) and the target variable (Churn).

Outlier Treatment: Handled extreme values (e.g., using capping or transformation) to ensure model stability.

##### 2. Feature Engineering

Crucially, several new, highly predictive features were engineered to capture customer behavior complexity:

Spend_per_Use: The ratio of monthly spending to service usage/minutes.

High_Support: A binary flag for customers with significantly higher-than-average support interactions.

Late_Payer: A derived feature indicating a history of missed or delayed payments.

##### 3. Model Selection & Training

Models Evaluated: Logistic Regression, Random Forest Classifier, and Gradient Boosting Classifier.

Evaluation Metric: The primary metric focused on was the  F1-Score to ensure a balance between Precision and Recall.

Cross-Validation: Utilized Stratified K-Fold Cross-Validation  to ensure robust and unbiased performance estimates across different models.

4. Hyperparameter Tuning

Used GridSearchCV, RandomizedSearchCV, or manual tuning to optimize the final chosen model, the Gradient Boosting Classifier, for peak performance.

📈 Key Results and Insights

###### Model Performance Summary

Gradient Boosting  - [F1 SCORE] = [0.9412]

Random Forest - [F1-Score] = [0.9379]

Logistic Regression - [F1-Score] = [0.8702]

###### Top 3 Churn Drivers 

Model interpretation confirmed that churn is driven by a combination of cost, usage, and service quality factors.

.[Support Calls]:Repeated negative interactions signal service dissatisfaction

[Total Spend]: 

[Contract Length- Monthly ]: .

#### Business Recommendations

**Based on the model's insights, the following strategic actions are recommended to maximize customer retention
**

Proactive Intervention for High-Value, High-Risk Customers: Identify the top 5% of customers predicted to churn and immediately enroll them in a dedicated retention campaign 

Targeted Service Improvement: Since Support Calls is the primary driver, allocate resources to improve the service quality associated with customer service to reduce the dissatisfaction.

Financial Strategy Review: The importance of features like Late_Payer suggests creating flexible or delayed payment options for customers showing early signs of financial difficulty to prevent churn.
