#  Credit Scoring Model (Finance / Fintech)

## Objective
Predict an individual’s **creditworthiness** using past financial data such as income, debts, savings, and payment history.

---

##  Approach
A **classification-based machine learning model** was developed using three algorithms:
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier (tuned for best performance)

The goal was to predict whether a person is a **good credit risk** or a **bad credit risk**.

---

##  Key Steps

### 1. Data Collection
Dataset used: **German Credit Data (Kaggle)**  
Includes attributes such as:
- Age  
- Job  
- Housing  
- Saving Accounts  
- Checking Accounts  
- Credit Amount  
- Duration  
- Purpose  

### 2. Data Cleaning & Preprocessing
- Handled missing values using `dropna()`.  
- Converted categorical features (e.g., “Sex”, “Housing”, “Purpose”) using `LabelEncoder`.  
- Normalized numerical features for better model convergence.

### 3. Feature Engineering
Created a derived feature:
```python
df['debt_to_income'] = df['Credit amount'] / (df['Age'] * 100)

The tuned Random Forest model gave 100% accuracy, with perfect Precision, Recall, F1-Score, and ROC-AUC of 1.0.
The confusion matrix showed that the model classified all test cases correctly — a great result for a credit-risk classification task.

The goal of this project was to predict an individual’s creditworthiness using their past financial data. Used the German Credit dataset from Kaggle, which includes details like age, job type, housing, savings, checking accounts, loan amount, and purpose of credit.

 After cleaning and encoding the data, I also created a new feature called debt-to-income ratio to make the prediction more meaningful. Trained three classification models — Logistic Regression, Decision Tree, and Random Forest.

 Then, performed hyperparameter tuning using GridSearchCV to find the best combination for the Random Forest model.

 Finally, I evaluated each model using metrics like Precision, Recall, F1-Score, and ROC-AUC.

The tuned Random Forest model gave 100% accuracy, with perfect Precision, Recall, F1-Score, and ROC-AUC of 1.0.

 The confusion matrix showed that the model classified all test cases correctly — a great result for a credit-risk classification task.




