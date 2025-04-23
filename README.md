## 🧑‍💼 IBM Employee Attrition Prediction
This project predicts employee attrition using classification models, helping HR professionals identify individuals at risk of leaving the company. The dataset is sourced from IBM HR Analytics.

1.Age | Age of the employee

2.Attrition | Whether the employee left the company (Yes/No)

3.BusinessTravel | Travel frequency

4.Department | Department 

5.DistanceFromHome | Commute distance

6.Education | Education level (1–5)

7.EducationField | Field of education

8.RelationshipSatisfaction | Satisfaction with personal relationships (1–4)

9.StockOptionLevel | Company stock option level

10.TotalWorkingYears | Total years of work experience

11.TrainingTimesLastYear | Number of training sessions in the last year

12.YearsAtCompany | Tenure in the company

13.YearsInCurrentRole | Time spent in current role

14.YearsSinceLastPromotion | Time since last promotion

15.YearsWithCurrManager | Years under current manager

**Target**: `Attrition` (0 = No, 1 = Yes)
**Type**: Binary Classification
**Imbalance**: Yes, with significantly fewer attrition cases
## 🧹 Preprocessing

- Encoded categorical features
- Scaled features using `MinMaxScaler`
- Addressed class imbalance using:
  - `class_weight='balanced'` or custom weights
  - `scale_pos_weight` for XGBoost

## 🤖 Models Trained & Evaluation

### 1️⃣ Logistic Regression
- Accuracy: 0.82
- ROC AUC: **0.82**
- Recall (Attrition): 0.13
- F1 Score (Attrition): 0.19

### 2️⃣ XGBoost Classifier

- Accuracy: 0.83
- ROC AUC: 0.73
- Recall (Attrition): 0.24
- F1 Score (Attrition): 0.31

### 3️⃣ K-Nearest Neighbors (K=3)

- Accuracy: 0.83
- ROC AUC: 0.57
- Recall (Attrition): 0.14
- F1 Score (Attrition): 0.21
### 4️⃣ Random Forest (Tuned)

- Accuracy: 0.79
- ROC AUC: 0.743
- Recall (Attrition): **0.56**
- F1 Score (Attrition): **0.49**
