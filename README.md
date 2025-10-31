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
