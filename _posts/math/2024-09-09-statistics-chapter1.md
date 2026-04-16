---
layout: post
title: Statistics Chapter 1
category: Math
---

# Chapter 1: What Is Statistics?

## Purpose of this Chapter
This chapter establishes the foundation of statistics, explaining its purpose and role in analyzing data to make inferences. It introduces populations, samples, and the connection between statistical methods and real-world applications.

---

## 1.1 Introduction

### Definition of Statistics
Statistics is the science of:
- **Collecting** data.
- **Analyzing** data.
- **Interpreting** data.
- **Presenting** data.

Statistics aims to:
1. Make decisions under uncertainty.
2. Draw conclusions about populations based on samples.

### Real-World Applications
- **Elections:** Predicting results through surveys.
- **Medicine:** Testing drug efficacy.
- **Manufacturing:** Assessing product quality.

---

## 1.2 Characterizing a Set of Measurements: Graphical Methods

### Purpose
Graphical methods provide a visual summary of data, enabling quick insights into patterns, distributions, and variability.

### Common Graphical Methods
1. **Histograms:**
   - Visualize the frequency distribution of data.
   - Divide the range of data into equal intervals (bins).
   - Height of each bar represents frequency.

   **Example:**
   Data: \( 2.1, 2.4, 2.2, 2.3, 2.7, 2.5, 2.4, 2.6, 2.6, 2.9 \)  
   - Bins: \( [2.0, 2.2], [2.2, 2.4], [2.4, 2.6], [2.6, 2.8], [2.8, 3.0] \).  
   - Histogram:
     ```
     [2.0, 2.2] -> ▇
     [2.2, 2.4] -> ▇▇
     [2.4, 2.6] -> ▇▇▇
     [2.6, 2.8] -> ▇▇▇▇
     [2.8, 3.0] -> ▇
     ```

2. **Boxplots:**
   - Summarize data using minimum, Q1, median, Q3, and maximum.
   - Detect outliers and spread.

3. **Scatterplots:**
   - Show relationships between two variables.
   - Example: Plotting height vs. weight.

---

## 1.3 Characterizing a Set of Measurements: Numerical Methods

Numerical measures are used to summarize data more precisely than graphical methods.

### Measures of Central Tendency:
1. **Mean**: The arithmetic average of the data.
   $$ \bar{y} = \frac{1}{n} \sum_{i=1}^n y_i $$
   Where \(n\) is the number of observations, and \(y_i\) are the data values.

2. **Median**: The middle value when the data is ordered.

### Measures of Variability:
1. **Variance**: Measures the spread of data around the mean.
   $$ s^2 = \frac{1}{n-1} \sum_{i=1}^n (y_i - \bar{y})^2 $$
   Where \(s^2\) is the sample variance.

2. **Standard Deviation**: The square root of the variance.
   $$ s = \sqrt{s^2} $$

### Empirical Rule:
For mound-shaped (normal) distributions:
- Approximately $68\%$ of data lies within $1$ standard deviation of the mean: $ \mu \pm \sigma $.
- Approximately $95\%$ lies within $2$ standard deviations: $ \mu \pm 2\sigma $.
- Nearly all data lies within $3$ standard deviations: $ \mu \pm 3\sigma $.


---

## 1.4 How Inferences Are Made

Statistics enable inferences about a population using a sample. For example:
- To predict if a candidate will win an election, a sample of voters is surveyed. If the sample shows strong support, an inference is made that the candidate is likely to win.

### Key Idea:
The sample's characteristics are used as estimates for the population's characteristics, with an associated degree of uncertainty.

---

## 1.5 Theory and Reality

Statistical theory provides the foundation for making inferences from a sample to a population, but reality often presents challenges that require practical adjustments.

### Key Points:
1. **Assumptions and Practicality**:
   - Statistical models rely on assumptions, such as random sampling or normal distribution.
   - In real-world scenarios, these assumptions may only be approximately true.

2. **Balancing Theory and Practice**:
   - A good statistician understands both the theoretical principles and the limitations imposed by practical conditions.

### Example:
In an election, while statistical theory assumes a perfectly random sample, practical challenges like non-responses or sampling biases can affect the results. Adjusting for these discrepancies is key to ensuring accurate predictions.

---

## 1.6 Summary

The first chapter introduces the purpose and importance of statistics in addressing real-world problems. It highlights the following:

- **Definition**: Statistics is the science of collecting, analyzing, and interpreting data to make informed decisions.
- **Population and Sample**:
  - **Population**: The complete set of data of interest.
  - **Sample**: A subset of the population used to make inferences.
- **Graphical Methods**: Histograms are used to visually represent data distributions and provide insights into variability and central tendencies.
- **Numerical Methods**:
  - Measures like **mean** and **variance** summarize data.
  - The **empirical rule** helps describe the spread of mound-shaped distributions.

### Mathematical Summary:
1. **Sample Mean**:
   The sample mean is calculated as:
   $$ \bar{y} = \frac{1}{n} \sum_{i=1}^n y_i $$
   where $n$ is the number of observations, and $y_i$ are the data values.

2. **Sample Variance**:
   The sample variance measures the spread of data around the mean:
   $$ s^2 = \frac{1}{n-1} \sum_{i=1}^n (y_i - \bar{y})^2 $$

3. **Standard Deviation**:
   The standard deviation is the square root of the variance:
   $$ s = \sqrt{s^2} $$

4. **Empirical Rule**:
   For a normal distribution:
   - Approximately $68\%$ of the data lies within $ \mu \pm \sigma $.
   - Approximately $95\%$ lies within $ \mu \pm 2\sigma $.
   - Almost all data lies within $ \mu \pm 3\sigma $.
