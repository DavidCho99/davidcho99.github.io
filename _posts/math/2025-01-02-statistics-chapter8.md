---
layout: post
title: Statistics Chapter 8
category: Math
---

# Chapter 8: Estimation

## Purpose of this Chapter
This chapter focuses on **estimation theory**, which involves determining the values of population parameters based on sample data. Key concepts include point estimation, interval estimation, properties of estimators, and methods of finding estimators such as maximum likelihood estimation (MLE).

---

## 8.1 Introduction

Estimation is the process of using sample data to infer the value of a population parameter.

### Types of Estimation:
1. **Point Estimation**: Provides a single value as an estimate of the parameter.
2. **Interval Estimation**: Provides a range of values (confidence interval) within which the parameter is likely to lie.

---

## 8.2 Properties of Point Estimators

A **point estimator** is a statistic used to estimate a parameter (e.g., $\bar{X}$ to estimate $\mu$).

### Desirable Properties:
1. **Unbiasedness**:
   An estimator $\hat{\theta}$ is unbiased if:
   $$
   E(\hat{\theta}) = \theta.
   $$

2. **Efficiency**:
   An estimator is efficient if it has the smallest variance among all unbiased estimators.

3. **Consistency**:
   An estimator $\hat{\theta}$ is consistent if:
   $$
   \hat{\theta} \to \theta \quad \text{as } n \to \infty.
   $$

4. **Sufficiency**:
   An estimator $\hat{\theta}$ is sufficient if it captures all the information about the parameter contained in the sample.

---

## 8.3 Methods of Point Estimation

### 1. Method of Moments
The **method of moments** involves equating sample moments to population moments.

Example:
For a population with mean $\mu$ and variance $\sigma^2$, the first moment is:
$$
E(X) = \mu.
$$
Set the sample mean equal to $\mu$ to estimate $\mu$:
$$
\hat{\mu} = \bar{X}.
$$

### 2. Maximum Likelihood Estimation (MLE)
The **maximum likelihood estimator** maximizes the likelihood function:
$$
L(\theta) = P(\text{Sample} \mid \theta).
$$
Equivalently, maximize the log-likelihood function:
$$
\ell(\theta) = \ln L(\theta).
$$

Example:
For a normal distribution $X \sim N(\mu, \sigma^2)$, the likelihood function is:
$$
L(\mu, \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left(-\frac{(X_i - \mu)^2}{2\sigma^2}\right).
$$
Maximizing $\ell(\mu, \sigma^2)$ yields:
$$
\hat{\mu} = \bar{X}, \quad \hat{\sigma}^2 = \frac{1}{n} \sum_{i=1}^n (X_i - \bar{X})^2.
$$

---

## 8.4 Confidence Intervals

A **confidence interval** provides a range of values for the parameter, along with a confidence level (e.g., 95%).

### General Form:
For a parameter $\theta$:
$$
\text{Confidence Interval} = (\hat{\theta} - E, \hat{\theta} + E),
$$
where $E$ is the margin of error.

### Confidence Interval for the Mean:
1. Known variance:
   $$
   \bar{X} \pm z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}.
   $$
2. Unknown variance:
   $$
   \bar{X} \pm t_{\alpha/2, n-1} \cdot \frac{S}{\sqrt{n}}.
   $$

### Confidence Interval for a Proportion:
For a proportion $p$:
$$
\hat{p} \pm z_{\alpha/2} \cdot \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}.
$$

---

## 8.5 Sample Size Determination

The required sample size depends on the desired confidence level and margin of error.

### For Estimating the Mean:
If $\sigma$ is known:
$$
n = \left(\frac{z_{\alpha/2} \cdot \sigma}{E}\right)^2.
$$

### For Estimating a Proportion:
$$
n = \frac{z_{\alpha/2}^2 \cdot \hat{p}(1-\hat{p})}{E^2}.
$$

---

## 8.6 Bayesian Estimation (Optional)

In **Bayesian estimation**, prior knowledge about the parameter is combined with sample data using Bayes’ theorem:
$$
P(\theta \mid \text{Data}) = \frac{P(\text{Data} \mid \theta) \cdot P(\theta)}{P(\text{Data})}.
$$

The result is a posterior distribution for the parameter $\theta$.

---

## 8.7 Summary

This chapter introduced:
1. Point estimation and its desirable properties (unbiasedness, efficiency, consistency, and sufficiency).
2. Methods of estimation, including method of moments and maximum likelihood estimation (MLE).
3. Confidence intervals for the mean, proportion, and variance.
4. Sample size determination to achieve desired confidence levels and margins of error.

---

## Exercises

1. Show that $\hat{\mu} = \bar{X}$ is an unbiased estimator for the mean $\mu$.
2. Derive the maximum likelihood estimator for the parameter $\lambda$ of an exponential distribution.
3. Construct a 95% confidence interval for the population mean $\mu$ if $\bar{X} = 50$, $S = 5$, and $n = 25$.
4. Determine the required sample size to estimate a population mean within $E = 2$ with 95% confidence, given $\sigma = 10$.
5. Use Bayesian estimation to compute the posterior mean for $\theta$ if the prior is $P(\theta) \sim N(0, 1)$ and the likelihood is based on a sample $\bar{X} = 2$ with $n = 10$.

---
