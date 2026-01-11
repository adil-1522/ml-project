# Titanic Survival Prediction 🚢

## 📌 Project Overview
This project predicts whether a passenger survived the Titanic disaster using machine learning.  
It demonstrates an end‑to‑end workflow: data cleaning, preprocessing, model training, evaluation, and insights.

## 📂 Dataset
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/datasets/elyamadad/titanic-dataset)
- Columns include passenger class, sex, age, siblings/spouses, parents/children, fare, cabin, and embarkation port.

## ⚙️ Steps
1. **Data Cleaning**
   - Filled missing `Age` values with median.
   - Filled missing `Embarked` values with most frequent category.
   - Dropped `Cabin` (too many missing values).
2. **Feature Engineering**
   - One‑hot encoded categorical features (`Sex`, `Embarked`).
   - Scaled numeric features (`Age`, `Fare`, etc.).
3. **Modeling**
   - Baseline: Logistic Regression.
   - Improved: Random Forest Classifier.
4. **Evaluation**
   - Compared accuracy, precision, recall, and F1‑score.
   - Random Forest performed better than Logistic Regression.
5. **Insights**
   - Key features influencing survival: `Sex`, `Pclass`, `Fare`, `Age`.

## 📊 Results
- Logistic Regression Accuracy: ~78%
- Random Forest Accuracy: ~82%
- Random Forest captured nonlinear relationships and gave better performance.

## 🚀 How to Run
1. Clone this repo:
   ```bash
   git clone https://github.com/adil-1522/ml-project.git
