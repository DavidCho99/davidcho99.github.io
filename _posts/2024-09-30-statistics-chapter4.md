---
layout: post
title: Statistics Chapter 4
category: Mathematics
---

# Chapter 4: Continuous Variables and Their Probability Distributions

## Purpose of this Chapter
This chapter explores **continuous random variables**, their probability distributions, and key concepts such as expected value, variance, and commonly used continuous distributions.

---

## 4.1 Introduction

A **continuous random variable** can take any value within an interval of the real line. Unlike discrete variables, continuous random variables are described using a **probability density function (PDF)** instead of a probability mass function (PMF).

---

## 4.2 The Probability Distribution for a Continuous Random Variable

The PDF, denoted as $f(x)$, satisfies:
1. $f(x) \geq 0$ for all $x$.
2. The total area under the curve is 1:
   $$
   \int_{-\infty}^\infty f(x) \, dx = 1.
   $$
3. The probability that $X$ lies within an interval $[a, b]$ is given by:
   $$
   P(a \leq X \leq b) = \int_a^b f(x) \, dx.
   $$

---

## 4.3 Expected Values for Continuous Random Variables

The **expected value** (mean) of a continuous random variable $X$ with PDF $f(x)$ is:
$$
E(X) = \int_{-\infty}^\infty x \cdot f(x) \, dx.
$$

The **variance** is:
$$
\text{Var}(X) = E(X^2) - [E(X)]^2,
$$
where:
$$
E(X^2) = \int_{-\infty}^\infty x^2 \cdot f(x) \, dx.
$$

---

## 4.4 The Uniform Probability Distribution

The **uniform distribution** describes a variable that is equally likely to take any value within an interval $[a, b]$.

### PDF:
$$
f(x) =
\begin{cases} 
\frac{1}{b-a}, & \text{if } a \leq x \leq b, \\
0, & \text{otherwise.}
\end{cases}
$$

### Mean and Variance:
- Mean:
  $$
  E(X) = \frac{a + b}{2}.
  $$
- Variance:
  $$
  \text{Var}(X) = \frac{(b-a)^2}{12}.
  $$

---

## 4.5 The Normal Probability Distribution

The **normal distribution** (Gaussian distribution) is the most widely used distribution in statistics. A random variable $X$ follows a normal distribution with mean $\mu$ and variance $\sigma^2$, denoted $X \sim N(\mu, \sigma^2)$.

### PDF:
$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}, \quad -\infty < x < \infty.
$$

### Properties:
1. Symmetric about $\mu$.
2. Mean: $E(X) = \mu$.
3. Variance: $\text{Var}(X) = \sigma^2$.

---

## 4.6 The Gamma Probability Distribution

The **gamma distribution** is used to model waiting times and is parameterized by $\alpha$ (shape) and $\beta$ (scale).

### PDF:
$$
f(x) = \frac{x^{\alpha-1} e^{-x/\beta}}{\Gamma(\alpha) \beta^\alpha}, \quad x > 0.
$$

Here, $\Gamma(\alpha)$ is the gamma function:
$$
\Gamma(\alpha) = \int_0^\infty t^{\alpha-1} e^{-t} \, dt.
$$

### Mean and Variance:
- Mean:
  $$
  E(X) = \alpha \beta.
  $$
- Variance:
  $$
  \text{Var}(X) = \alpha \beta^2.
  $$

---

## 4.7 The Beta Probability Distribution

The **beta distribution** is used for variables that take values in the interval $[0, 1]$.

### PDF:
$$
f(x) = \frac{x^{\alpha-1}(1-x)^{\beta-1}}{B(\alpha, \beta)}, \quad 0 \leq x \leq 1,
$$
where $B(\alpha, \beta)$ is the beta function:
$$
B(\alpha, \beta) = \int_0^1 t^{\alpha-1} (1-t)^{\beta-1} \, dt.
$$

### Mean and Variance:
- Mean:
  $$
  E(X) = \frac{\alpha}{\alpha + \beta}.
  $$
- Variance:
  $$
  \text{Var}(X) = \frac{\alpha \beta}{(\alpha + \beta)^2 (\alpha + \beta + 1)}.
  $$

---

## 4.8 Some General Comments

- The shape of a probability distribution depends on its parameters (e.g., $\mu$, $\sigma^2$ for normal distribution).
- Continuous distributions have applications in modeling physical processes, waiting times, proportions, and more.

---

## 4.9 Other Expected Values

For functions of a random variable $g(X)$:
$$
E[g(X)] = \int_{-\infty}^\infty g(x) \cdot f(x) \, dx.
$$

---

## 4.10 Tchebysheff’s Theorem

For any random variable $X$ with mean $\mu$ and standard deviation $\sigma$:
$$
P(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}, \quad k > 0.
$$

This theorem applies to continuous distributions as well.

---

## 4.11 Expectations of Discontinuous Functions and Mixed Probability Distributions (Optional)

In mixed distributions (e.g., combining discrete and continuous components), the expected value is computed by summing and integrating over the respective parts.

---

## 4.12 Summary

This chapter introduced key concepts and distributions for continuous random variables:
1. Definitions of PDFs and the properties of continuous variables.
2. Important distributions such as uniform, normal, gamma, and beta.
3. Calculation of expected values, variance, and probabilities for continuous distributions.

---

## Exercises

1. A random variable $X$ is uniformly distributed over $[2, 5]$. Find $P(3 \leq X \leq 4)$.
2. The height of a population follows a normal distribution with $\mu = 170$ cm and $\sigma = 10$ cm. Find the probability that a randomly selected individual is between 160 cm and 180 cm.
3. A gamma random variable has $\alpha = 3$ and $\beta = 2$. Compute its mean and variance.
4. For a beta random variable with $\alpha = 2$ and $\beta = 3$, calculate $E(X)$ and $\text{Var}(X)$.
5. Verify Tchebysheff’s theorem for a normal random variable with $\mu = 100$, $\sigma = 15$, and $k = 2$.

----
