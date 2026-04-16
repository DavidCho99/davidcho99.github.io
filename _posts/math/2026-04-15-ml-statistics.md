---
layout: post
title: ML Statistics
category: Math
---

# ML Statistics

This is a machine-learning-focused extraction from my Statistics notes 

## 1) Data Summary (EDA)

If you cannot summarize the data, you cannot model it.

- Graphical: histogram, boxplot (outliers/spread), scatterplot (relationships)
- Numerical:
  - Mean: $$\bar{x} = \frac{1}{n}\sum_{i=1}^n x_i$$
  - Sample variance: $$s^2 = \frac{1}{n-1}\sum_{i=1}^n (x_i-\bar{x})^2$$
  - Standard deviation: $$s = \sqrt{s^2}$$
- Empirical rule (normal-ish data): about 68% / 95% / ~99.7% within 1 / 2 / 3 standard deviations.

## 2) Probability Essentials

### Events and rules

- Sample space, events, set operations (union/intersection/complement).
- Two key laws:
  - Complement: $$P(A^c)=1-P(A)$$
  - Addition (general): $$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$

### Conditional probability and independence

- Conditional probability:
  $$P(A\mid B)=\frac{P(A\cap B)}{P(B)} \quad (P(B)>0)$$
- Independence:
  $$A \perp B \iff P(A\cap B)=P(A)P(B) \iff P(A\mid B)=P(A)$$

### Total probability and Bayes' rule

- Law of total probability partition $$B_1,\dots,B_k$$
  $$P(A)=\sum_{i=1}^k P(A\mid B_i)P(B_i)$$
- Bayes' rule:
  $$P(B_j\mid A)=\frac{P(A\mid B_j)P(B_j)}{\sum_{i=1}^k P(A\mid B_i)P(B_i)}$$

## 3) Random Variables and Distributions

### Discrete vs continuous

- Discrete RV: PMF $$p(x)=P(X=x)$$, with $$\sum_x p(x)=1$$.
- Continuous RV: PDF $$f(x)$$, with $$P(a\le X\le b)=\int_a^b f(x)\,dx$$ and $$\int_{-\infty}^{\infty} f(x)\,dx=1$$.

### Expectation and variance (core operators)

- Expectation:
  - Discrete: $$E[X]=\sum_x x\,p(x)$$
  - Continuous: $$E[X]=\int_{-\infty}^{\infty} x f(x)\,dx$$
- Variance:
  $$\mathrm{Var}(X)=E[(X-E[X])^2]=E[X^2]-E[X]^2$$

### Common distributions you will keep seeing in ML

- Binomial: number of successes in $$n$$ trials.
- Poisson: counts per interval.
- Uniform: simple bounded uncertainty.
- Normal: noise model; CLT justification.
- Gamma / Beta: flexible positive-support / (0,1)-support distributions.
- Multinomial: multi-class counts.

## 4) Multivariate Distributions, Dependence, Covariance

- Joint, marginal, conditional distributions:
  $$f_{X,Y}(x,y),\quad f_X(x)=\int f_{X,Y}(x,y)\,dy,\quad f_{Y\mid X}(y\mid x)=\frac{f_{X,Y}(x,y)}{f_X(x)}$$
- Covariance:
  $$\mathrm{Cov}(X,Y)=E[(X-E[X])(Y-E[Y])]$$
- Useful linear rules (used constantly in models):
  - Linearity: $$E[aX+bY]=aE[X]+bE[Y]$$
  - For independent $$X,Y$$: $$\mathrm{Var}(X+Y)=\mathrm{Var}(X)+\mathrm{Var}(Y)$$

## 5) Estimation: Point Estimators, MLE, and (Optional) Bayes

### Point vs interval

- Point estimation: one number.
- Interval estimation: a range (confidence interval).

### Properties worth remembering

- Unbiasedness: $$E[\hat{\theta}]=\theta$$
- Consistency: $$\hat{\theta}\to \theta$$ as $$n\to\infty$$

### Method of moments and maximum likelihood

- Method of moments: match sample moments to population moments.
- Maximum likelihood estimation (MLE): choose parameters that maximize
  $$L(\theta)=P(\text{sample}\mid \theta)$$
  $$\ell(\theta)=\log L(\theta)$$

### Bayesian estimation

Bayes updates parameters with data:
$$\text{posterior} \propto \text{likelihood}\times \text{prior}$$

## 6) Sampling Distributions and CLT (why averages become normal)

- Sampling distribution of the sample mean $\bar{X}$:$$E[\bar{X}]=\mu$$ $$\mathrm{Var}(\bar{X})=\sigma^2/n$$
- Central limit theorem (CLT): for large $n$, $\bar{X}$ is approximately normal even if the original data is not.

## 7) Confidence Intervals (uncertainty you can report)

- Generic form:
  $$\text{estimate} \pm (\text{critical value})\times(\text{standard error})$$
- Common cases in the notes:
  - Mean, proportion
  - Sample size planning (how much data you need for a target precision)

## 8) Minimal ML Checklist

- Sampling: treat train/val/test splits as random sampling when possible.
- Independence/i.i.d.: know when it breaks (time series, leakage, grouped data).
- Uncertainty: prefer reporting intervals (or at least standard errors) over only point estimates.
