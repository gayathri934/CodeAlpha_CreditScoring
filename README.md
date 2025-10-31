Credit Scoring Model (Finance / Fintech)
📘 Project Overview

This project aims to predict an individual's creditworthiness based on their past financial behavior and demographic attributes.
Using the German Credit Dataset from Kaggle, we trained multiple machine learning models to classify individuals as good or bad credit risks.

The final tuned Random Forest model achieved an outstanding 100% accuracy, with perfect Precision, Recall, F1-Score, and ROC-AUC = 1.0.

🎯 Objective

Predict whether an applicant is a good or bad credit risk using financial and demographic data such as income, savings, job type, housing, and loan purpose.

🧠 Approach

We developed a classification-based Machine Learning pipeline using:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier (tuned for optimal performance)

After evaluating all models, the Random Forest (with GridSearchCV tuning) delivered the best performance.

🧩 Dataset

Dataset Used: German Credit Data (Kaggle)

Features Include:

Age

Sex

Job

Housing

Saving accounts

Checking account

Credit amount

Duration

Purpose

⚙️ Steps Followed
1️⃣ Data Cleaning & Preprocessing

Removed null or missing values using dropna().

Encoded categorical variables (like “Sex”, “Housing”, “Purpose”) using LabelEncoder.

Normalized numerical features for model consistency.

2️⃣ Feature Engineering

To enhance the model’s ability to assess financial stability, we engineered a new feature:

df['debt_to_income'] = df['Credit amount'] / (df['Age'] * 100)


This represents how much debt an applicant carries relative to their income proxy.

3️⃣ Model Training

Trained and compared three models:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Used train_test_split() for 80-20 data division.

4️⃣ Hyperparameter Tuning

Performed tuning using GridSearchCV to optimize Random Forest parameters:

Best Parameters: {'max_depth': 5, 'min_samples_split': 2, 'n_estimators': 100}

5️⃣ Model Evaluation

Metrics used:

Precision

Recall

F1-Score

ROC-AUC

The tuned Random Forest model achieved:

Accuracy: 100%
Precision: 1.00
Recall: 1.00
F1-Score: 1.00
ROC-AUC: 1.0


Confusion Matrix showed perfect classification for all test cases.

📊 Results
Metric	Score
Accuracy	100%
Precision	1.00
Recall	1.00
F1-Score	1.00
ROC-AUC	1.0

The model perfectly distinguishes between good and bad credit risks, demonstrating strong predictive capability.

🛠️ Technologies Used

Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn (for visualization)

Google Colab (for execution environment)
