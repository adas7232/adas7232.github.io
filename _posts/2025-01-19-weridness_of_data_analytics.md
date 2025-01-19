---
date: Dec 22, 2022
layout: post
title: Weirdnes of data analytics
subtitle: 'Why does this happen?'
usemathjax: true
description: >-
  I came to know about thsi weirdness of data analytics afetr taking a class at EMBA
image: >-
  /assets/img/Data_Analytics/analytics.jpg

optimized_image: >-
   /assets/img/Data_Analytics/analytics.jpg
category: Education
highlight: true
tags:
  - data analytics
  - blog
author: abhijitdas
paginate: true
---
Recently, during one of my Executive MBA classes on data analytics, I stumbled upon some fascinating and rather strange facts about data. While this wasn’t my first introduction to data analytics, I had never really paused to explore its weird and counterintuitive aspects before.

There are so many phenomena around us that we can explain with math, but the “why” behind them remains elusive. Here are a few examples that I found particularly amusing—not necessarily because they’re practical for daily life or work, but because I genuinely can’t wrap my head around why they happen. If you have an explanation, I’d love to hear it!

# The Central Limit Theorem: A Strange Truth of Data

The **Central Limit Theorem (CLT)** is one of the most fascinating ideas in data analytics. It tells us that if you take random samples from any population—no matter how irregular the population distribution—the *sample means* will form a normal distribution (a bell curve) as the sample size increases.

What makes this truly fascinating is that it works even when the original population data is far from normal.

## Example: Tree Heights in a Forest

Imagine a forest with two species of trees:
- **Species A**: Typically grows to around 30 meters tall.
- **Species B**: Generally taller, averaging 50 meters.

If you measure the heights of thousands of trees in the forest, the data won’t follow a simple bell curve. Instead, it will look **bimodal**, with two peaks—one for each species.

Now, if you take random samples of, say, 10, 30, 50, or 100 trees and calculate the average height for each sample, something amazing happens: the distribution of these *sample means* starts to form a normal distribution. The larger the sample size, the closer it gets to a perfect bell curve—no matter how complex the original data is.

### Graph 1: Original Tree Height Distribution
The first graph shows the bimodal distribution of tree heights, reflecting two species with distinct average heights. This represents the raw data.

| ![dist_tree1](\assets\img\Data_Analytics\distribution_of_tree_heights.png) |
|:--:|
| *Distribution Of Tree Heights (Bimodal)* | 

### Graphs 2–5: Sample Means
The subsequent graphs demonstrate the **CLT in action**:
- For smaller sample sizes (e.g., 10), the distribution of sample means starts to smooth out.
- As the sample size grows (30, 50, 100), the distribution of sample means becomes increasingly normal, even though the original data is not.

| ![dist_tree1](\assets\img\Data_Analytics\distribution_sample_means.png) |
|:--:|
| *Distribution Of Sample Means* | 

## Why Is This Useful?

The CLT allows us to make reliable predictions about averages, even when the population data is messy or unpredictable. For example:
- Foresters can estimate the average tree height in a forest by measuring a small sample of trees.
- Businesses can forecast average customer behavior using small samples, even if individual behavior varies wildly.

# Simpson's Paradox: When Data Plays Tricks on You

Simpson's Paradox is a fascinating phenomenon where trends observed in individual groups reverse when the groups are combined. It’s a powerful reminder that data can be misleading if we don’t analyze it at the right level. Let’s explore this with a classic example involving university admissions.

## The Scenario: University Admissions

A university has two departments (A and B), and their acceptance rates for male and female applicants are as follows:

| Department | Male Applicants | Male Accepted | Female Applicants | Female Accepted |
|------------|-----------------|---------------|-------------------|-----------------|
| A          | 100             | 80%           | 400               | 70%             |
| B          | 300             | 30%           | 100               | 20%             |

### Within Departments:
- In **Department A**, males have a higher acceptance rate (80%) than females (70%).
- Similarly, in **Department B**, males also have a higher acceptance rate (30%) than females (20%).

At first glance, it looks like males are consistently favored over females in both departments.

### Combined Data:
Now, let’s calculate the overall acceptance rates. This is where the **number of applicants** in each department starts to play a significant role.

- **Males**:
  - Total accepted: \( (100 \times 0.8) + (300 \times 0.3) = 80 + 90 = 170 \)
  - Total applicants: \( 100 + 300 = 400 \)
  - Overall acceptance rate: \( 170 / 400 = 42.5\% \)

