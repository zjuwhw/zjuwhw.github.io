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
- **Rough statement**: No matter what the list, the vast majority of entries will be in the range **average ± a few SDs**
- **Precise statment**: No matter what the list, a proportion of at least 1-1/k<sup>2</sup> of the entries will be in the range **average ± a few SDs**

```
Typical use

Age: average 20 years, SD 5 years.
What percent are more than 80 years old?

Markov's bound:
at most 25% (1/k, k = 80/20 = 4)

Chebychev's bound: 
at most 0.7% (1/k^2, k=(80-20)/5 = 12)

In conclusion, both bounds are correct.
But Chebychev's bound is much sharper.
Because it uses the SD, not just the average.
```

#### 4.4 Changing units of measurement; standard units

- Mechanics of changing units
	- Multiplying by a constant, e.g. centimeters = 2.54 * inches
	- Mutliplying by a constant, then adding a constant, e.g. ◦F = (9/5)◦C + 32
	- Can also first add a constant, then mulitple by a constant, e.g. new variable = (old variable + b) * a
- Adding a constant
	- new average = old everage + constant
	- new SD = old SD
- Multiplying by a constant
	- new average = old average * constant
	- new SD = old SD * |constant|
- Linear transformations: new list = a * (old list) + b
	- new average = a * (old average) + b
	- new SD = |a| * (old SD)
- Standard units: the z-score
	- z = (x - average)/SD
	- x = z * SD + average
	- z measures "how many SDs above average"
	- the average of any list in standard units is 0
	- the SD of any list in standard units is 1
	- the vast majority (at least 8/9) of any list in standard units will be in the range -3 to 3

### 5 The normal curve

#### 5.1 Bell shaped curves; the standard normal curve

-  A bell shaped distribution

![](/images/Bell_shaped.png)

-  The standard normal curve

![](/images/standard_normal_curve.png)

![](/images/standard_normal_curve_density.png)

```
Useful to remember

total area = 1
balance point: z=0
points of inflection: z=-1, z=1

Central areas:
between z=-1 and z=1: about 68%
between z=-2 and z=2: about 95%

Tail areas:
to the left of -1: about 16%
to the right of 1: about 16%
to the left of -2: about 2.5%
to the right of 2: about 2.5%

Percentiles:
95th percentils: z=1.65, roughly
5th percentile: z=-1.65, roughly
```

#### Normal curves: relation to the standard normal

- The normal curve withe mean μ and SD σ

![](/images/normal_curve_density.png)

- Finding a percent under a normal curve

```
For a list with average 67 and SD 3,
what percent are between 63 and 67?

(63-67)/3 = -1.33 standard units
67 = 0 standard units

So, the question becomes:
Under standard normal curve,
what percent are between -1.33 and 0?

The applet says the area is 40.82%.
In R, the expression is "pnorm(0) - pnorm(-1.33)"
```

## Appendix: The Greek Symbols

![](/images/Greek_Symbol.png)