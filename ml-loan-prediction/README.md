# Loan Acceptance Prediction: Decision Tree Modeling and Optimization

**Course:** MSSP 6080 — Practical Machine Learning, University of Pennsylvania (SP2)
**Author:** Liqi Liang | Fall 2024

## Overview

This project builds and iteratively optimizes a binary classifier to predict whether a LendingClub loan application will be accepted. Using 81,103 applications, I establish a baseline decision tree and systematically explore five optimization strategies.

## Dataset
LendingClub loan applications. Target: `policy_code` (1 = Accepted, 0 = Rejected). Class imbalance: 88.6% rejected.

## Methods
- Baseline: Decision Tree (entropy criterion) with 4 financial features
- Optimization experiments: feature engineering (region dummies, debt indicator), training set size, feature subset selection, Decision Tree vs. Logistic Regression, GridSearchCV hyperparameter tuning, k-fold cross-validation

## Results
| Experiment | Best Config | Key Metric |
|---|---|---|
| Training size | 90% training | Accuracy: 95.4% |
| Feature selection | amount + fico + dti + emp_length | F1: 0.76 |
| Model type | Decision Tree > Logistic Regression | — |
| Hyperparameter tuning | gini, max_depth=9, min_samples_leaf=2 | CV score: 0.927 |
| Cross-validation | k=7 | Best F1/stability balance |

## What I Independently Completed
Coursework project. Instructor provided dataset and task prompts. I independently completed all feature engineering, model selection, five optimization experiments, and written analysis.

## Requirements
```
pandas, numpy, scikit-learn, matplotlib, seaborn
```
