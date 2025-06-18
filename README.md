# Flu Vaccination Predictor Project 🧬💉

## 🚀 Overview

This project aims to **predict flu vaccination uptake** (both H1N1 and seasonal flu) using data from the **CDC 2009 H1N1 Flu Survey**. By leveraging **machine learning models**, we explore key factors that influence whether individuals decide to get vaccinated — offering insights to shape public health strategy.

Developed as part of the **ReDI-School of Digital Integration Course - Data Circle Fall 2025 in Hamburg** by **ALPHA GROUP**:
- Assimagbe Albert Raphael
- Saad Ali

---

## 🎯 Objectives

- Analyze public behaviors and attitudes toward vaccination
- Predict uptake of:
  - 🦠 **H1N1 vaccine**
  - ❄️ **Seasonal flu vaccine**
- Interpret model outputs to find influencing factors
- Provide actionable recommendations for healthcare communication and intervention

---

## 📊 Dataset

- **Source**: CDC 2009 H1N1 Flu Survey (U.S.)
- **Size**: 26,707 respondents
- **Features**: 36 variables including:
  - 🧑 Demographics (age, race, education)
  - 🏥 Health behavior (doctor visits, chronic illness)
  - 💭 Opinions (concerns, beliefs, vaccine confidence)
- **Targets**:
  - `h1n1_vaccine` (Yes/No)
  - `seasonal_vaccine` (Yes/No)

---

## 🔍 Exploratory Data Analysis (EDA)

- **Older adults (65+)** more likely to receive seasonal flu vaccines
- **Doctor recommendations** heavily influence vaccination decisions
- Low uptake for H1N1 compared to seasonal flu
- Behavioral patterns like handwashing and chronic condition prevalence analyzed

---

## 🧹 Data Preprocessing

- Removed columns with excessive missing values
- Imputed missing values using **mode/median**
- Categorical variables encoded using **Label Encoding**
- Created **interaction features**:
  - Age × Health Worker
  - Income × Doctor Recommendation
  - Education × Opinion on Vaccine
- Applied **StandardScaler** for numeric values
- Dropped low-variance features to reduce noise

---

## 🤖 Modeling Approach

Separate models trained for:
- H1N1 vaccine prediction
- Seasonal flu vaccine prediction

### Models Tested:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- AdaBoost
- k-Nearest Neighbors (k-NN)

### Evaluation Metrics:
- Accuracy
- F1 Score
- ROC AUC
- Training time
- Memory efficiency

---

## 📈 Model Performance

### H1N1 Vaccine (Best: Random Forest)
- **Accuracy**: 84%
- **ROC AUC**: 0.83
- **F1 Score**: 0.52

### Seasonal Vaccine (Best: Gradient Boosting)
- **Accuracy**: 78%
- **ROC AUC**: 0.85
- **F1 Score**: 0.76

---

## 💡 Key Findings

- **Doctor’s recommendation** is the most influential feature
- **Belief in vaccine effectiveness** and **risk perception** drive vaccination
- **Demographics alone** have limited predictive power
- **SHAP analysis** and **Logistic Regression coefficients** both highlight:
  - Vaccine confidence
  - Medical advice
  - Opinions and access over pure demographics

---

## 📌 Recommendations

### 📢 Public Health
- Strengthen vaccination campaigns with **evidence-based messaging**
- Target:
  - **Young adults**
  - **Uninsured populations**
  - **Low-trust groups**
- Empower healthcare workers to advocate during patient visits

### 🛠 Technical
- **Deploy Random Forest** for balance between performance and interpretability
- Use **Logistic Regression** for dashboards and explainability
- Future work:
  - Add time-based trend analysis
  - Explore deep learning models for fine-grained prediction

---


