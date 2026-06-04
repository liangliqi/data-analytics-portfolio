# Unsupervised Learning on U.S. University Data: PCA and K-Means Clustering

**Course:** MSSP 6080 — Practical Machine Learning, University of Pennsylvania (SP2)
**Author:** Liqi Liang | Fall 2024

## Overview

This project applies unsupervised machine learning to U.S. university statistics to discover latent institutional structure — without predefined labels — using PCA for dimensionality reduction and K-Means for clustering.

## Dataset
Government statistics on U.S. colleges covering enrollment, financials, selectivity, and faculty metrics.

## Methods
- MinMax normalization across all features
- PCA: varied components 2–10, selected 4; interpreted feature loadings per component
- K-Means: Elbow Method used to select K=4; clusters characterized by institutional profile

## Key Findings
- 4 PCA components captured substantial variance with meaningful compression
- K=4 clusters corresponded roughly to: large research universities, selective liberal arts colleges, mid-size public institutions, and smaller/less selective schools
- Elbow Method showed diminishing returns beyond K=4

## What I Independently Completed
Coursework project. Instructor provided dataset and task prompts. I independently completed all normalization, PCA, clustering code, component interpretation, and K selection rationale.

## Requirements
```
pandas, numpy, scikit-learn, matplotlib
```
