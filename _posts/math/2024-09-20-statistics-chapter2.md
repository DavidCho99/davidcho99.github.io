---
layout: post
title: Statistics Chapter 2
category: Math
---

# Chapter 2: Probability

## Purpose of this Chapter
This chapter introduces the foundational concepts of probability, which form the basis for statistical inference. Understanding probability allows us to quantify uncertainty and make predictions about random phenomena.

---

## 2.1 Introduction

### What Is Probability?
Probability measures the likelihood of an event occurring, expressed as a number between 0 and 1:
- \( P(A) = 0 \): Event \( A \) will not occur.
- \( P(A) = 1 \): Event \( A \) will certainly occur.
- \( 0 < P(A) < 1 \): Event \( A \) may occur with some likelihood.

---

## 2.2 Probability and Inference
Statistical inference relies on probability to:
1. Predict population characteristics based on a sample.
2. Quantify the uncertainty of conclusions.

---

## 2.3 A Review of Set Notation

### Definitions
- **Sample Space (\( S \))**: The set of all possible outcomes.  
  Example:
  $$
  S = \{1, 2, 3, 4, 5, 6\}
  $$

- **Event**: A subset of the sample space.  
  Example:
  $$
  A = \{\text{rolling an even number}\} = \{2, 4, 6\}
  $$

- **Union** (\( A \cup B \)): Events in \( A \), \( B \), or both.

- **Intersection** (\( A \cap B \)): Events in both \( A \) and \( B \).

- **Complement** (\( A^c \)): Events not in \( A \).

---

## 2.4 A Probabilistic Model for an Experiment: The Discrete Case

### Key Components
1. **Sample Space (\( S \))**.
2. **Events**: Subsets of \( S \).
3. **Probability Function (\( P \))**: Assigns probabilities to events.

Example: Rolling a die:  
$$
S = \{1, 2, 3, 4, 5, 6\}
$$

Probability of rolling an even number:  
$$
P(\text{even}) = P(\{2, 4, 6\}) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = \frac{1}{2}.
$$

---

## 2.5 Calculating the Probability of an Event: The Sample-Point Method

### Formula
For a finite sample space:
$$
P(A) = \sum_{x \in A} P(x)
$$

Example: For a loaded die:
$$
P(1) = 0.1, \, P(2) = 0.2, \, P(3) = 0.2, \, P(4) = 0.1, \, P(5) = 0.2, \, P(6) = 0.2.
$$
The probability of rolling \( \{2, 4, 6\} \) is:
$$
P(\{2, 4, 6\}) = P(2) + P(4) + P(6) = 0.2 + 0.1 + 0.2 = 0.5.
$$

---

## 2.6 Tools for Counting Sample Points

1. **Multiplication Rule**  
   If an experiment has \( k \) stages, with \( n_1, n_2, \ldots, n_k \) outcomes:
   $$
   \text{Total outcomes} = n_1 \cdot n_2 \cdot \ldots \cdot n_k
   $$

   Example: Tossing a coin and rolling a die:
   - Coin: \( 2 \) outcomes (\( H, T \)).
   - Die: \( 6 \) outcomes.
   - Total outcomes:
     $$
     2 \cdot 6 = 12
     $$

2. **Permutations**  
   Number of ways to arrange \( n \) distinct objects:
   $$
   P(n, r) = \frac{n!}{(n-r)!}
   $$

3. **Combinations**  
   Number of ways to choose \( r \) objects from \( n \) without regard to order:
   $$
   C(n, r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}
   $$

   Example: Choosing 2 fruits from 3 (\( A, B, C \)):
   $$
   C(3, 2) = \binom{3}{2} = \frac{3!}{2! \cdot (3-2)!} = 3.
   $$

---

## 2.7 Conditional Probability and Independence

### Conditional Probability
The probability of \( A \) given \( B \):
$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}, \quad P(B) > 0.
$$

Example:
$$
P(A) = 0.3, \, P(B) = 0.4, \, P(A \cap B) = 0.2.
$$
Then:
$$
P(A \mid B) = \frac{0.2}{0.4} = 0.5.
$$

### Independence
Events \( A \) and \( B \) are independent if:
$$
P(A \cap B) = P(A) \cdot P(B).
$$

---

## 2.8 Two Laws of Probability

1. **Additive Rule**  
   For events \( A \) and \( B \):
   $$
   P(A \cup B) = P(A) + P(B) - P(A \cap B).
   $$

2. **Complement Rule**  
   $$
   P(A^c) = 1 - P(A).
   $$

Example:
$$
P(A) = 0.6, \, P(B) = 0.5, \, P(A \cap B) = 0.2.
$$
Then:
$$
P(A \cup B) = 0.6 + 0.5 - 0.2 = 0.9.
$$

---

## 2.10 The Law of Total Probability and Bayes’ Rule

### Law of Total Probability
For mutually exclusive events \( B_1, B_2, \ldots, B_n \) covering \( S \):
$$
P(A) = \sum_{i=1}^n P(A \mid B_i) \cdot P(B_i).
$$

