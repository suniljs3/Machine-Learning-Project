# Machine-Learning-Project
For each dataset complete the following tasks: Data Cleaning, Summarization, visualisation, Co-Rel Analysis, Hypothesis testing and then apply the appropriate Machine Learning techniques.

Dataset: IBM HR Analytics Employee Attrition & Performance 

Dataset link : https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

1) What are the key factors driving employee attrition?
2) Is job satisfaction significantly different between employees who leave and those who stay?
3) Can we predict attrition using job role, salary, and work-life balance?
4) Do longer working hours increase attrition risk?
5) Which features are most important for predicting attrition?

1. What are the key factors driving employee attrition?
Approach:

Use Exploratory Data Analysis (EDA) to compare features (e.g., Age, JobRole, MonthlyIncome, Overtime, WorkLifeBalance) by Attrition.

Use correlation heatmaps, grouped statistics, and boxplots.

Train a classification model (e.g., Random Forest, Logistic Regression) and extract feature importances.

Key metrics to explore:

Overtime

DistanceFromHome

EnvironmentSatisfaction

JobSatisfaction

MonthlyIncome

JobInvolvement

WorkLifeBalance

TotalWorkingYears

2. Is job satisfaction significantly different between employees who leave and those who stay?
Approach:

Use a t-test or Mann-Whitney U test to compare JobSatisfaction scores between:

Attrition = Yes and Attrition = No

Visualization:

Boxplot or violin plot of JobSatisfaction grouped by Attrition.

3. Can we predict attrition using job role, salary, and work-life balance?
Approach:

Build a classification model (e.g., Logistic Regression, Random Forest, XGBoost) using:

JobRole (categorical → one-hot encoding)

MonthlyIncome (numerical)

WorkLifeBalance (ordinal)

Evaluation Metrics:

Accuracy, Precision, Recall, F1-score

ROC-AUC Curve

4. Do longer working hours increase attrition risk?
Approach:

Analyze Attrition vs AverageDailyHours or OverTime (use OverTime and maybe compute hours from DailyRate if needed).

Use statistical tests or logistic regression with Attrition ~ OverTime + HoursPerWeek.

Visualization:

Histograms or boxplots of TotalWorkingYears, OverTime, or any proxy for working hours vs. Attrition.

5. Which features are most important for predicting attrition?
Approach:

Train tree-based models (e.g., Random Forest, XGBoost).

Use .feature_importances_ or SHAP (SHapley Additive exPlanations) values to interpret.

Top likely features:

OverTime

MonthlyIncome

JobLevel

JobRole

Age

EnvironmentSatisfaction

WorkLifeBalance
