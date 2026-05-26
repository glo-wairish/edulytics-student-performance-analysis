# edulytics-student-performance-analysis
Schools and institutions struggle to identify factors affecting student performance early enough. Edulytics uses data analytics and visualization to uncover trends in attendance, grades, and engagement.
# Predictive Modeling of Student Academic Performance: A Comparative Study

## 🚀 Project Overview
Traditional academic assessments are largely reactive, identifying student performance risks only after final examinations have concluded. This project addresses this gap by leveraging **Educational Data Mining (EDM)** and machine learning to build a proactive predictive framework.

Using an educational dataset containing behavioral, demographic, and academic variables, this study develops, validates, and compares a traditional parametric model (**Multiple Linear Regression**) against an ensemble machine learning model (**Random Forest**). The core objective is to optimize predictive accuracy for student final grades ($G3$), establishing a data-driven foundation for institutional **Early Warning Systems (EWS)**.

---

## 📊 Key Results & Performance Summary
The models were trained on an 80/20 train-test split of the 649 student records. Multiple Linear Regression emerged as the superior model, capturing the linear nature of academic momentum with exceptional precision.

| Performance Metric | Random Forest Model | Multiple Linear Regression (Winner) |
| :--- | :---: | :---: |
| **R-Squared ($R^2$)** | 0.8509 (85.09%) | **0.8667 (86.67%)** |
| **Mean Absolute Error (MAE)** | 0.7551 | **0.7180** (~0.72 points error) |
| **Root Mean Squared Error (RMSE)** | 1.2600 | **1.1403** |

### 💡 Core Insights:
* **The Power of Momentum:** A student's second-period grade (G2) and first-period grade (G1) are the absolute strongest predictors of final success (G3).
* **Linear Edge:** Multiple Linear Regression outperformed Random Forest across all evaluation metrics, indicating that the academic features in this domain interact in a highly linear fashion. The final MLR model maintains an error margin of **only 3.6%** on a 20-point grading scale.

---

## 🎯 Objectives
* **Model Formulation:** Implement and fit a robust Multiple Linear Regression (MLR) framework and a non-parametric Random Forest (RF) regressor.
* **Statistical Rigor:** Perform thorough regression diagnostic checks to validate structural assumptions.
* **Feature Importance:** Analyze and rank demographic, behavioral, and academic features impacting final student outcomes.

---

## 🛠️ Tech Stack & Methodologies
* **Languages & Core Libraries:** Python, Pandas, NumPy, Scikit-Learn, Statsmodels, Matplotlib, Seaborn.
* **Feature Engineering:** One-Hot Encoding for categorical factors, tracking historical academic failures, and compounding social features (e.g., alcohol consumption indexes).
* **Statistical Methods:** Backward Elimination (p-value threshold < 0.05), Durbin-Watson Autocorrelation Testing, Multicollinearity Diagnosis (VIF analysis), Residual Normality Checks.

---

## 🔍 Feature Importance & Insights

### 1. Multiple Linear Regression (Refined via Backward Elimination)
Through systematic backward elimination, non-significant variables were dropped to yield a clean, interpretable, and production-ready linear equation heavily driven by:
* Mid-term Progression (G1 and G2 scores)
* Institutional Absenteeism (Total absences)
* Historical Academic Failures

### 2. Random Forest Node Splitting
The ensemble model confirmed statistical insights, heavily prioritizing the G2 score, aggregate absences, and $G1$ score across its decision tree splits, demonstrating that behavioral patterns and past performance heavily outweigh demographic factors.

---

## 💼 Strategic Recommendations for Educational Institutions
1. **Deploy Automated Early Warning Systems (EWS):** Integrate the MLR model into school management software to flag at-risk students immediately following mid-term (G1/G2) grading intervals.
2. **Dynamic Attendance Thresholds:** Establish automated administrative alerts when a student's absenteeism triggers coefficients modeled to impact final grading trends negatively.
3. **Targeted Academic & Psychological Support:** Allocate institutional remedial and counseling resources proactively to students identified with baseline histories of academic failure.

---

## 📂 How to Run the Project

1. Clone this repository:
   ```bash
   git clone [https://github.com/glo-wairish/student-performance-prediction.git](https://github.com/your-username/student-performance-prediction.git)
