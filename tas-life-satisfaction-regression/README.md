# Life Satisfaction in Early Adulthood: Regression Analysis of Health, Employment, and Family Factors

## Overview

This project examines determinants of life satisfaction among young adults at age 22, using longitudinal survey data from the **ICPSR Transition to Adulthood Supplement (TAS), Waves 1–5, 2005–2011** (ICPSR Study 31622). The analysis applies multiple linear regression with progressive model building, assumption diagnostics, outlier correction, variable transformation, and interaction testing.

---

## Research Questions

1. Are health, employment, education, and parental involvement independently associated with life satisfaction in early adulthood?
2. Does employment status moderate the effect of health on life satisfaction?

---

## Data

**Source:** ICPSR Study 31622 — Panel Study of Income Dynamics, Transition to Adulthood Supplement  
**Sample:** 2,739 respondents at age 22 (2,706 after outlier removal)

| Variable | Description |
|---|---|
| `life_satisfaction` | Self-reported satisfaction (1–4 scale, higher = more satisfied) |
| `health` | Self-rated health (1–5 scale, recoded: higher = better) |
| `work_last_week` | Employed in the past week (0/1) |
| `education` | Highest grade completed (8–18) |
| `mother_involvement` | Biological mother's involvement during childhood (1–4) |
| `father_involvement` | Biological father's involvement during childhood (1–4) |
| `gender` | 1 = Male, 2 = Female |
| `race_color` | 0 = White, 1 = non-White (derived from race indicators) |
| `cps_involvement` | Family CPS involvement before age 18 (0/1) |

---

## Methods

### Model Sequence

**Model 1 — Base model:** OLS regression with health, employment, gender, race, education, and parental involvement as predictors.

**Diagnostics:**
- Linearity checked via LOESS vs. linear fit plots for continuous predictors
- Normality assessed via histogram and Q-Q plot of residuals
- Outliers removed where |residual| > 2 (33 observations, n reduced from 2,739 to 2,706)

**Model 2 — Corrected model:** Re-estimated on cleaned data with:
- Health and education mean-centered
- Parental involvement log-transformed (log(x+1))
- Sequential model building (Models 1–6) with AIC comparison

**Model 3 — Interaction model:** Adds `health_centered × work_last_week` interaction term to test whether the effect of health on life satisfaction differs by employment status.

---

## Key Findings

- **Health** is the strongest predictor of life satisfaction (β ≈ 0.32, p < 0.001) across all model specifications
- **Employment** (work_last_week) has a significant positive association with life satisfaction, independent of health
- **Parental involvement** — both maternal and paternal — is positively associated with life satisfaction in early adulthood
- The **health × employment interaction** is not statistically significant, suggesting the effect of health on life satisfaction does not substantially differ between employed and unemployed individuals
- The corrected model explains approximately 22% of variance in life satisfaction (Adjusted R² = 0.218)

---

## Files

| File | Description |
|---|---|
| `tas_life_satisfaction_regression.Rmd` | Full analysis source |
| `tas_life_satisfaction_regression.html` | Rendered output |
| `df.rda` | ICPSR TAS dataset (DS0012) — not included; download from [ICPSR 31622](https://www.icpsr.umich.edu/web/ICPSR/studies/31622) |

> **Note:** The raw data file (`df.rda`) requires an ICPSR account to download. Once downloaded, place it in the same directory as the `.Rmd` file before knitting.

---

## Requirements

```r
install.packages(c("stargazer", "knitr", "ggplot2"))
```
