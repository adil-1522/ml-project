# Customer Churn Prediction with Segmentation and Retention Analysis

## 📌 Project Overview
This project focuses on predicting customer churn in a telecom dataset using machine learning and extending the analysis with customer segmentation and retention insights. The goal is to identify churn-prone customers and understand behavioral patterns that drive churn.

This project demonstrates both **supervised and unsupervised learning**, making it an intermediate-level data science project.

---

## 🎯 Problem Statement
Customer churn is a critical challenge in the telecom industry. Retaining existing customers is more cost-effective than acquiring new ones.

**Objectives:**
- Predict whether a customer is likely to churn
- Identify key behavioral drivers of churn
- Segment customers based on usage and service behavior
- Analyze retention risk across customer segments

---

## 📊 Dataset Description
The dataset contains customer-level information such as:
- Usage metrics (DayMins, DataUsage, RoamMins)
- Billing information (MonthlyCharge)
- Customer service interactions (CustServCalls)
- Customer tenure (AccountWeeks)

Target variable:
- **Churn** (1 = churned, 0 = not churned)

---

## 🔍 Exploratory Data Analysis (EDA)
Key insights from EDA:
- Dataset is class-imbalanced
- Customers with frequent service calls churn more
- Usage and billing patterns differ significantly between churned and non-churned customers

---

## 🛠 Feature Engineering
A new feature was engineered:
- **ChargesPerMin** = MonthlyCharge / DayMins

This feature captures perceived pricing efficiency and improved model performance.

---

## 🤖 Model Building (Supervised Learning)
Models trained:
- Logistic Regression (baseline)
- Random Forest
- XGBoost (final model)

Due to class imbalance, evaluation focused on:
- Recall
- F1-score
- ROC-AUC

**Final XGBoost Performance:**
- ROC-AUC ≈ **0.86**
- High recall for churn class

---

## 📈 Model Interpretation
Feature importance analysis revealed that:
- DayMins
- CustServCalls
- MonthlyCharge
- ChargesPerMin

are the most influential factors in predicting churn.

---

## 🧩 Customer Segmentation (Unsupervised Learning)
Customer segmentation was performed using **KMeans clustering**.

Steps followed:
- Selected behavioral features (excluding churn)
- Applied feature scaling
- Used the Elbow Method to select **5 clusters**
- Profiled and interpreted each segment

---

## 🔄 Retention Analysis
Retention analysis was conducted using:
- Historical churn rate per segment
- Predicted churn probability from XGBoost

Key findings:
- Customers with frequent service calls have the highest churn risk
- Highly inactive customers show the highest predicted churn probability
- Low usage alone does not necessarily indicate churn

---

## 🏁 Conclusion
This project demonstrates an end-to-end data science workflow, combining churn prediction with customer segmentation and retention analysis. By integrating supervised and unsupervised learning, the project provides deeper insights into customer behavior and churn risk.

---

## 🚀 Future Work
- Apply SHAP for model explainability
- Experiment with alternative clustering techniques
- Deploy the model as a web application

---

## 🧑‍💻 Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib
