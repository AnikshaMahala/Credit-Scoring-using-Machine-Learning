# Credit-Scoring-using-Machine-Learning

## Project Overview

This project aims to develop a credit scoring model using machine learning to predict the likelihood of loan repayment. By automating and improving the risk assessment process, the project enables financial institutions to make data-driven decisions on loan approvals, enhancing efficiency and reducing default risks.

## Problem Statement

Credit scoring is a systematic approach to evaluate the creditworthiness of individuals or businesses applying for financial products such as loans or credit cards. It considers factors like credit history, payment behavior, outstanding debts, and financial stability. This project focuses on creating a predictive model to aid in this process by estimating loan repayment likelihood.

## Motivation

- Predictive credit scoring provides financial institutions with the ability to:

 - Streamline decision-making processes.

 - Quantify borrower risk efficiently.

 - Provide data-driven loan approval or denial decisions.

 - A higher credit score suggests lower credit risk, increasing the likelihood of securing favorable loan terms. Conversely, a lower score might lead to higher interest rates or credit denial.

## Dataset Description

- The dataset contains:

 - 39,717 records of loan applications.

 - 111 columns covering financial metrics, credit history indicators, loan status, and borrower details.

 - Target variable: Loan Status, categorized as Fully Paid, Charged Off, or Default.

## Methodology

1. Data Preprocessing

- 1.1 Exploratory Data Analysis (EDA)

  - Focused on the Loan Status target variable.

  - Filtered dataset to retain relevant statuses and created a binary classification target: Late Loan (repaid or not).

- 1.2 Data Cleaning

  - Dropped columns with more than 10% missing values.

  - Replaced missing values in remaining columns with their median.

- 1.3 Feature Engineering

  - Binning: Grouped continuous and categorical variables to establish a monotonic relationship with the target.

  - Weight of Evidence (WOE) transformations: Converted feature values into WOE scores.

  - Calculated Information Value (IV) to quantify predictive strength.

  - Enhanced feature interpretability and alignment with risk patterns.

2. Model Development

- 2.1 Logistic Regression

  - Primary model used for predicting loan default likelihood.

  - Selected features like income and loan grade, applying WOE-transformed data.

- 2.2 Decision Tree Classifier

  - Used as a baseline for comparison with logistic regression.

3. Model Evaluation

  - Performance metrics: ROC curve, classification report.

  - Logistic regression achieved 86% accuracy, excelling in precision and recall for the majority class.

## Results

- The logistic regression model outperformed the decision tree classifier.

- The model struggled with minority class (Class 1) due to data skewness.


## Requirements

 - Python 3.x

 - Libraries: pandas, numpy, matplotlib, scikit-learn, statsmodels

## Future Work

- Explore additional models like Random Forest or Gradient Boosting.

- Deploy the model into a real-world application for live credit scoring.

- Integrate external datasets to enrich feature space and improve accuracy.
