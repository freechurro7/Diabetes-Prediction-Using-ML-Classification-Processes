# Diabetes-Prediction-Using-ML-Classification-Processes
This project applies machine learning classification techniques to predict the likelihood of diabetes in female patients based on diagnostic measurements from the Pima Indians Diabetes Dataset. The goal is to identify high-risk individuals by training models on medical features like glucose level, BMI, insulin levels, and more.

# Scope of the Problem

Diabetes is a serious, chronic condition affecting over 589 million people worldwide, with numbers expected to reach 853 million by 2050. Alarmingly, 4 in 10 diabetics remain undiagnosed, and millions die annually due to diabetes-related complications. This capstone project explores the power of machine learning to aid early detection of diabetes using patient health data.

# Summary
By building a predictive model on the Pima Indians Diabetes Dataset, we aim to identify high-risk individuals before the disease progresses, enabling timely intervention and improved health outcomes.

# Objectives
1. To explore and clean real-world health data for diabetes diagnosis.
2. To identify key health features that influence diabetes risk.
3. To build and compare ML classification models for diabetes prediction.
4. To translate findings into practical screening recommendations.

# Dataset Description

| Feature                  | Description                      |
| ------------------------ | -------------------------------- |
| Pregnancies              | Number of pregnancies            |
| Glucose                  | Plasma glucose concentration     |
| BloodPressure            | Diastolic blood pressure (mmHg)  |
| SkinThickness            | Triceps skin fold thickness (mm) |
| Insulin                  | Serum insulin level (μU/mL)      |
| BMI                      | Body mass index (kg/m²)          |
| DiabetesPedigreeFunction | Family history risk score        |
| Age                      | Patient age                      |
| Outcome                  | 1 = Diabetic, 0 = Non-diabetic   |

# Key Findings:

1. The dataset is slightly unbalanced (more non-diabetics).
2. Glucose, BMI, and Age are strong indicators of diabetes.
3. Patients aged 40 and above, and those with high glucose and BMI, have a higher probability of diabetes.
4. Those with multiple pregnancies showed increased risk, potentially indicating gestational diabetes.
5. Many records contain zero values for medical attributes like Glucose and Insulin, which were treated as missing data and imputed appropriately.

## Risk Factor Scoring

Developed a simple risk score based on common thresholds:
Glucose ≥ 140 → +1, BMI ≥ 30 → +1, Age ≥ 40 → +1, Insulin ≥ 150 → +1, and Pregnancies ≥ 3 → +1
A higher total score reflects a greater likelihood of diabetes.

# Machine Learning

Trained and evaluated several ML classification models: Logistic Regression, Decision Tree Classifier, Random Forest (Hypertuned with RandomizedSearchCV) and XGBoost

## Model Evaluation

| Metric                   | Score |
| ------------------------ | ----- |
| Accuracy                 | \~78% |
| Precision (diabetes = 1) | 66%   |
| Recall (diabetes = 1)    | 69%   |
| F1 Score                 | 0.67  |
| AUC Score                | High  |

## Confusion Matrix Example

|             | Predicted: No | Predicted: Yes |
| ----------- | ------------- | -------------- |
| Actual: No  | 79 (TN)       | 20 (FP)        |
| Actual: Yes | 17 (FN)       | 38 (TP)        |

# Real-World Prediction: Case Example

Patient Anaya: Age: 43, Pregnancies: 2, Glucose: 130 mg/dL, BMI: 35, Insulin: 128, Pedigree Function: 0.82

Model Output:
→ 83% probability of diabetes (Predicted as diabetic)

# Recommendations
Based on the analysis and model results:

1. Regular glucose monitoring is essential, especially for individuals with high BMI and glucose levels.

2. Early screening should be prioritized for people over 40, the obese, and those with multiple pregnancies.

3. Screening for gestational diabetes should occur during weeks 24–28 of pregnancy and earlier for high-risk women.

4. Public health campaigns should emphasize early diagnosis and prevention.

# Medium Article
https://medium.com/@agbaoyeadedeji78/diabetes-prediction-using-machine-learning-classification-approaches-a-capstone-project-by-team-cbd0b784a30b

