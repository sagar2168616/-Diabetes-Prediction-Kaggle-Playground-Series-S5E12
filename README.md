🩺 Diabetes Prediction — Kaggle Playground Series S5E12
📌 Project Overview

This project documents my end-to-end machine learning journey in the Kaggle Playground Series S5E12 competition.
The goal was to predict diabetes risk using demographic, lifestyle, and clinical indicators.

Rather than focusing only on the final score, this repository highlights:

Iterative model improvement

Smart feature engineering

Handling real-world data challenges

Advanced ensemble learning techniques

🧠 Key Skills Demonstrated

Exploratory Data Analysis (EDA)

Feature Engineering

Categorical Encoding Strategies

Model Selection & Evaluation

Cross-Validation & Ensembling

Data Augmentation with External Datasets

Kaggle Competition Best Practices

📊 Dataset Description

Primary Dataset: Kaggle Playground Series S5E12

Rows: 700,000

Features:

Numerical: Age, BMI, Blood Pressure, Cholesterol, Activity metrics

Categorical: Gender, Ethnicity, Education, Income, Smoking, Employment

Target: diagnosed_diabetes (binary classification)

🚀 Project Evolution (Submission Timeline)
🔹 Submission 1 — Baseline Model (Accuracy: 0.60)
Approach

Performed basic preprocessing

Separated numerical and categorical features

Applied One-Hot Encoding to categorical variables

Standardized features using StandardScaler

Trained a Logistic Regression model

Key Learnings

Logistic Regression struggles with non-linear relationships

One-hot encoding significantly increases dimensionality

Accuracy plateaued due to model simplicity

Outcome

📉 Public Score: ~0.60

Served as a baseline benchmark

🔹 Submission 2 — Feature Engineering + CatBoost (Accuracy: 0.67)
Improvements Introduced

Added domain-driven engineered features:

Pulse Pressure

Sedentary Ratio

Cholesterol / HDL Ratio

Health History Score

Performed outlier handling using IQR-based winsorization

Switched to CatBoostClassifier

Implemented early stopping

Why CatBoost?

Handles categorical features efficiently

Robust to overfitting

Performs well on tabular healthcare data

Outcome

📈 Public Score: ~0.67

Significant improvement over baseline

Confirmed importance of feature engineering

🔹 Submission 3 — Advanced Ensemble + External Data (Accuracy: 0.69)
Major Enhancements
1️⃣ External Dataset Augmentation

Integrated a secondary diabetes dataset

Removed target leakage columns (glucose, HbA1c, insulin)

Row-wise concatenation introduced intentional NaNs

Leveraged CatBoost’s ability to learn from missing values

2️⃣ Advanced Feature Engineering

Added composite features:

Blood Pressure Ratio

Lipid Risk Score

BMI × Age

Waist × BMI

History Sum Index

3️⃣ Multi-Model Ensemble

Trained three independent models:

CatBoost

LightGBM

XGBoost

Used Stratified K-Fold Cross-Validation (10 folds)

Blended predictions using weighted averaging:

Final = 0.5 * CatBoost + 0.3 * LightGBM + 0.2 * XGBoost

Outcome

📈 Public Score: ~0.69

Most stable and generalized solution

Demonstrated production-grade ML pipeline

🧩 Technical Highlights

Handled mixed datasets with missing feature alignment

Used model-specific encoding strategies

Prevented data leakage explicitly

Employed probability-based predictions for competition compliance

Balanced performance vs. computational efficiency

📈 Final Results Summary
Submission	Technique Used	Public Score
1	Logistic Regression + OHE	0.60
2	Feature Engineering + CatBoost	0.67
3	External Data + Ensemble	0.69
🎯 What This Project Shows

✔ Ability to iterate intelligently
✔ Understanding of model strengths & weaknesses
✔ Practical experience with large tabular datasets
✔ Kaggle-ready ML workflow
✔ Strong problem-solving mindset
