# Sentiment Classification of Microblog Text

**Course:** MSSP 6080 — Practical Machine Learning, University of Pennsylvania (SP2)
**Author:** Liqi Liang | Fall 2024

## Overview

This project classifies the sentiment of microblog posts (tweets) as Positive or Negative using a bag-of-words approach. I compare 7 classifiers across 5 experimental conditions using 10-fold stratified cross-validation, optimizing for Cohen's Kappa.

## Dataset
5,000 labeled tweets with two sentiment label sets (`labels_A`, `labels_B`).

## Methods
- Bag-of-words (unigram and bigram) feature extraction via `CountVectorizer`
- 7 classifiers: Bernoulli NB, Complement NB, Multinomial NB, Linear SVM, RBF SVM, Polynomial SVM, Logistic Regression (L1/L2/unregularized)
- 10-fold stratified cross-validation, optimized for Cohen's Kappa

## Results
| Evaluation | Accuracy | Cohen's Kappa |
|---|---|---|
| Cross-validation (BernoulliNB) | 72.50% | 0.449 |
| Held-out test set | 74.60% | 0.492 |

**Best model:** Bernoulli Naïve Bayes with unigram features

## What I Independently Completed
Coursework project. Instructor provided dataset and task prompts. I independently completed all classifier selection, feature engineering decisions, optimization experiments, and written analysis.

## Requirements
```
pandas, numpy, scikit-learn, matplotlib
```
