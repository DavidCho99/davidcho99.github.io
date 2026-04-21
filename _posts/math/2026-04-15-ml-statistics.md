---
layout: post
title: "ML Statistics (Compact)"
category: Math
tags: [math, ml, statistics]
---

This is a compact “just enough stats” reference for practical ML.

## 1) Data splits and leakage
- Train/validation/test are for **generalization**, not for getting the best number once.
- Leakage: any feature engineering, scaling, imputation, or selection that “sees” validation/test data.

## 2) Bias/variance intuition
- High bias: underfit (too simple).
- High variance: overfit (too flexible).

## 3) Common metrics (what they mean)
- Regression: MAE, MSE/RMSE, $R^2$.
- Classification: accuracy, precision, recall, F1, ROC-AUC / PR-AUC (class imbalance).

## 4) Confidence vs calibration
- A model can be accurate but poorly calibrated.
- If you act on probabilities, check calibration (reliability diagram, ECE).

## 5) Overfitting checks
- Compare train vs validation curves.
- Use a baseline and sanity checks (label shuffling should break performance).

