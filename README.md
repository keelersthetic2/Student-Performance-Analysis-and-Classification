Student Performance Classification
-----------------
Predicting math outcomes using statistical tests and machine learning
-----------------
(Naive Bayes, LDA, Logistic Regression, Oversampling, Undersampling, Class Weights)
-----------------
PROJECT OVERVIEW
-----------------
This project analyzes the StudentsPerformance dataset to understand and predict student math performance.
It progresses through three major stages:

1. Exploratory Data Analysis (EDA)
2. Statistical tests and linear regression
3. Machine learning classification, including imbalanced-data techniques

The classification tasks are:

1. pass_math – whether a student passes math (score >= 60).
2. top_math – whether a student is in the top 10% of math scores (a rare class).

The work is inspired by concepts from “Practical Statistics for Data Scientists.”

SKILLS DEMONSTRATED
---------------------------------------------------------------------------------
- Exploratory data analysis
- Summary statistics, distributions, correlations, visualizations
- Two-sample t-tests
- Simple and multiple linear regression
- Residual diagnostics and VIF
- Gaussian Naive Bayes
- Linear Discriminant Analysis (LDA)
- Logistic Regression (coefficients, odds ratios, probability outputs)
- Confusion matrices and metric interpretation
- ROC curve and AUC evaluation
- Imbalanced classification (undersampling, oversampling, class weights)
- Probability distribution analysis

REPOSITORY STRUCTURE
---------------------------------------------------------------------------------
The project is organized into three notebooks:

01_exploratory_data_analysis.ipynb
EDA, score distributions, comparisons, correlations

02_statistical_tests_and_regression.ipynb
Gender Comparisons, two-sample t-tests, simple linear regression, multiple regression, VIF, model interpretation

03_classification.ipynb
Naive Bayes, LDA, Logistic Regression, ROC curves
Imbalanced classification using undersampling, oversampling, and class weights
Probability distribution analysis for model predictions

NOTEBOOK SUMMARIES
---------------------------------------------------------------------------------
01 – Exploratory Data Analysis

- Examines math, reading, and writing score distributions
- Computes correlations and basic insights
- Prepares the foundation for modeling

02 – Statistical Tests and Regression

- Performs two-sample t-tests comparing gender math scores
- Fits simple and multiple linear regression models
- Evaluates assumptions using residual plots
- Interprets model coefficients and VIF values

03 – Classification (Main Component)

Balanced Classification (pass_math)
Models trained:

- Gaussian Naive Bayes
- Linear Discriminant Analysis
- Logistic Regression

Evaluations include accuracy, precision, recall, confusion matrices, ROC curves, and AUC.
Logistic Regression achieved the strongest performance with AUC around 0.964.

Imbalanced Classification (top_math)

The dataset is about 10% top performers and 90% non-top performers, which causes high baseline accuracy but poor recall.

Techniques applied:

- Baseline logistic regression
- Random undersampling
- Random oversampling
- Logistic Regression with class_weight='balanced'

Results summary:

- Baseline model: poor recall for top students
- Undersampling: increased recall, small dataset, improved trade-off
- Oversampling: best overall performance (recall ~96%, AUC ~0.966)
- Class weights: higher recall but low precision

Exploring Predictions
Probability distributions were plotted for predicted probabilities of the top-performer class.
Oversampling produced the clearest separation between the two classes, consistent with the strong AUC score.

KEY FINDINGS
---------------------------------------------------------------------------------
- Logistic Regression is the strongest overall model for the balanced pass/fail task.
- LDA performs well but slightly behind Logistic Regression.
- Naive Bayes is acceptable but weaker due to independence assumptions.
- For rare-class prediction, accuracy is misleading; recall is the important metric.
- Oversampling provides the best trade-off for identifying top performers.
- Probability plots show strong separation between classes after balancing.

DATASET
---------------------------------------------------------------------------------
StudentsPerformance dataset (public Kaggle dataset)

FINAL NOTES
---------------------------------------------------------------------------------
This project demonstrates an end-to-end applied data science workflow:
EDA -> statistical reasoning -> regression -> classification -> imbalanced learning -> model interpretation.
