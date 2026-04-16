---
layout: post
title: Statistics Chapter 5
category: Math
---

# Chapter 5: Multivariate Probability Distributions

## Purpose of this Chapter
This chapter introduces **multivariate probability distributions**, focusing on joint, marginal, and conditional distributions, as well as important properties such as independence, covariance, and correlation.

---

## 5.1 Introduction

Multivariate probability distributions describe the behavior of two or more random variables simultaneously. For random variables $X$ and $Y$, the joint probability distribution provides the probabilities associated with their simultaneous outcomes.

---

## 5.2 Bivariate and Multivariate Probability Distributions

### Joint Probability Distribution
The **joint probability distribution** of two discrete random variables $X$ and $Y$ is defined by:
$$
P(X = x, Y = y) = p(x, y),
$$
where:
$$
\sum_x \sum_y p(x, y) = 1.
$$

For continuous random variables, the **joint probability density function (PDF)** $f(x, y)$ satisfies:
1. $f(x, y) \geq 0$ for all $x, y$.
2. $ \int_{-\infty}^\infty \int_{-\infty}^\infty f(x, y) \, dx \, dy = 1 $.

---

## 5.3 Marginal and Conditional Probability Distributions

### Marginal Distributions
The **marginal probability distribution** of $X$ is obtained by summing (discrete case) or integrating (continuous case) the joint distribution over $Y$:
- Discrete:
  $$
  P(X = x) = \sum_y p(x, y).
  $$
- Continuous:
  $$
  f_X(x) = \int_{-\infty}^\infty f(x, y) \, dy.
  $$

### Conditional Distributions
The **conditional distribution** of $X$ given $Y = y$ is:
- Discrete:
  $$
  P(X = x \mid Y = y) = \frac{P(X = x, Y = y)}{P(Y = y)}.
  $$
- Continuous:
  $$
  f_{X \mid Y}(x \mid y) = \frac{f(x, y)}{f_Y(y)}, \quad f_Y(y) > 0.
  $$

---

## 5.4 Independent Random Variables

Random variables $X$ and $Y$ are **independent** if:
- Discrete:
  $$
  P(X = x, Y = y) = P(X = x) \cdot P(Y = y).
  $$
- Continuous:
  $$
  f(x, y) = f_X(x) \cdot f_Y(y).
  $$

### Example:
If $X$ and $Y$ represent two independent dice rolls:
- $P(X = 3, Y = 4) = P(X = 3) \cdot P(Y = 4) = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}$.

---

## 5.5 The Expected Value of a Function of Random Variables

For a function $g(X, Y)$ of two random variables:
- Discrete:
  $$
  E[g(X, Y)] = \sum_x \sum_y g(x, y) \cdot p(x, y).
  $$
- Continuous:
  $$
  E[g(X, Y)] = \int_{-\infty}^\infty \int_{-\infty}^\infty g(x, y) \cdot f(x, y) \, dx \, dy.
  $$

---

## 5.6 Special Theorems

### Linearity of Expectation
If $a, b$ are constants:
$$
E(aX + bY) = aE(X) + bE(Y).
$$

---

## 5.7 The Covariance of Two Random Variables

The **covariance** measures the linear relationship between two random variables:
$$
\text{Cov}(X, Y) = E[(X - E(X))(Y - E(Y))].
$$

Simplified formula:
$$
\text{Cov}(X, Y) = E(XY) - E(X)E(Y).
$$

### Properties:
1. $\text{Cov}(X, Y) > 0$: Positive linear relationship.
2. $\text{Cov}(X, Y) < 0$: Negative linear relationship.
3. $\text{Cov}(X, Y) = 0$: No linear relationship.

---

## 5.8 The Expected Value and Variance of Linear Functions of Random Variables

### Expected Value:
For random variables $X$ and $Y$, and constants $a, b, c$:
$$
E(aX + bY + c) = aE(X) + bE(Y) + c.
$$

### Variance:
$$
\text{Var}(aX + bY) = a^2 \text{Var}(X) + b^2 \text{Var}(Y) + 2ab \text{Cov}(X, Y).
$$

---

## 5.9 The Multinomial Probability Distribution

The **multinomial distribution** is a generalization of the binomial distribution, modeling the outcomes of $n$ trials with $k$ categories.

### PMF:
$$
P(X_1 = x_1, \ldots, X_k = x_k) = \frac{n!}{x_1! x_2! \cdots x_k!} p_1^{x_1} p_2^{x_2} \cdots p_k^{x_k},
$$
where:
- $\sum_{i=1}^k x_i = n$.
- $\sum_{i=1}^k p_i = 1$.

---

## 5.10 The Bivariate Normal Distribution (Optional)

The **bivariate normal distribution** is a joint distribution of two normally distributed variables $X$ and $Y$ with means $\mu_X$, $\mu_Y$, variances $\sigma_X^2$, $\sigma_Y^2$, and covariance $\sigma_{XY}$.

### PDF:
$$
f(x, y) = \frac{1}{2\pi \sigma_X \sigma_Y \sqrt{1-\rho^2}} \exp\left(-\frac{1}{2(1-\rho^2)} \left[ \frac{(x-\mu_X)^2}{\sigma_X^2} - 2\rho\frac{(x-\mu_X)(y-\mu_Y)}{\sigma_X \sigma_Y} + \frac{(y-\mu_Y)^2}{\sigma_Y^2} \right] \right),
$$
where $\rho = \frac{\sigma_{XY}}{\sigma_X \sigma_Y}$ is the correlation coefficient.

---

## 5.11 Conditional Expectations

The **conditional expectation** of $X$ given $Y = y$ is:
$$
E(X \mid Y = y) = \int_{-\infty}^\infty x \cdot f_{X \mid Y}(x \mid y) \, dx.
$$

---

## 5.12 Summary

This chapter covered the concepts of multivariate probability distributions, including:
1. Definitions of joint, marginal, and conditional distributions.
2. Independence of random variables.
3. Measures of dependence: covariance and correlation.
4. Special distributions like the multinomial and bivariate normal.

---

## Exercises

1. For two random variables $X$ and $Y$ with $f(x, y) = 2$ for $0 \leq x \leq 1$, $0 \leq y \leq 1$, find $P(X \leq 0.5, Y \leq 0.5)$.
2. Compute the covariance of $X$ and $Y$ if $E(X) = 2$, $E(Y) = 3$, $E(XY) = 10$.
3. If $X$ and $Y$ are independent, prove that $E(XY) = E(X)E(Y)$.
4. In a multinomial experiment with $n = 10$, $k = 3$, and probabilities $p_1 = 0.4$, $p_2 = 0.4$, and $p_3 = 0.2$, find the probability of outcomes $(4, 3, 3)$.
5. Verify that $\rho$ lies between $-1$ and $1$ for the bivariate normal distribution.

---
