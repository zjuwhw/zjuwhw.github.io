---
layout: post
title: Statistics Mooc
date: 2017-05-09
tags: ["统计", "mooc"]
---

This is the notebook for Berkley's Edx course serise - [stat2.1](https://www.edx.org/course/introduction-statistics-descriptive-uc-berkeleyx-stat2-1x), [stat2.2](https://www.edx.org/course/introduction-statistics-probability-uc-berkeleyx-stat2-2x), [stat2.3](https://www.edx.org/course/introduction-statistics-inference-uc-berkeleyx-stat2-3x).

* TOC
{:toc}


## Stat2.1 Descriptive Statistics

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

#### 5.2 Normal curves: relation to the standard normal

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

#### 5.3 Approximating data histograms; percentiles revisited

#### 5.4 Not all histograms are bell shaped; Chebychev revisited

### 6 Relation between two variables

#### 6.1 Scatter diagrams

- univariate data: histogram
- bivariate data: scatter diagram
- association: any relation between variables
- positive association
- negative association
- linear association

#### 6.2 The correlation coefficient: calculation and properties

- correlation coefficient (r): a number between -1 and 1; it measures linear association, that is, how tightly the points are clustered about a straight line

![](/images/correlation_coefficent.png)

- r is a pure number with no units
- -1 <= r <= 1
- It doesn't matter if you switch the variables x and y; r stays the same
- Adding a constant to one of the lists, r stays the same
- Multiplying one the lists by a positve constant, r stays the same
- Multiplying just one (not both) of the list by a negative constant, r changes to -r 

#### 6.3 Using r: with cation

- Association is not causation
- r measures linear association
- correlated: **linearly** related
- Even one outlier can have a noticeable effect on r

### 7 Regression

#### 7.1 Estimation; bivariate normal ("football shaped") scatter diagrams

- Estimation: one variable, pick one value to estimate.
	- natural estimate: the average
	- math fact: The r.m.s. of the errors will be smallest if you choose estimator = average.
	- average: least squares estimate
- Estimation: two variables, given the value of one variable, estimate the value of the other
	- If the scater diagram is roughly football shaped, you can assume:
		- the distributions of both the variables are roughly normal
		- the distribution of values in each vertical and horizontal strip is roughly normal

#### 7.2 Regression line: intuition; the equation in standard units; regression estimates

- estimate of y (in standard units) = r * x (in standard units), r is the correlation coefficient

#### 7.3 Regression effect, Galton, and the regression fallacy

#### 7.4 Equation of the regression line

- the equation in three ways

![](/images/regression_equation.png)

### 8 Error in the regression estimate

#### 8.1 Least squares: why the regression line and no other

- How much error?
	- error = vertical distance between the point and the line, for every point in the scatter diagram
	- rough size of error = r.m.s of errors
- regreesion line: least squares line

#### 8.2 The r.m.s error of regression; calculations assuming bivariate normal scatter

- r.m.s. error of regression = r.m.s. of residuals = sqrt(1-r<sup>2</sup>) * SD of y
	- r = 1 or -1: r.m.s. error of regression = 0, which says, scatter is a perfect straight line; regression makes no error.
	- r = 0: r.m.s. error of regression = SD of y, which says, no linear association; regression is the same as using the average.
	- All other r: Regression is not perfect, but better than using the average.
	
|one variable|two variables|
|:--|:--|
|normal curve|football shaped scatter diagram|
|average|regression line|
|SD|r.m.s. error of regression|

- Some useful analogies
	- For about 68% of the points, the regression estimate of correct to within 1 r.m.s. error.
	- For about 95% of the points, the regression estimate is correct to within 2 r.m.s. errors.
- Residual plot
	- the average of the residuals is always 0
	- there is no linear association between the residuals and x
	- the residual plot cannot show any trend or linear relation
	- Good regression: residual plot looks like a formless blob around the horizontal axis

#### 8.3 How regression is commonly used; estimating an "unknown true line"

## Stat2.2 Probability

### 1 the two fundamental rules

#### 1.1 What is probability?

- probability of an event = number of outcomes in the event / total number of outcomes
- Frequency theory, long run proportion
- Many probabilities can't interpreted as long run frequencies, because they are based on experiments that can't be repeated under identical conditions

#### 1.2 Addition rule

- Probabilities are numbers between 0 and 1
- Notation
	- P(A) is read as "the probability that the event A occurs"
	- P(A): "probability of A"
	- P(coin lands heads), P(heads), P(H)
- Venn diagrams
- Addition rule: P(A or B) = P(A) + P(B), if A and B are mutually exclusive.
- inclusion-exclusion formula: P(A or B) = P(A) + P(B) - P(A and B) for all A and B
- Complement rule: P(not A) = 1 - P(A)

#### 1.3 Multiplication rule

- P(B|A): **conditional probability** of B, given that A has happened
- Multiplication Rule: P(A and B) = P(A) * P(B|A) for all A, B

#### 1.4 Problem-solving techniques

- get started on a solution
	- be precise in your use of terminology and notation
	- pay attention to detail
	- avoid rushing to conclusions

#### 1.5 Conditional or unconditional?

#### 1.6 Bayes' Rule

