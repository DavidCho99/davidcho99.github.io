---
layout: post
title: Statistics Chapter 6
category: Math
---

# Chapter 6: Functions of Random Variables

## Purpose of this Chapter
This chapter introduces the concepts and methods for deriving the distributions of functions of random variables. It includes single and multivariable cases and covers techniques such as transformation methods and moment-generating functions.

---

## 6.1 Functions of a Single Random Variable

If $Y = g(X)$ is a function of a random variable $X$, the distribution of $Y$ depends on the form of $g(X)$ and the distribution of $X$.

### Transformation Method for Continuous Random Variables
To find the PDF of $Y$:
1. Compute the inverse transformation $X = h(Y)$.
2. Compute the derivative of the transformation: $\frac{d}{dy} h(Y)$.
3. Use the formula:
   $$
   f_Y(y) = f_X(h(y)) \cdot \left| \frac{d}{dy} h(y) \right|,
   $$
   where $h(Y)$ is the inverse of $g(X)$.

### Example:
If $X$ is uniformly distributed on $[0, 1]$ and $Y = 2X$, then:
1. $X = \frac{Y}{2}$.
2. $\frac{d}{dy} \left(\frac{Y}{2}\right) = \frac{1}{2}$.
3. The PDF of $Y$ is:
   $$
   f_Y(y) = f_X\left(\frac{y}{2}\right) \cdot \left|\frac{1}{2}\right| = 1 \cdot \frac{1}{2}, \quad 0 \leq y \leq 2.
   $$

---

## 6.2 Functions of Two Random Variables

Let $Z = g(X, Y)$ be a function of two random variables $X$ and $Y$. To find the distribution of $Z$, use the joint PDF $f(x, y)$.

### Method for Continuous Random Variables
1. Identify the region where the function $g(X, Y)$ is valid.
2. Transform to new variables, $U$ and $V$, where $Z = g(X, Y)$.
3. Compute the Jacobian determinant:
   $$
   \left| \frac{\partial(x, y)}{\partial(u, v)} \right|.
   $$
4. Use the formula for the joint PDF of $U$ and $V$:
   $$
   f_{U,V}(u, v) = f_{X,Y}(x, y) \cdot \left| \frac{\partial(x, y)}{\partial(u, v)} \right|.
   $$

---

## 6.3 The Distribution of the Sum of Independent Random Variables

Let $Z = X + Y$, where $X$ and $Y$ are independent random variables. The PDF of $Z$ is obtained by the **convolution** of the PDFs of $X$ and $Y$:
$$
f_Z(z) = \int_{-\infty}^\infty f_X(x) \cdot f_Y(z - x) \, dx.
$$

---

## 6.4 The Moment-Generating Function Technique

The **moment-generating function (MGF)** can simplify the derivation of the distribution of a function of random variables.

### Definition:
The MGF of a random variable $X$ is:
$$
M_X(t) = E(e^{tX}) = \int_{-\infty}^\infty e^{tx} f_X(x) \, dx.
$$

### Key Property:
If $M_X(t) = M_Y(t)$ for all $t$ in some interval, then $X$ and $Y$ have the same distribution.

### Example:
For $X \sim \text{Exponential}(\lambda)$, the MGF is:
$$
M_X(t) = \frac{\lambda}{\lambda - t}, \quad t < \lambda.
$$

---

## 6.5 The Distribution of the Maximum and Minimum of Random Variables

### Maximum of Two Independent Variables
Let $Z = \max(X, Y)$ for two independent random variables. The CDF of $Z$ is:
$$
F_Z(z) = P(Z \leq z) = P(X \leq z \text{ and } Y \leq z) = F_X(z) \cdot F_Y(z).
$$

### Minimum of Two Independent Variables
Let $W = \min(X, Y)$. The CDF of $W$ is:
$$
F_W(w) = P(W \leq w) = 1 - P(X > w \text{ and } Y > w) = 1 - (1 - F_X(w))(1 - F_Y(w)).
$$

---

## 6.6 Order Statistics

The $k$th **order statistic** is the $k$th smallest value in a sample of size $n$.

### Distribution of the $k$th Order Statistic
If $X_{(k)}$ is the $k$th order statistic:
1. The PDF is given by:
   $$
   f_{X_{(k)}}(x) = \frac{n!}{(k-1)!(n-k)!} \cdot [F_X(x)]^{k-1} \cdot f_X(x) \cdot [1 - F_X(x)]^{n-k}.
   $$

---

## 6.7 The Delta Method

The **delta method** is used to approximate the variance of a function of a random variable.

### Formula:
If $Y = g(X)$ and $X$ has mean $\mu$ and variance $\sigma^2$, then:
$$
\text{Var}(Y) \approx \left[g'(\mu)\right]^2 \sigma^2,
$$
where $g'(\mu)$ is the derivative of $g(X)$ evaluated at $\mu$.

---

## 6.8 Summary

This chapter introduced the methods to derive distributions of functions of random variables, including:
1. Transformation methods for single and multiple variables.
2. Convolution for sums of random variables.
3. Order statistics and their distributions.
4. The moment-generating function as a powerful tool for deriving distributions.
5. The delta method for variance approximation.

---

## Exercises

1. Let $X$ be uniformly distributed on $[0, 1]$, and $Y = X^2$. Find the PDF of $Y$.
2. If $X \sim \text{Exponential}(\lambda)$ and $Y = 2X$, derive the PDF of $Y$.
3. Compute the PDF of $Z = X + Y$ for $X$ and $Y$ uniformly distributed on $[0, 1]$.
4. Verify the MGF of $X \sim \text{Normal}(\mu, \sigma^2)$.
5. For a sample of size $n = 5$, derive the PDF of the second smallest value (second order statistic) if $X \sim \text{Uniform}(0, 1)$.

---
