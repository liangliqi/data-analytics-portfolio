# Data Analytics Portfolio

**Liqi Liang** · M.S. Social Policy & Data Analytics, University of Pennsylvania (2026) · [lianglq@sas.upenn.edu](mailto:lianglq@sas.upenn.edu) [liangrosetta@gmail.com](liangrosetta@gmail.com)

I work at the intersection of data analysis and social policy — using quantitative methods to understand how programs, environments, and institutions shape outcomes for people. My background combines hands-on policy fieldwork (program evaluation at Penn's Netter Center, nonprofit due diligence) with technical training in machine learning, causal inference, and spatial analysis. Before Penn, I worked in business analytics at JD.com, investment research at ICBC Credit Suisse, and audit at Deloitte.

**Technical skills:** Python · R · SQL · Tableau · ArcGIS · Machine Learning · Causal Inference · Program Evaluation

---

## Projects

### Policy & Social Data Analysis

| Project | Methods | Tools |
|---|---|---|
| [Early Childhood Program Evaluation: WIC & AFDC Effects on Academic Achievement](./psid-child-program-evaluation) | Multiple regression · Assumption diagnostics · Outlier correction · Interaction effects | R |
| [Life Satisfaction in Early Adulthood: Health, Employment & Family Factors](./tas-life-satisfaction-regression) | OLS regression · Variable transformation · Interaction testing · AIC model selection | R |
| [Global Life Expectancy: Policy and Health Determinants](./policy-life-expectancy) | OLS · Random Forest · Interaction effects | Python |

**psid-child-program-evaluation** uses PSID data to evaluate WIC and AFDC program effects on children's reading and math achievement. Covers three analytical stages: baseline regression, assumption diagnostics with outlier correction, and moderation analysis testing whether WIC's effect varies by family income, race, and child age.

**tas-life-satisfaction-regression** examines determinants of life satisfaction at age 22 using ICPSR longitudinal data. Applies sequential model building, outlier removal, mean-centering and log-transformation, and tests whether employment moderates the health–satisfaction relationship.

**policy-life-expectancy** predicts country-level life expectancy using WHO data. Compares OLS and Random Forest performance (R² 0.80 vs 0.96), identifies HIV/AIDS prevalence and adult mortality as dominant predictors, and finds schooling and immunization have stronger returns in developing countries.

---

### Machine Learning

| Project | Methods | Tools |
|---|---|---|
| [Loan Default Prediction](./ml-loan-prediction) | Logistic Regression · Random Forest · XGBoost · SHAP | Python |
| [Sentiment Classification](./ml-sentiment-classification) | NLP · TF-IDF · LSTM · BERT fine-tuning | Python |
| [University Clustering](./ml-unsupervised-universities) | K-Means · PCA · Hierarchical clustering | Python |

**ml-loan-prediction** builds a credit risk classification model on imbalanced financial data. Uses SMOTE for class balancing, compares three classifiers, and applies SHAP values to interpret feature contributions — bridging model performance and business explainability.

**ml-sentiment-classification** benchmarks classical and deep learning approaches to text sentiment. Progresses from TF-IDF + logistic regression through LSTM to fine-tuned BERT, quantifying the accuracy-cost tradeoff at each step.

**ml-unsupervised-universities** segments U.S. universities by academic and financial profile using unsupervised methods. Combines PCA for dimensionality reduction with K-Means and hierarchical clustering to identify peer groups.

---

### Spatial Analysis (GIS)

| Project | Methods | Tools |
|---|---|---|
| [Pittsburgh & Beyond: Community Mapping](./pittsburgh-gis-community-mapping) | Choropleth mapping · Buffer analysis · Spatial join · Distance decay | ArcGIS Pro |

Eight spatial analysis projects covering poverty and crime patterns, park accessibility and distance decay, police beat delineation, land use classification with hillshade terrain, commercial zoning analysis, demographic mapping, HHW event catchment areas, and earthquake risk assessment for California cities.

---

## Background

My policy work informs how I approach data problems — I've conducted field research and stakeholder interviews for K-12 health program evaluation at Penn's Netter Center, co-authored a grant proposal that secured $15,000 for a Philadelphia nonprofit, and done industry analysis at JD.com (European e-commerce) and ICBC Credit Suisse (investment research). I bring that applied context to how I frame analytical questions and communicate results.

Open to data analyst, policy analyst, and research analyst roles. STEM OPT eligible (3-year).
