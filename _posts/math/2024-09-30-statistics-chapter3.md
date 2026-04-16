---
layout: post
title: Statistics Chapter 3
category: Math
---

# Chapter 3: Discrete Random Variables and Their Probability Distributions

---

## 3.1 Basic Definition

### What is a Random Variable?
A **random variable** assigns a numerical value to each outcome in a sample space. There are two types:
1. **Discrete Random Variable**: Takes countable values.
   Example: Number of heads in 3 coin tosses.
2. **Continuous Random Variable**: Takes values within an interval.

---

## 3.2 The Probability Distribution for a Discrete Random Variable

### Probability Mass Function (PMF)
For a discrete random variable $X$, the **probability mass function** (PMF) assigns probabilities to each possible value of $X$:
$$
P(X = x) = p(x), \quad \text{where } \sum_x p(x) = 1.
$$

### Example:
Consider a fair die:
$$
P(X = x) = \frac{1}{6}, \quad x = 1, 2, 3, 4, 5, 6.
$$

---

## 3.3 The Expected Value of a Random Variable or a Function of a Random Variable

### Expected Value
The **expected value** (mean) of a random variable $X$ is:
$$
E(X) = \sum_x x \cdot P(X = x).
$$

### Example:
A fair die:
$$
E(X) = \sum_{x=1}^6 x \cdot P(X = x) = \sum_{x=1}^6 x \cdot \frac{1}{6}.
$$
Simplifying:
$$
E(X) = \frac{1}{6} (1 + 2 + 3 + 4 + 5 + 6) = 3.5.
$$

---

## 3.4 The Binomial Probability Distribution

### Definition
A random variable $X$ follows a **binomial distribution** if:
1. The experiment consists of $n$ independent trials.
2. Each trial results in success (probability $p$) or failure (probability $1-p$).
3. $X$ is the number of successes in $n$ trials.

The probability mass function is:
$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}, \quad k = 0, 1, 2, \dots, n.
$$

### Expected Value and Variance
- Expected value: 
  $$
  E(X) = n \cdot p.
  $$
- Variance:
  $$
  \text{Var}(X) = n \cdot p \cdot (1-p).
  $$

---

## 3.5 The Geometric Probability Distribution

### Definition
A random variable $X$ follows a **geometric distribution** if $X$ is the number of trials until the first success. The PMF is:
$$
P(X = k) = (1-p)^{k-1} p, \quad k = 1, 2, 3, \dots.
$$

### Expected Value
- Expected value:
  $$
  E(X) = \frac{1}{p}.
  $$

---

## 3.6 The Negative Binomial Probability Distribution (Optional)

### Definition
A random variable $X$ follows a **negative binomial distribution** if $X$ is the number of trials until the $r$-th success. The PMF is:
$$
P(X = k) = \binom{k-1}{r-1} p^r (1-p)^{k-r}, \quad k = r, r+1, \dots.
$$

### Expected Value and Variance
- Expected value:
  $$
  E(X) = \frac{r}{p}.
  $$
- Variance:
  $$
  \text{Var}(X) = \frac{r \cdot (1-p)}{p^2}.
  $$

---

## 3.7 The Hypergeometric Probability Distribution

### Definition
A random variable $X$ follows a **hypergeometric distribution** when sampling without replacement from a finite population. The PMF is:
$$
P(X = k) = \frac{\binom{r}{k} \binom{N-r}{n-k}}{\binom{N}{n}}, \quad k = \max(0, n-(N-r)), \dots, \min(r, n).
$$

### Expected Value
- Expected value:
  $$
  E(X) = n \cdot \frac{r}{N}.
  $$

---

## 3.8 The Poisson Probability Distribution

### Definition
A random variable $X$ follows a **Poisson distribution** if the number of events occurring in a fixed interval of time or space follows the PMF:
$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad k = 0, 1, 2, \dots.
$$
Where $\lambda$ is the average number of events in the interval.

### Expected Value and Variance
- Expected value:
  $$
  E(X) = \lambda.
  $$
- Variance:
  $$
  \text{Var}(X) = \lambda.
  $$

---

## 3.9 Moments and Moment-Generating Functions

### Definition
The **$r$-th moment** of a random variable $X$ is:
$$
\mu_r = E(X^r).
$$

The **moment-generating function** (MGF) is:
$$
M_X(t) = E(e^{tX}).
$$

### Properties:
1. $M_X^{(r)}(0) = E(X^r)$ (The $r$-th derivative evaluated at $t=0$ gives the $r$-th moment).
2. The MGF uniquely determines the distribution.

---

## 3.10 Probability-Generating Functions (Optional)

The **probability-generating function** for a discrete random variable $X$ is:
$$
G_X(t) = E(t^X) = \sum_{k=0}^\infty P(X = k) t^k.
$$

---

## 3.11 Tchebysheff’s Theorem

### Statement
For any random variable $X$ with mean $\mu$ and variance $\sigma^2$, the probability that $X$ lies within $k$ standard deviations of the mean is:
$$
P(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}.
$$

---

## 3.12 Summary

This chapter introduced discrete random variables, their probability distributions, and key concepts such as:
1. Expected value and variance.
2. Binomial, geometric, negative binomial, hypergeometric, and Poisson distributions.
3. Moment-generating and probability-generating functions.
4. Tchebysheff’s Theorem for understanding the spread of data.

---

## Exercises
1. A coin is flipped 10 times. What is the probability of getting exactly 6 heads?
2. A random variable $X$ follows a Poisson distribution with $\lambda = 3$. Calculate $P(X = 2)$.
3. Verify Tchebysheff’s inequality for a dataset with $\mu = 5$, $\sigma^2 = 4$, and $k = 2$.
4. Show that the sum of two independent Poisson random variables is also Poisson.
5. Find the MGF of the geometric distribution and use it to calculate $E(X)$.

---
