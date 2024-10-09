# Loan Eligibility Prediction

## Overview

This project aims to predict the eligibility of loan applicants based on various features such as income, education, employment status, and credit history. It uses machine learning models to classify applicants as either eligible or ineligible for loans. The dataset consists of information on 614 loan applicants and includes missing values that were handled during the preprocessing stage.

## Features of the Dataset

- **Loan_ID**: Unique Loan Identifier
- **Gender**: Male/Female
- **Married**: Applicant's marital status
- **Dependents**: Number of dependents
- **Education**: Applicant's education level (Graduate/Not Graduate)
- **Self_Employed**: Whether the applicant is self-employed
- **ApplicantIncome**: Applicant's income
- **CoapplicantIncome**: Co-applicant's income
- **LoanAmount**: Loan amount requested
- **Loan_Amount_Term**: Term of loan in months
- **Credit_History**: Whether the applicant has a credit history (1 for Yes, 0 for No)
- **Property_Area**: Urban, Rural, or Semiurban
- **Loan_Status**: Whether the loan was approved or not (Y/N)

## Libraries Used

- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations
- **matplotlib**: Data visualization
- **sklearn**: Machine learning models (Decision Tree, Naive Bayes)
- **StandardScaler**: Data normalization
- **LabelEncoder**: Encoding categorical variables

## Data Preprocessing

- Handled missing values in columns such as `Gender`, `Married`, `Dependents`, `Self_Employed`, and `LoanAmount` by filling them with appropriate statistical measures (mode or mean).
- Created new features `TotalIncome` and `TotalIncome_log` to combine applicant and co-applicant incomes for better model performance.
- Normalized features using `StandardScaler`.

## Model Building

Two models were used to predict loan eligibility:

1. **Decision Tree Classifier**
   - Accuracy: 69.92%
2. **Naive Bayes Classifier**
   - Accuracy: 81.30%

## Results

The Naive Bayes classifier outperformed the Decision Tree in predicting loan eligibility, with an accuracy of 81.3%. Further improvements could involve tuning the models, handling class imbalance, and testing other machine learning algorithms.

## How to Use

1. Clone this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib scikit-learn
