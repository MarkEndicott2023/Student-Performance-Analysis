# Student Performance Analysis

CMSE 381 project predicting student exam scores (regression) and school type (classification) from survey-style academic and lifestyle features.

## Data

`student_performance_factors.csv` — 6,607 student records, 19 features, target `Exam_Score`.

- **Numeric (6):** Hours_Studied, Attendance, Sleep_Hours, Previous_Scores, Tutoring_Sessions, Physical_Activity
- **Categorical (13):** Parental_Involvement, Access_to_Resources, Extracurricular_Activities, Motivation_Level, Internet_Access, Family_Income, Teacher_Quality, School_Type, Peer_Influence, Learning_Disabilities, Parental_Education_Level, Distance_from_Home, Gender

## Models

**Regression (target: Exam_Score)** — metrics on full fit

| Model | R² | RMSE | MAE |
|---|---|---|---|
| OLS (numeric features) | 0.598 | 2.466 | 1.312 |
| LassoCV (numeric features) | 0.598 | 2.466 | 1.313 |
| LassoCV + degree-2 polynomial features | 0.764 | 1.825 | — |

**Classification (target: School_Type)**

| Model | Accuracy |
|---|---|
| Perceptron | 0.643 (test) |
| Random Forest (stratified 5-fold CV) | 0.670 |
| Logistic Regression, L1 penalty (LogisticRegressionCV) | 0.500 (test) |

## Notebooks

- [tinkering_mark.ipynb](tinkering_mark.ipynb) — OLS, Lasso, Perceptron, Random Forest
- [tinkering_mason.ipynb](tinkering_mason.ipynb) — Polynomial Lasso regression, L1 logistic classification
- [project_template.ipynb](project_template.ipynb) — project structure template
