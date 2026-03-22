# 💳 CreditWise Loan System

A Machine Learning project that predicts whether a loan should be approved or not based on applicant financial and personal data.

---

## 🚀 Project Overview

The **CreditWise Loan System** is built to automate the loan approval process using machine learning.
It analyzes multiple features such as income, credit score, employment status, and financial ratios to make intelligent predictions.

This reduces manual effort and helps financial institutions make faster and more reliable decisions.

---

## 📊 Dataset Details

* 📌 Total Records: **1000 entries**
* 📌 Features: **19 input features + 1 target (Loan_Approved)**
* 📌 Data Types:

  * Numerical (income, credit score, etc.)
  * Categorical (gender, education, loan purpose, etc.)

---

## ⚙️ How the Model Works

### 1. Data Preprocessing

* Handled missing values:

  * Numerical → replaced using **mean**
  * Categorical → replaced using **mode**
* Removed unnecessary column:

  * `Applicant_ID` (not useful for prediction)

---

### 2. Exploratory Data Analysis (EDA)

* Checked class distribution of loan approvals
* Visualized:

  * Income distributions
  * Credit score vs loan approval
  * Categorical feature distributions
* Key Insight:

  * ✅ Higher **credit score → higher chances of loan approval**
  * ❌ Income alone did not show strong pattern

---

### 3. Feature Engineering

* Applied encoding:

  * Label Encoding → Education_Level, Loan_Approved
  * One-Hot Encoding → categorical variables

* Created new features:

  * `DTI_Ratio_sq` (Debt-to-Income squared)
  * `Credit_Score_sq`

👉 Purpose: Increase impact of important features identified in correlation analysis

---

### 4. Feature Scaling

* Applied **StandardScaler** to normalize data
* Important for distance-based models like KNN

---

### 5. Model Training

Multiple models were trained and compared:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Naive Bayes

---

### 6. Model Evaluation

Metrics used:

* Accuracy
* Precision ⚠️ (most important in this case)
* Recall
* F1 Score
* Confusion Matrix

👉 Why Precision is important?
Because we want to **avoid approving high-risk customers**.

---

## 📈 Results & Achievements

* ✅ **Naive Bayes performed best based on precision**
* ✅ Model successfully learned patterns from financial data
* ✅ Feature engineering improved model performance
* ✅ Identified **credit score as the most influential feature**
* ✅ Built a complete ML pipeline from raw data → prediction

---

## 🧠 Key Insights

* Credit score plays a major role in loan approval
* Most features had low linear correlation → tree-based models could perform better
* Feature transformation (squared features) helps improve model learning

---

## 🛠️ Tech Stack

* Python 🐍
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* Jupyter Notebook

---

## ▶️ How to Run

1. Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/CreditWiseLoanSystem.git
```

2. Navigate to project:

```
cd CreditWiseLoanSystem
```

3. Install dependencies:

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Run notebook:

```
jupyter notebook
```

---

## 🔮 Future Improvements

* Use advanced models (Random Forest, XGBoost)
* Deploy as a web app (Flask / Streamlit)
* Add real-time loan prediction interface
* Improve dataset quality and size

---

## 🙋‍♀️ Author

**Anjali Gupta**

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
