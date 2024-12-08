## MICROSOFT CLASSIFYING CYBERSECURITY INCIDENTS
# OVERVIEW
This repository contains the implementation of a machine learning pipeline designed to classify cybersecurity incidents into three categories: True Positive (TP), Benign Positive (BP), and False Positive (FP). Using the Microsoft GUIDE dataset, the project leverages advanced data preprocessing, feature engineering, and classification techniques to optimize model performance and support Security Operation Centers (SOCs) in automating incident triage.

# BUSSINESS USE CASES:
The developed solution can significantly improve multiple areas of cybersecurity operations:
Security Operations Centers (SOCs): Automates the triage process and enhances analysts' decision-making.
Incident Response Automation: Provides SOCs with faster, data-driven insights and recommended actions.
Threat Intelligence: Increases the precision of detecting true and false positives using historical data.
Enterprise Security Management: Reduces false positives, improves threat detection, and ensures swift incident response.
# PROJECT APPROACH
1. Data Exploration and Preprocessing
Initial Inspection: Load and examine the train dataset (train.csv) to understand the structure, data types, and distribution of the target variable.
Exploratory Data Analysis (EDA): Visualize patterns, identify correlations, and detect anomalies, particularly class imbalances.
2. Model Building
Train-Validation Split: Split the data into training and validation sets for effective model evaluation.
Baseline Model: Start with simple models (e.g., Logistic Regression, Decision Trees) to set a performance benchmark.
Advanced Models: Use Random Forest, XGBoost, and other sophisticated models for classification.
Cross-Validation: Implement k-fold cross-validation to ensure robustness.
3. Model Evaluation
Performance Metrics: Focus on Macro-F1 Score, Precision, and Recall to measure the model’s ability to generalize to unseen data.
Hyperparameter Tuning: Use techniques like Grid Search or Random Search to optimize model performance.
Handling Class Imbalance: Apply methods like SMOTE or adjust class weights to handle class imbalance.
4. Final Evaluation
Testing: Evaluate the final model using the test dataset (test.csv) and report key metrics.
Comparison to Baseline: Ensure the model’s performance outperforms the baseline and holds up on unseen data.
5.RESULTS
Model Performance: A highly accurate classification model that predicts cybersecurity incident triage grades (TP, BP, FP).
Feature Analysis: Insights into which features influence model predictions the most.
Model Documentation: Comprehensive process documentation, highlighting each phase from data collection to model evaluation.
Evaluation Metrics
Macro-F1 Score: Balances precision and recall, providing a holistic view of performance across all classes.
Precision: Measures the proportion of true positive predictions out of all positive predictions.
Recall: Measures the model’s ability to identify all true positives, ensuring critical incidents are not missed.
Dataset Overview
The GUIDE dataset contains cybersecurity incident records annotated with triage grades (TP, BP, FP). The data is stratified and includes over 1 million triage-annotated incidents, ensuring a comprehensive representation of real-world security incidents.
6.Features:
Evidence: Individual pieces of evidence like IP addresses, emails, and user details.
Alerts: Aggregated evidence signaling a potential security incident.
Incidents: A collection of alerts representing a complete security threat scenario.
Usage
Load the data from train.csv and test.csv.
Preprocess and engineer features.
Train and evaluate your model.
Check model performance with key metrics (Macro-F1 Score, Precision, Recall).

# RESULTS:
Best Model is LIGHTGM
overall F1 Score:
Validation Set: 0.99,Test Set: 0.96
Feature Importance:Top features like OrgId, IncidentId,alertTitle and DetectorId significantly influenced predictions.
Model Performance:my model is performing excellently overall, with Class 2 being well-detected (high TP) and Class 0(BP) and Class 1(FP) showing good.

# DATASET:
Microsoft GUIDE Dataset (processed into traindata_processed.csv and testdata_processed.csv)

# TECHNOLOGIES USED :python
Pandas: Data handling and manipulation.
Scikit-Learn: Model training (Random Forest), evaluation, and splitting data.
Imbalanced-learn (imblearn): Handling imbalanced datasets with SMOTE.
Joblib: Model serialization (saving and loading the model).
LightGBM,XGBM: Efficient and scalable machine learning model for classification tasks
