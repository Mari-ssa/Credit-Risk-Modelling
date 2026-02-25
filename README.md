# Credit Risk Modeling – Loan Approval Prediction

## Project Overview
This project focuses on building and evaluating machine learning models for **credit risk assessment**, specifically predicting whether a loan application will be **approved or rejected**. 

---

## Dataset
- **Source:** Kaggle – Loan Approval Prediction Dataset  
- **Description:** The dataset contains applicant demographics, financial information, loan details, and credit history.
- **Target Variable:**  
  - `loan_status`  
    - `1` → Approved  
    - `0` → Rejected  

---

## Exploratory Data Analysis (EDA)
Key observations from exploratory analysis include:
- Credit score (CIBIL score) strongly differentiates approved and rejected loans.
- Income and loan amount individually show significant overlap between approval outcomes.
- Ratio-based features such as loan-to-income provide better insight into repayment risk.
- Longer loan terms tend to be associated with higher rejection rates, although overlap exists.

---

## 🛠 Feature Engineering & Preprocessing
- Cleaned and standardized column names.
- Converted categorical variables into numerical format.
- Created a **loan-to-income ratio** to measure repayment burden.
- Applied **feature scaling (StandardScaler)** to normalize input variables.
- Removed non-informative identifiers such as loan ID.
- Used **stratified train–test split** to preserve class distribution.

---

##  Models Implemented

### Logistic Regression
- Used as a baseline model due to its interpretability and common use in credit risk.
- Predicted probabilities were leveraged to apply **custom decision thresholds**.
- Increasing the threshold improved precision and reduced false approvals, demonstrating risk-sensitive decision making.

### Decision Tree Classifier
- Implemented to capture non-linear relationships between features.
- Tree depth was restricted to prevent overfitting.
- Achieved very high accuracy, precision, and recall.
- Threshold tuning had minimal impact due to confident, rule-based predictions.

---

## Model Evaluation
Models were evaluated using:
- Accuracy
- Precision (Approved Loans)
- Recall (Rejected Loans)
- Confusion Matrices

Key insights:
- Logistic regression benefited significantly from threshold tuning.
- Decision Tree showed superior overall performance and stability.
- Precision and recall were prioritized over accuracy to reflect real-world credit risk considerations.

---

## Key Learnings
- Accuracy alone is insufficient for evaluating credit risk models.
- Precision is critical to avoid approving high-risk applicants.
- Recall for rejected loans ensures risky cases are not missed.
- Threshold tuning allows alignment of models with business risk tolerance.
- Model selection involves a trade-off between interpretability and predictive power.

---

## Future Improvements
- Implement ensemble models such as Random Forest or XGBoost.
- Apply cross-validation for more robust evaluation.
- Introduce cost-sensitive learning to model financial loss explicitly.
- Add explainability techniques such as feature importance or SHAP values.

---

## Technologies Used
- Python  
- NumPy, Pandas  
- Matplotlib  
- Scikit-learn  

---

## Author
**Marissa Arul Michael Varghese**  
Credit Risk Modeling Project 
