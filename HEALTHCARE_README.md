# 🏥 Healthcare Risk Scoring & Diabetes Prediction

## 📌 Project Overview
This project analyzes patient health data to **predict diabetes risk** and provide **explainable insights** that can help doctors and healthcare providers make informed decisions.

Using machine learning models (Logistic Regression and Random Forest), the project:
- Predicts whether a patient is diabetic or not
- Generates a **risk score (probability)**
- Groups patients into **Low, Moderate, High, and Very High risk buckets**
- Explains predictions using **SHAP (Explainable AI)**

---

## 🎯 Problem Statement
Early detection of diabetes is critical in healthcare.  
Traditional diagnosis relies on manual analysis of medical parameters, which can be time-consuming and inconsistent.

**Goal:**  
Build a data-driven system that:
- Identifies high-risk patients early
- Explains *why* a patient is high risk
- Helps prioritize medical attention

---

## 📊 Dataset
**Pima Indians Diabetes Dataset**

- Records: 768 patients
- Target variable: `Outcome`
  - `0` → Non-diabetic
  - `1` → Diabetic

### Features:
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

📌 Note: Some medical values are recorded as `0`, which represent missing measurements and are handled during preprocessing.

---

## 🛠️ Technologies Used
- **Python**
- **Pandas, NumPy** – Data handling
- **Matplotlib, Seaborn** – Visualization
- **Scikit-learn** – Machine Learning
- **SHAP** – Model Explainability
- **Joblib** – Model saving

---

## 🔍 Project Workflow

1. **Data Loading & Exploration**
   - Basic statistics
   - Distribution plots
   - Correlation analysis

2. **Data Cleaning**
   - Replaced invalid zero values with median
   - Feature scaling using `StandardScaler`

3. **Feature Engineering**
   - Age groups
   - BMI categories
   - One-hot encoding

4. **Model Training**
   - Logistic Regression (baseline, interpretable)
   - Random Forest (higher accuracy)

5. **Model Evaluation**
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - ROC-AUC
   - Confusion Matrix

6. **Risk Scoring**
   - Converted prediction probabilities into risk scores
   - Created risk buckets:
     - Low
     - Moderate
     - High
     - Very High

7. **Explainability (SHAP)**
   - Global feature importance
   - Individual patient-level explanations

---

## 📈 Key Insights
- **Glucose** is the strongest predictor of diabetes
- Higher **BMI** significantly increases risk
- Diabetes risk increases with **age**
- Very High risk group contains the majority of actual diabetic patients
- SHAP analysis confirms clinical relevance of features

---

## 🩺 Business & Healthcare Impact
- Helps doctors **prioritize high-risk patients**
- Improves transparency in ML predictions
- Can assist in early intervention and preventive care
- Supports data-driven decision-making in hospitals

---

## ▶️ How to Run the Project

### 1. Clone the repository
```bash
git clone <repository-url>
cd healthcare-risk-scoring
