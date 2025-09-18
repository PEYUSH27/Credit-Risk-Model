# Credit-Risk-Model

Credit Risk Prediction using Logistic Regression
This repository contains a credit risk prediction model built using logistic regression, aimed at classifying loan defaults based on borrower and loan characteristics.

Overview
The project uses a loan dataset to build a logistic regression model that predicts the probability of a borrower defaulting on a loan. The notebook contains the entire workflow from data preprocessing to model training, evaluation, and prediction on a new dataset.

Dataset
Loan_default.csv: This dataset contains borrower information and loan details including features such as Age, Income, LoanAmount, CreditScore, MonthsEmployed, InterestRate, and more. The target variable is Default indicating whether the loan was defaulted on or not.

Pred123.xlsx: This is a new dataset on which predictions for loan default probabilities are made using the trained model.

Key Steps in the Notebook
1-Data Loading and Cleaning

2-LoanID column is dropped as it is not useful for modeling.

3-Missing values are handled by dropping rows with nulls in key features.

4-Feature Encoding and Scaling

5-Categorical features are label encoded for model compatibility.

6-Features are standardized using StandardScaler to improve model performance.

7-Feature Selection

8-L1 penalty logistic regression is used for selecting important features by penalizing non-important ones.

9-The model is trained using only the selected important features.

10-Model Training and Evaluation

11-Train-test split with 70:30 ratio is applied.

12-Logistic Regression model is trained on the training set.

13-Model is evaluated with classification report and confusion matrix.

14-Overall model accuracy is around 88.7%. Precision, recall, and F1-score metrics are inspected, noting class imbalance effects.

15-Model Interpretation

16-Logistic regression coefficients and intercept are extracted to formulate the logistic regression equation indicating the relationship between input features and default probability.

17-Statistical summary of model including p-values for coefficients is generated via statsmodels.Logit.

18-Prediction on New Data

The new dataset (Pred123.xlsx) is processed similarly (encoding and scaling).

The model predicts the default probability and class for each new entry.

A visualization of predicted default probabilities is shown for insight.

Usage
Run the Python notebook (Credit_Risk_Model_-LR.ipynb) to replicate the analysis.

Update the file paths to your local environment if necessary.

Use the trained model to predict default probabilities for new loan applications and support credit risk assessment.

Dependencies
Python libraries: pandas, scikit-learn, seaborn, matplotlib, statsmodels
