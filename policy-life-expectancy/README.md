# Life Expectancy Determinants: Regression and Random Forest Analysis

**Course:** MSSP 6070 — Practical Programming for Data Science, University of Pennsylvania (SP2)
**Author:** Liqi Liang | Fall 2024

## Overview

This project analyzes socioeconomic, health, and environmental determinants of life expectancy across 193 countries (2000–2015) using WHO data. I compare three modeling approaches to identify key drivers of global health disparities and assess how country development status moderates the effects of education and immunization.

A full written report accompanies this notebook: [Final_Case_Study_Report_Liqi_Liang.pdf](./Final_Case_Study_Report_Liqi_Liang.pdf)

## Dataset

WHO Life Expectancy dataset (Kaggle): 2,938 observations across 193 countries, 2000–2015. Variables include health indicators (HIV/AIDS, immunization rates, BMI), economic metrics (GDP, health expenditure), and social determinants (schooling, development status).

## Methods

**Data Cleaning**
- Removed countries with only one year of data
- Linear interpolation within country groups for missing values
- Mean imputation for remaining gaps
- Removed highly collinear variables (income composition, under-five deaths, thinness 5-9 years)

**Models**
| Model | Method | R² |
|---|---|---|
| Model 1 | OLS Linear Regression | 0.802 |
| Model 2 | Random Forest Regressor | 0.958 |
| Model 3 | OLS with Interaction Effects (Status × Schooling, Status × Immunization) | ~0.804 |

## Key Findings

- **Schooling** is the strongest positive predictor in the linear model; **HIV/AIDS** dominates Random Forest feature importance (score = 0.590)
- Both models agree: HIV/AIDS prevalence and adult mortality are the most critical negative determinants globally
- Interaction effects reveal that schooling and immunization have **stronger positive impacts in developing countries**, suggesting disproportionate policy returns in low-resource settings

## What I Independently Completed

This was a final course project. I independently completed all data cleaning and imputation logic, multicollinearity analysis and variable selection, all three models and their interpretation, and the written case study report.

## Requirements

```
pandas, numpy, matplotlib, seaborn, scipy, plotly, statsmodels, scikit-learn
```