### Bayes’ Rule
$$
P(B_i \mid A) = \frac{P(A \mid B_i) \cdot P(B_i)}{P(A)}.
$$

Example:
$$
P(B_1) = 0.6, \, P(B_2) = 0.4.
$$
$$
P(A \mid B_1) = 0.5, \, P(A \mid B_2) = 0.2.
$$
Find \( P(B_1 \mid A) \):
$$
P(A) = (0.5 \cdot 0.6) + (0.2 \cdot 0.4) = 0.38.
$$
$$
P(B_1 \mid A) = \frac{0.5 \cdot 0.6}{0.38} = 0.789.
$$

---

## 2.11 Numerical Events and Random Variables

### What are Random Variables?
A **random variable** is a numerical outcome of a random experiment. There are two types:
1. **Discrete Random Variables**: Take countable values.
   Example: The number of heads in 3 coin tosses.
2. **Continuous Random Variables**: Take any value within an interval.
   Example: The height of students in a class.

### Probability Distribution
A **probability distribution** describes the likelihood of each possible value of a random variable.

For discrete random variables:
$$
P(X = x) = p(x), \quad \text{where } \sum_x p(x) = 1.
$$

For continuous random variables:
$$
P(a \leq X \leq b) = \int_a^b f(x) \, dx, \quad \text{where } \int_{-\infty}^\infty f(x) \, dx = 1.
$$

---

## 2.12 Random Sampling

### Definition
**Random sampling** ensures each member of the population has an equal chance of being selected. This is critical for unbiased statistical inference.

### Types of Sampling:
1. **Simple Random Sampling**: Each subset of size \( n \) is equally likely to be chosen.
2. **Stratified Sampling**: Population is divided into strata, and samples are taken from each stratum.
3. **Cluster Sampling**: Population is divided into clusters, and entire clusters are randomly selected.

---

## 2.13 Summary
This chapter introduced the basics of probability, including:
1. Definitions of key terms like **sample space** and **events**.
2. Mathematical rules like the **addition rule**, **complement rule**, and **Bayes’ Rule**.
3. The role of random variables in describing outcomes.
4. The importance of random sampling for unbiased inference.

Probability is a cornerstone of statistics, forming the bridge between data and inference.

---
### Exercises

1. A fair die is rolled twice. What is the probability of getting a sum of 7?

   - Sample space: Rolling two dice results in \( 6 \times 6 = 36 \) outcomes.
   - Favorable outcomes for a sum of 7: \( (1,6), (2,5), (3,4), (4,3), (5,2), (6,1) \) (6 outcomes).
   - Probability:
     $$
     P(\text{sum} = 7) = \frac{6}{36} = \frac{1}{6}.
     $$

2. If a coin is flipped 3 times, what is the probability of getting at least 2 heads?

   - Sample space: \( 2^3 = 8 \) outcomes: \( \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\} \).
   - Favorable outcomes: At least 2 heads (\( HHH, HHT, HTH, THH \)) = 4 outcomes.
   - Probability:
     $$
     P(\text{at least 2 heads}) = \frac{4}{8} = \frac{1}{2}.
     $$

3. A bag contains 3 red balls, 5 green balls, and 2 blue balls. If one ball is drawn at random, what is the probability it is not green?

   - Total balls: \( 3 + 5 + 2 = 10 \).
   - Favorable outcomes: \( \{ \text{red or blue balls} \} = 3 + 2 = 5 \).
   - Probability:
     $$
     P(\text{not green}) = \frac{5}{10} = \frac{1}{2}.
     $$

4. For a random sample of size \( n = 10 \), calculate the probability of selecting at least 3 defective items from a batch where \( 20\% \) are defective.

   - Let \( X \) be the number of defective items, \( X \sim \text{Binomial}(n=10, p=0.2) \).
   - Probability:
     $$
     P(X \geq 3) = 1 - P(X \leq 2).
     $$
   Using the binomial probability formula:
     $$
     P(X = k) = \binom{n}{k} p^k (1-p)^{n-k},
     $$
   calculate:
     $$
     P(X \leq 2) = P(X = 0) + P(X = 1) + P(X = 2).
     $$
     Substituting values, solve for \( P(X \geq 3) \).

5. Using Bayes' Rule, solve:

   Given:
   - \( P(B_1) = 0.4, \, P(B_2) = 0.6 \),
   - \( P(A \mid B_1) = 0.7, \, P(A \mid B_2) = 0.5 \).

   Step 1: Find \( P(A) \) using the law of total probability:
   $$
   P(A) = P(A \mid B_1)P(B_1) + P(A \mid B_2)P(B_2).
   $$
   Substituting values:
   $$
   P(A) = (0.7)(0.4) + (0.5)(0.6) = 0.28 + 0.30 = 0.58.
   $$

   Step 2: Apply Bayes' Rule:
   $$
   P(B_1 \mid A) = \frac{P(A \mid B_1)P(B_1)}{P(A)}.
   $$
   Substituting values:
   $$
   P(B_1 \mid A) = \frac{(0.7)(0.4)}{0.58} = \frac{0.28}{0.58} \approx 0.483.
   $$