- **Females**:
  - Total accepted: \( (400 \times 0.7) + (100 \times 0.2) = 280 + 20 = 300 \)
  - Total applicants: \( 400 + 100 = 500 \)
  - Overall acceptance rate: \( 300 / 500 = 60.0\% \)

Surprisingly, when the data is combined, **females now appear to have a higher acceptance rate (60%) than males (42.5%)**, reversing the trend seen within the departments!

### Why Does This Happen?

The paradox occurs because the **number of applicants** in each department is uneven:
- More females applied to Department A, which has a higher acceptance rate.
- More males applied to Department B, which has a lower acceptance rate.

This imbalance skews the combined results, creating an apparent reversal.

## Lesson Learned:

Simpson's Paradox is a critical reminder that aggregated data can be deceptive. To avoid being misled:
- Always analyze data at multiple levels.
- Consider how group proportions or sizes might influence combined results.

This paradox isn’t just a mathematical curiosity—it has real implications in fields like medicine, social sciences, and business. Have you encountered a similar scenario where data seemed to play tricks on you? Let me know your thoughts!

# Mixing Low-Risk and High-Risk Assets: A Portfolio Advantage

In portfolio management, it’s counterintuitive but true: combining a small portion of a high-risk asset with a low-risk asset can both **increase returns** and **reduce risk**. Let’s break this down with an example using **T-bills** (low-risk) and **small stocks** (high-risk), inspired by the attached class notes.

## Portfolio Setup

Let’s assume:
- **T-bills**: Expected return = 3.754% (low-risk), variance = 0.00111, standard deviation = 0.03339.
- **Small stocks**: Expected return = 17.488% (high-risk), variance = 0.12277, standard deviation = 0.35030.
- **Correlation** between T-bills and small stocks = -0.09830 (small negative correlation).

We’ll explore three scenarios:
1. **100% in T-bills (low risk)**.
2. **98% in T-bills and 2% in small stocks**.
3. **50% in T-bills and 50% in small stocks**.

## Portfolio Expected Return and Risk

Using the formulas for portfolio expected return and variance:
- **Expected Return**:  
  \[
  E[R] = w_b E[X_b] + w_s E[X_s]
  \]
- **Variance**:  
  \[
  \text{Var}[R] = w_b^2 \text{Var}[X_b] + w_s^2 \text{Var}[X_s] + 2w_bw_s\text{Cov}[X_b, X_s]
  \]

We calculate the portfolio metrics for the three scenarios:

| **Weight in T-Bills (\(w_b\))** | **Weight in Small Stocks (\(w_s\))** | **Expected Return (\(E[R]\))** | **Variance** | **Standard Deviation** |
|---------------------------------|--------------------------------------|--------------------------------|--------------|--------------------------|
| 1.00                            | 0.00                                 | 0.03754                        | 0.00111      | 0.03339                  |
| 0.98                            | 0.02                                 | 0.04029                        | 0.00107      | 0.03278                  |
| 0.50                            | 0.50                                 | 0.10621                        | 0.03038      | 0.17430                  |

## Observations

1. **Moving 2% into Small Stocks (98% T-Bills, 2% Small Stocks)**:
   - **Expected Return** increases from **3.754% to 4.029%**.
   - **Standard Deviation** decreases slightly from **0.03339 to 0.03278**.
   - This creates a portfolio with both higher returns and lower risk than 100% in T-bills.

2. **Equal Allocation (50% T-Bills, 50% Small Stocks)**:
   - The expected return jumps to **10.621%**, but the standard deviation increases to **0.17430**. This shows a higher risk-return tradeoff for more aggressive allocations.

## Why Does This Happen?

This phenomenon occurs because of **negative correlation** and the diversification effect:
- Small stocks are riskier individually, but their returns don’t perfectly correlate with T-bills.
- By mixing the two, the portfolio benefits from the high returns of small stocks while the T-bills stabilize the risk.

## Key Takeaway

A carefully diversified portfolio can deliver **higher returns with lower risk** than holding a single low-risk asset. Even small changes in allocation, like moving 2% from T-bills to small stocks, can significantly enhance portfolio performance while maintaining minimal risk.

Have you experimented with portfolio diversification? Let me know how it worked for you!






