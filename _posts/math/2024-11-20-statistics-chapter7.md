---
layout: post
title: Statistics Chapter 7
category: Math
---

# Chapter 7: Sampling Distributions

## Purpose of this Chapter
This chapter delves into **sampling distributions**, which describe the distribution of sample statistics over repeated sampling from the same population. Understanding sampling distributions is crucial for making inferences about population parameters based on sample data.

---

## 7.1 Introduction

### Key Concepts:
- **Population**: The entire set of individuals or observations.
- **Sample**: A subset drawn from the population.
- **Statistic**: A numerical measure computed from a sample (e.g., sample mean $\bar{X}$).
- **Sampling Distribution**: The probability distribution of a statistic over all possible samples of a given size from the population.

---

## 7.2 The Sampling Distribution of the Sample Mean

If $X_1, X_2, \ldots, X_n$ are independent and identically distributed (i.i.d.) random variables with mean $\mu$ and variance $\sigma^2$, the **sample mean** is defined as:
$$
\bar{X} = \frac{1}{n} \sum_{i=1}^n X_i
$$

### Properties of $\bar{X}$:
1. **Expected Value**:
   $$
   E(\bar{X}) = \mu
   $$
2. **Variance**:
   $$
   \text{Var}(\bar{X}) = \frac{\sigma^2}{n}
   $$
3. **Standard Error**:
   $$
   \text{SE}(\bar{X}) = \frac{\sigma}{\sqrt{n}}
   $$

---

## 7.3 The Central Limit Theorem (CLT)

The **Central Limit Theorem** states that, for a sufficiently large sample size $n$, the sampling distribution of the sample mean $\bar{X}$ approaches a normal distribution, regardless of the population's original distribution:
$$
\bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right) \quad \text{as } n \to \infty
$$

### Practical Implication:
- The CLT allows us to use normal probability models to make inferences about the sample mean when the sample size is large (commonly $n \geq 30$).

---

## 7.4 The Sampling Distribution of the Sample Variance

For a normal population with variance $\sigma^2$, the sample variance $S^2$ is given by:
$$
S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \bar{X})^2
$$

### Distribution of $S^2$:
- The statistic $\frac{(n-1)S^2}{\sigma^2}$ follows a chi-square distribution with $n-1$ degrees of freedom:
  $$
  \frac{(n-1)S^2}{\sigma^2} \sim \chi^2_{n-1}
  $$

---

## 7.5 The t-Distribution

When sampling from a normal population with an unknown variance, the **t-distribution** is used. The t-statistic is defined as:
$$
t = \frac{\bar{X} - \mu}{S / \sqrt{n}}
$$
where $S$ is the sample standard deviation.

### Properties of the t-Distribution:
1. Symmetric and bell-shaped, similar to the normal distribution.
2. Has heavier tails than the normal distribution, which accounts for the additional uncertainty from estimating the population standard deviation.
3. As the sample size increases, the t-distribution approaches the standard normal distribution.

---

## 7.6 The F-Distribution

The **F-distribution** arises when comparing two sample variances. If $S_1^2$ and $S_2^2$ are independent sample variances from normal populations, the F-statistic is:
$$
F = \frac{S_1^2 / \sigma_1^2}{S_2^2 / \sigma_2^2}
$$

### Properties of the F-Distribution:
1. It is skewed to the right.
2. Defined only for positive values.
3. Used primarily in analysis of variance (ANOVA) and regression analysis.

---

## 7.7 Relationships Among Distributions

1. **Chi-Square and Normal**:
   - If $Z \sim N(0, 1)$, then $Z^2 \sim \chi^2_1$.

2. **t-Distribution**:
   - If $Z \sim N(0, 1)$ and $W \sim \chi^2_\nu$ are independent, then:
     $$
     t = \frac{Z}{\sqrt{W / \nu}} \sim t_\nu
     $$

3. **F-Distribution**:
   - If $W_1 \sim \chi^2_{\nu_1}$ and $W_2 \sim \chi^2_{\nu_2}$ are independent, then:
     $$
     F = \frac{(W_1 / \nu_1)}{(W_2 / \nu_2)} \sim F_{\nu_1, \nu_2}
     $$

---

## 7.8 Applications of Sampling Distributions

### Estimation:
- Sampling distributions provide the foundation for constructing confidence intervals for population parameters.

### Hypothesis Testing:
- They are essential for determining the distribution of test statistics under the null hypothesis.

### Quality Control:
- Understanding the variability of sample statistics helps in setting control limits for process monitoring.

---

## 7.9 Summary

In this chapter, we explored:
1. The concept of sampling distributions and their importance in statistical inference.
2. The Central Limit Theorem and its implications.
3. Key distributions: chi-square, t, and F, along with their applications.

---

## Exercises

1. **Sampling Distribution of the Mean**:
   - Given a population with mean $\mu = 50$ and standard deviation $\sigma = 10$, what is the probability that the sample mean $\bar{X}$ for a sample of size $n = 25$ falls between 48 and 52?

2. **Application of the Central Limit Theorem**:
   - A population has a mean of 100 and a standard deviation of 20. If a random sample of size 40 is selected, what is the probability that the sample mean is greater than 105?

3. **t-Distribution Application**:
   - A sample of size 15 yields a sample mean of 75 and a sample standard deviation of 8. Construct a 95% confidence interval for the population mean.

4. **F-Distribution in Variance Comparison**:
   - Two independent samples have sizes $n_1 = 10$ and $n_2 = 12$ with sample variances $S_1^2 = 15$ and $S_2^2 = 20$, respectively. Test at the 5% significance level whether the two population variances
 
