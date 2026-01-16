# CreditWise – Loan Approval Prediction System

CreditWise is a machine learning project that predicts whether a loan application will be approved or not based on applicant financial, demographic, and credit-related attributes. The project demonstrates a complete ML workflow including data exploration, preprocessing, feature encoding, scaling, model training, and evaluation.

---

## 📌 Project Overview

Loan approval is a critical process for financial institutions. This project uses historical loan application data to build predictive models that classify whether a loan will be **approved (Yes)** or **rejected (No)**.

The notebook performs:
- Exploratory Data Analysis (EDA)
- Feature preprocessing and encoding
- Model training using multiple algorithms
- Performance evaluation using standard classification metrics

---

## 📂 Dataset

**File:** `loan_approval_data.csv`

Each row represents a loan applicant with the following attributes:

### 🔢 Numerical Features
- `Applicant_Income`
- `Coapplicant_Income`
- `Age`
- `Dependents`
- `Credit_Score`
- `Existing_Loans`
- `DTI_Ratio`
- `Savings`
- `Collateral_Value`
- `Loan_Amount`
- `Loan_Term`

### 🏷 Categorical Features
- `Employment_Status`
- `Marital_Status`
- `Loan_Purpose`
- `Property_Area`
- `Education_Level`
- `Gender`
- `Employer_Category`

### 🎯 Target Variable
- `Loan_Approved` → **Yes / No**

---

## 🔍 Exploratory Data Analysis (EDA)

The notebook includes:
- Dataset structure and summary (`info()`, `describe()`)
- Missing value analysis
- Class distribution of `Loan_Approved`
- Visualizations for:
  - Loan approval ratio
  - Income distributions
  - Categorical feature distributions

---

## 🛠 Data Preprocessing

### 1. Column Removal
- `Applicant_ID` is dropped as it does not contribute to prediction.

### 2. Encoding
- **Label Encoding**:
  - `Education_Level`
  - `Loan_Approved`
- **One-Hot Encoding**:
  - `Employment_Status`
  - `Marital_Status`
  - `Loan_Purpose`
  - `Property_Area`
  - `Gender`
  - `Employer_Category`

### 3. Train-Test Split
- Data is split into training and testing sets using `train_test_split()`.

### 4. Feature Scaling
- `StandardScaler` is applied to normalize numerical features.

---

## 🤖 Machine Learning Models

The following classification models are trained and evaluated:

### ✅ Logistic Regression
- Baseline linear classifier
- Evaluated using accuracy, precision, recall, F1-score, and confusion matrix

### ✅ K-Nearest Neighbors (KNN)
- Distance-based classifier with `k=5`
- Evaluated on scaled feature space

### ✅ Naive Bayes (GaussianNB)
- Probabilistic classifier assuming feature independence
- Evaluated using standard classification metrics

---

## 📊 Model Evaluation Metrics

Each model is evaluated using:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **Confusion Matrix**

These metrics help compare model performance and determine the best classifier for loan approval prediction.

---


