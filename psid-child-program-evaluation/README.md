# Early Childhood Program Evaluation: Regression Analysis of WIC and AFDC Effects

## Overview

This project uses data from the **Child Development Supplement of the Panel Study of Income Dynamics (PSID-CDS)** to evaluate how participation in two federal early childhood programs — WIC (Women, Infants, and Children Nutrition Program) and AFDC (Aid to Families with Dependent Children) — relates to children's academic outcomes.

The analysis is structured in three parts, each building methodologically on the previous.

---

## Research Questions

1. Do WIC and AFDC participation during pregnancy have independent effects on children's reading achievement, after controlling for family income, child age, birth weight, and home environment?
2. Do the OLS regression assumptions hold for a model predicting math achievement? How does outlier correction affect the results?
3. Is the effect of WIC participation on math achievement moderated by family income, race, or child age?

---

## Data

**Source:** Child Development Supplement (CDS) of the Panel Study of Income Dynamics (PSID)  
**Sample:** ~1,843–2,036 children (varies by model and missing data exclusions)  
**Key variables:**

| Variable | Description |
|---|---|
| `readss97` | Woodcock-Johnson Reading Achievement Score (1997) |
| `mathraw97` | Woodcock-Johnson Math Achievement Raw Score (1997) |
| `WICpreg` | WIC program participation during pregnancy (0/1) |
| `AFDCpreg` | AFDC program participation during pregnancy (0/1) |
| `AGE97` | Child age in 1997 |
| `faminc97` / `loginc97` | Family income (raw / log-transformed) |
| `bthwht` | Low birth weight status (0/1) |
| `HOME97` | Home environment quality score (emotional/cognitive stimulation) |
| `CHRACE` / `RACE` | Child race (recoded to binary: 0 = White, 1 = non-White) |

---

## Methods by Part

### Part 1 — Multiple Regression (Reading Achievement)
Three nested OLS models estimate the individual and joint effects of WIC and AFDC participation. Partial F-tests assess unique variance contributions.

### Part 2 — Assumption Diagnostics and Corrections (Math Achievement)
- Linearity checked via scatterplots with fitted lines
- Homoscedasticity assessed via residuals vs. fitted plot
- Normality assessed via histogram and Q-Q plot
- Outliers identified using studentized residuals (|z| > 3), leverage values (> 0.03), and Cook's Distance (> 4/n)
- Corrected model re-estimated on cleaned data; HOME97 added as an extended specification

### Part 3 — Interaction Effects (Math Achievement)
Tests whether WIC's effect is moderated by:
- **Family income** (`WICpreg × loginc97`)
- **Race** (`WICpreg × RACE`)
- **Child age** (`WICpreg × AGE97`)

Each interaction model compared to the base via ANOVA. A full model includes all three interaction terms simultaneously.

---

## Key Findings

- Both WIC and AFDC participation are **negatively associated** with reading and math scores after controlling for other factors — likely reflecting unmeasured socioeconomic disadvantage among program participants rather than program harm
- Home environment quality (HOME97) is a **strong positive predictor** across all models and partially mediates income effects
- All three interaction terms are statistically significant: the effect of WIC participation is moderated by family income, race, and child age
- Outlier removal improves model fit (R² increases from 0.864 to 0.908); coefficient patterns remain substantively stable

---

## Files

| File | Description |
|---|---|
| `psid_child_development_regression.Rmd` | Full analysis — all three parts (source) |
| `psid_child_development_regression.html` | Rendered output with all results and plots |
| `good.csv` | PSID-CDS analysis dataset |

---

## Requirements

```r
install.packages(c("stargazer", "knitr"))
```

To run: open `psid_child_development_regression.Rmd` in RStudio and knit to HTML. The working directory should contain `good.csv`.
