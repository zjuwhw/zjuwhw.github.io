---
layout: post
title: Statistics Mooc
date: 2017-05-09
tags: ["统计", "mooc"]
---

This is the notebook for Berkley's Edx course serise - [stat2.1](https://www.edx.org/course/introduction-statistics-descriptive-uc-berkeleyx-stat2-1x), [stat2.2](https://www.edx.org/course/introduction-statistics-probability-uc-berkeleyx-stat2-2x), [stat2.3](https://www.edx.org/course/introduction-statistics-inference-uc-berkeleyx-stat2-3x).

* TOC
{:toc}


## Stat2.1

### 1. Introduction

#### 1.1 Why study descriptive statistics?

- Statistics: The science f drawing conclusions from data
- Descriptive statistics: Describing and summarizing data
- Probability: Understanding and quantifying randomness
- Inference: Making conclusions based on data from random samples

- Graphical descriptions --> Numerical summaries; single variable --> relation between two variables

#### 1.2 Variables terminology

- quantitative variables
- contiuous and discrete
- categorical and qualitative

#### 1.3 Bar graphs: describing categorical data

### 2 The histogram

#### 2.1 Describing one quantitative variable

- Stem and leaf plot

#### 2.2 How to draw a histogram

- show the distribution
- allows for the bariable to be "binned" into unequal intervals

#### 2.3 Units and density

#### 2.4 Percentiles: estimaing from histogram

- famous percentiles
	- 25th percentile = lower quartile
	- 50th percentile = median
	- 75th percentile = upper quartile

#### 2.5 Percentiles: more carefully, from the data

### 3 Measures of Location

#### 3.1 The median and the mode

- Mode: the value that has the highest frequency
- Unimodal: one peak

#### 3.2 The average: calculation and basic properties

- average/mean: add up all the entries in the list, then divide by the number of entries
	- Units of the average: same as the units of the list

#### 3.3 Comparing and combining averages

#### 3.4 The average and the histogram; the average and the median

- The median is unaffected by outliers
- In a right-skewed distribution, the average is greater than the median

#### 3.5 Markov's inequality

- Markov's inequality: If a list has only non-negative entries, then the proportion of entries that are >= k times the average is at most 1/k (k can be any positive number)
- For example:
	- Q: the average age of a group of people is 20 years. What proportion are more than 80 years old?
	- A: The proportion is **at most** 1/4 (k=4)

### 4 Measures of spread

#### 4.1 Range and interquartile range

-  range = maximum - minimum
-  interquartile range (IQR) = upper quartile - lower quartile
-  "The IQR of data is 8 years" means "the middle 50% of the data are distributed over 8 years"

#### 4.2 Deviations from average; the standard deviation (SD)

- deviation from average = value - average
- standard deviation (SD) = root mean square (r.m.s.) of deviations from average
- variance = mean sequare of deviations from average
- The average and the SD have the same units


![](/images/SD_formula1.png)

- The vexed question of n-1

![](/images/SD_formula2.png)

In some situations where you are trying to use the SD of a sample to estimate the SD of the population from which the sample was drawn, then according to some criteria, it might be better to use n-1 instead of n in the denominator.

#### 4.3 Properties of the SD; Chebychev's inequality

- Pafnuty Lvovich Chebychev (1821-1894) 
- Chebychev's inequality: In any list, the proportion of the entries that are k or more SDs away from the average is at most 1/k<sup>2</sup>
- Rough statement: No matter what the list, the vast majority of entries will be in the range **average ± a few SDs**
- Precise statment: No matter what the list, a proportion of at least 1-1/k<sup>2</sup> of the entries will be in the range **average ± a few SDs**

