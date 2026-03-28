# Student Performance Analysis

Predicting student exam scores using regression and classification models.

## Data

`student_performance_factors.csv` — 6,607 student records, 20 features, 1 target variable (`Exam_Score`).

**Numeric features:** Hours_Studied, Attendance, Sleep_Hours, Previous_Scores, Tutoring_Sessions, Physical_Activity

**Categorical features:** Parental_Involvement, Access_to_Resources, Extracurricular_Activities, Motivation_Level, Internet_Access, Family_Income, Teacher_Quality, School_Type, Peer_Influence, Learning_Disabilities, Parental_Education_Level, Distance_from_Home, Gender

## Models

- **OLS Regression** — baseline, R² = 0.598
- **Lasso Regression** — L1 regularization for feature selection
- **Lasso + Polynomial Features** — degree-2 interactions, R² = 0.764
- **Perceptron** — linear classifier for School Type prediction
- **Random Forest** — ensemble classifier with stratified k-fold CV

## Notebooks

- `tinkering_mark.ipynb` — OLS, Lasso, Perceptron, Random Forest
- `tinkering_mason.ipynb` — Polynomial feature engineering + Lasso regression
- `project_template.ipynb` — Project structure template