```
P(A) = 0.8; P(B) = 0.2; P(bad|A) = 0.01; P(bad|B) = 0.02

P(A and bad)
 = P(A) * P(bad|A)
 = 0.8 * 0.01 
 = 0.008
P(bad)
 = P(A and bad) + P(B and bad) 
 = P(A) * P(bad|A) + P(B) * P(bad|B) 
 = 0.008 + 0.004 
 = 0.012
P(A|bad)
 = P(A and bad) / P(bad) 
 = 0.008/0.012 
 = 0.67
```

- Bayes'Rule: Use it to find the conditional probability of an event at an earlier stage, given the result of a later stage.

### 2 Random sampling with and without replacement

#### 2.1 Independence

- Definition of conditional probability: P(A and B) = P(A) * P(B|A); P(B|A) = P(A and B)/P(A)
- independent trials
	- tosses of a coin
	- rolls of a die
	- draws with replacement
- dependent trials
	- cards dealt from a deck
	- draws without replacement
- Independent events
	- Two events A and B are independent if P(B|A) = P(B|not A) = P`(B)
	- P(A and B) = P(A) * P(B), if A and B are independent

#### 2.2 Sampling with replacement: the binomial formula（二项分布）

![](/images/binomial_formal.png)

#### 2.3 Sampling without replacement: the hypergeometric（超几何） formula

![](/images/hypergeometric_formula.png)

#### 2.4 Examples

- geometric distribution: waiting time till the first sucess; (1-p)<sup>k-1</sup>*(p) for k = 1, 2, 3...
- negative binomial probabilites

### 3 the law of averages and expected values

#### 3.1 Not the law of averages

- move from exact **calculations** to **approximations**
- Law of averages:
	- As you keep tossing, in the long run you get **about half** heads.
	- It is about the **proportion** of heads being close to 1/2.

#### 3.2 The law of averages

- More formal statment
	- As you keep tossing, in the long run, the chance that the **proportion of heads** is in the range **0.5 ± a fixed amount** goes to 1
	- You can choose the **fixed amount** to be as small as you want, as long as you keep it fixed as the number of tosses goes up.
- Law of large numbers
	- independent, repeated, success-failur trials
	- probability of success on a single trial: p
	- As the number of trials increases, the chance that the proportion of successes is in range **p ± a fixed amount** goes to 1.

#### 3.3 The expected value of a random sum

- Notation:
	- random variables: X, Y
	- the sum of the first n X's: S<sub>n</sub> = X<sub>1</sub> + X<sub>2</sub>+ ... X<sub>n</sub>

```
X: the number of spots on one rool of a die
Probability distribution table for X:
 - spot 1: 1/6
 - spot 2: 1/6
 - spot 3: 1/6
 - spot 4: 1/6
 - spot 5: 1/6
 - spot 6: 1/6

Long run average value of X:
1*1/6 + 2*1/6 + 3*1/6 + 4*1/6 + 5*1/6 + 6*1/6 = 3.5
```

- Expected value of X = expectation of X = E(X)
- Let X<sub>1</sub>, X<sub>2</sub>,..., X<sub>n</sub>, be independent and identically distributed (i.i.d.) random variables, and let S<sub>n</sub> = X<sub>1</sub> + X<sub>2</sub>+ ... X<sub>n</sub>. Then, E(S<sub>n</sub>) = n*E(X<sub>1</sub>)
- Exected value of the binomial, E(X) = np

#### 3.4 The expected value of a random average

### 4 the central limit theorem

#### 4.1 The standard error of a random sum

- Standard error
	- The standard error of **a random variable X** is defined by SE(X) = sqrt(E((X-E(X))<sup>2</sup>)
	- SE(X) measures the rough sie of the chance error in X: roughly how far off X is from E(X)
- Standard deviation
	- The standard deviation of **a list of numbers**: SD = r.m.s. of the deviations from average
	- The SD measures the rough size of the deviations: roughly how far off the numbers are from the average

```
X: one draw at random from 1,2,2,3

X: 
P(X = 1) = 1/4
P(X = 2) = 1/2
P(X = 3) = 1/4
E(X) = 2 = average of the box

X-E(X)
P(-1) = 1/4
P(0) = 1/2
P(1) = 1/4
E(X-E(X)) = 0

(X-E(X))^2
P(0) = 1/2
P(1) = 1/2
E((X-E(X))^2) = 0.5

standard error of X = SE(X) = sqrt(E((X-E(X))^2)) = 0.71
= SD of the box (note: for one draw, n = 1)
```


![](/images/SE.png)

#### 4.2 Probabilities for the sum of a large sample

#### 4.3 The Central limit theorem

#### 4.4 The scope of the normal approximation

### 5 the accuracy of simple random samples

#### 5.1 Errors in random percents and averages

#### 5.2 Sampling without replacement: the correction factor

#### 5.3 Accuracy

## Stat2.3 Inference
 

## Appendix

### Appendix 1 : The Greek Symbols

![](/images/Greek_Symbol.png)

source: [https://zh.wikipedia.org/wiki/%E5%B8%8C%E8%85%8A%E5%AD%97%E6%AF%8D](https://zh.wikipedia.org/wiki/%E5%B8%8C%E8%85%8A%E5%AD%97%E6%AF%8D)

### Appendix 2 : Common Distribution

![](/images/common_distribution_1.png)

![](/images/common_distribution_2.png)

ps: pmf, probability mass function（概率质量函数）; pdf, probability density function（概率密度函数）; mgf, Moment-generating function（动差生成函数）

source: [http://www.stat.tamu.edu/~twehrly/611/distab.pdf](http://www.stat.tamu.edu/~twehrly/611/distab.pdf)