# Loan Approval Prediction
## Exploratory Data Analysis and Machine Learning-Based Loan Approval Prediction

**KPR Institute of Engineering and Technology**  
**Department:** Artificial Intelligence and Data Science

### Student Details
- **Student Name:** Bhavansri M
- **Roll Number:** 24AD017
- **Course Code:** U21ADP05
- **Assignment:** Exploratory Data Analysis
- **Submission Date:** 15 October 2026

## Abstract
This project explores a loan approval dataset and develops a machine learning classification model to predict loan approval status. Python, Pandas, NumPy, Matplotlib, Seaborn and Scikit-learn are used for data analysis, preprocessing, visualization and model evaluation. The analysis examines applicant age, annual income, loan amount, interest rate, loan purpose, home ownership and credit history. A classification model achieved approximately **94.57% accuracy** and a **ROC-AUC of 0.9290** on the test dataset.

## 1. Introduction and Objectives
Loan approval decisions depend on several factors, including applicant income, credit history, loan amount and financial obligations. Exploratory Data Analysis (EDA) helps identify patterns and relationships in these factors before developing a prediction model.

### Objectives
- Understand the dataset and its features.
- Examine missing values, duplicates and data types.
- Analyze the distribution of loan approval status.
- Visualize relationships between applicant characteristics and loan approval.
- Train and evaluate a machine learning classification model.
- Interpret results and discuss limitations.

## 2. Dataset Description
The dataset contains **58,645 rows and 13 columns**.

The target variable is `loan_status`:
- `0` — Loan not approved
- `1` — Loan approved

The dataset contains applicant and loan-related features such as age, income, home ownership, employment length, loan intent, loan grade, loan amount, interest rate, loan-to-income percentage, previous default information and credit history length.

## 3. EDA and Preprocessing
The dataset was loaded and inspected using Pandas. Column data types, descriptive statistics, missing values and duplicate records were examined.

The dataset contained **no missing values and no duplicate rows** in the inspected version. The target distribution was imbalanced, with 50,295 records in class 0 and 8,350 records in class 1.

Categorical and numerical features were prepared for machine learning using a preprocessing pipeline. The data was split into training and testing sets, and preprocessing was fitted using training data.

## 4. Data Visualizations and Interpretations

### 4.1 Loan Amount Distribution
The loan amount distribution is right-skewed, with most applicants requesting comparatively smaller loans and fewer applicants requesting very large amounts.

### 4.2 Applicant Age Distribution
Most applicants are concentrated in the younger adult age groups. A small number of unusually high age values should be investigated before drawing conclusions.

### 4.3 Loan Approval Status Distribution
The dataset contains substantially more records with loan status 0 than status 1. This class imbalance is important when interpreting accuracy, precision and recall.

### 4.4 Correlation Heatmap
The heatmap shows relationships between numerical features. Loan interest rate and loan-to-income percentage have positive correlations with the target in the observed dataset, while annual income has a negative correlation. Correlation does not establish causation.

### 4.5 Annual Income vs Loan Amount
The scatter plot shows how loan amounts vary across annual income levels. The observations are widely distributed, suggesting that income alone does not explain loan amount or approval status.

### 4.6 Loan Status by Loan Intent
Approval outcomes vary across loan purposes. These differences are descriptive and do not prove that loan intent alone determines approval.

### 4.7 Loan Status by Home Ownership
The distribution of loan outcomes varies across home-ownership categories. These patterns should be interpreted alongside other applicant characteristics.

## 5. Model Evaluation and Results

The trained classification model was evaluated on the held-out test dataset.

| Metric | Test Result |
|---|---:|
| Accuracy | 94.57% |
| Precision | 92.16% |
| Recall | 67.66% |
| F1-score | 78.00% |
| ROC-AUC | 0.9290 |

### 5.1 Confusion Matrix
The confusion matrix contains:
- True negatives: 9,963
- False positives: 96
- False negatives: 541
- True positives: 1,129

The model correctly identifies many non-approved applications, but it misses some approved applications. The recall score indicates that there is room to improve the identification of class 1.

### 5.2 ROC Curve
The ROC-AUC of approximately 0.929 indicates strong ability to distinguish between the two target classes across classification thresholds. It does not mean that 92.9% of all predictions are correct.

### 5.3 Neural Network Training
The neural network validation accuracy reached approximately 94.9% at its highest observed point. Training loss decreased over the iterations, while validation accuracy fluctuated slightly. The selected model's final test metrics should be used when reporting its generalization performance.

## 6. Conclusion and Future Scope
This project used EDA, data visualization and machine learning to study loan approval status. The model achieved 94.57% test accuracy and a ROC-AUC of 0.9290. However, the recall of 67.66% shows that some positive-class cases are missed.

Future work could compare multiple classification algorithms, investigate class imbalance, tune classification thresholds and evaluate fairness across applicant groups. Predictions should support, not replace, responsible human review of loan applications.

## 7. Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Google Colab
- GitHub

## 8. References
1. Kaggle — Loan Approval Prediction dataset used in this project.
2. Pandas documentation — https://pandas.pydata.org/docs/
3. Scikit-learn documentation — https://scikit-learn.org/stable/
4. Matplotlib documentation — https://matplotlib.org/stable/
5. Seaborn documentation — https://seaborn.pydata.org/

## 9. Project Files
- `loan approval prediction.pdf` — Complete EDA project report.
- `README.md` — Project overview, analysis, and results.

**Note:** The model results reported above are based on the results recorded during this project's analysis. This project is for academic purposes and should not be used as the sole basis for real loan decisions.
