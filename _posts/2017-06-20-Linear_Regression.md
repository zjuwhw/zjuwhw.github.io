---
layout: post
title: Linear Regression
date: 2017-06-20
tags: ["statistics"]
---

This is the notebook for the book "[Applied Linear Regression Models](https://www.amazon.com/Applied-Linear-Regression-Models-Student/dp/0073014664)".

* TOC
{:toc}

## Part 1 Simple linear regression

### Chapter 1 Linear regression with one predictor variable

#### 1.1 Relations between variables

- relation
	- *Function relation*: Y = f(X), e.g. total cost = the number of products * cost per product
	- *Statistical relation*: not a perfect one, e.g. performance for 10 employees at midyear and year-end
- variable
	- X: *independent/explanatory/predictor variable*
	- Y: *dependent/response variable*
- plot
	- *scatter diagram/plot*
	- each point represents a *trial* or a *case*

#### 1.2 Regression Models and Their Uses

- History
	- [Sir Francis Galton](https://en.wikipedia.org/wiki/Francis_Galton) in the latter part of 19th century
	- relation between heights of parents and children
	- regression to the mean
- Basic Concepts
	- A regression model
	- two characters:
		- there is a probability distribution of Y for each level of X
		- The means of these probability distribution vary in some systematic fashion with X
	- *regression function*: the systematic relationship
		- *linear*, *curvilinear*, etc.
	- *regression curve*: the graph of the regression function
	- probability distributions: *symmetrical*, *skewed* etc.
- Regression models with more than one predictor variable
- Construction of Regression Models
	- Selection of predictor variables
	- Functional form of regression relation
	- Scope of model
- Uses of regression analysis
	- description
	- control
	- prediction
	- overlap in practice
- Regeression and causality
- Use of Computers

#### 1.3 Simple linear regression model with distribution of error terms unspecified

- Formal statement of model

$$Y_{i} = \beta_{0} + \beta_{1}X_{i} + \varepsilon_{i}$$

where:

- $Y_{i}$ is the value of th response variable in the ith trail
- $\beta_{0}\text{ and }\beta_{1}$ are paramters
- $X_{i}$ is a known constant, namely, the value of the predictor variable in the ith trial
- $\varepsilon_{i}$ is a random error term
	- mean $E(\varepsilon_{i}) = 0$
	- variance $\sigma^{2}(\varepsilon_{i}) = \sigma^{2}$
	- covariance $\sigma(\varepsilon_{i}, \varepsilon_{j}) = 0$, for all i, j; $i \neq j$

- Important features of model

1. $Y_{i}$ contains two components: the constant term $\beta_{0} + \beta_{1}X_{i}$ and the random term $\varepsilon_{i}$. Hence, $Y_{i}$ is a random variable
2. Since $E(\varepsilon_{i}) = 0$, $E(Y_{i}) = E(\beta_{0} + \beta_{1}X_{i} + \varepsilon_{i}) = \beta_{0} + \beta_{1}X_{i} + E(\varepsilon_{i}) = \beta_{0} + \beta_{1}X_{i}$
3. The response $Y_{i}$ in the ith trail exceeds or falls short of the value of the regssion fucntion by the error term amount $\varepsilon_{i}$
4. The erorr term $\varepsilon_{i}$ are assumed to have constant variance $\sigma^{2}$ and $\sigma^{2}(Y_{i}) = \sigma^{2}$
5. The error terms are assumed to be uncorrelated, so are the responses $Y_{i}$ and $Y_{j}$

- Meaning of regression paramters
	- *regrssion coefficients*: the paramters $\beta_{0}\text{ and }\beta_{1}$
	- *the slope of the regression line*: $\beta_{1}$

- Alternative versions of regression model

$$Y_{i} = \beta_{0}X_{0} + \beta_{1}X_{i} + \varepsilon_{i}\text{, where }X_{0} \equiv 1$$

$$Y_{i} = \beta_{0}^{*} + \beta_{1}(X_{i} - \bar{X}) + \varepsilon_{i}\text{, where }\beta_{0}^{*} = \beta_{0} + \beta_{1}\bar{X}$$

#### 1.4 Data for regression analysis

- Observational Data
- Eperimental Data
	- treatment
	- experimental units
- Completely randomized design

#### 1.5 Overview of steps in regression analysis

#### 1.6 Estimation of regression function

- Methods of Least Squares
	- To find estimates $b_{0}$ and $b_{1}$ for $\beta_{0}$ and $\beta_{1}$, respectively, for which Q is a minimum, where $Q = \displaystyle\sum_{i=1}^{n}(Y_{i} - \beta_{0} - \beta_{1}X_{i})^2$.
	- Least Squares Estimators $b_{0}$ and $b_{1}$ can be found in two ways:
		- numerical search procedures
		- analytical procedures

$$b_{1} = \frac{\sum(X_{i} - \bar{X})(Y_{i} - \bar{Y})}{\sum(X_{i} - \bar{X})^2}$$

$$b_{0} = \frac{1}{n}(\sum Y_{i} - b_{1} \sum X_{i}) = \bar{Y} - b_{1}\bar{X}$$

- Proof

The paritial derivatives are

$$\frac{\partial Q}{\partial\beta_{0}} = -2\sum(Y_{i} - \beta_{0} - \beta_{1}X_{i})$$

$$\frac{\partial Q}{\partial\beta_{1}} = -2\sum X_{i}(Y_{i} - \beta_{0} - \beta_{1}X_{i})$$

We set them equal to zero, using $b_{0}$ and $b_{1}$ to denote the particular values of $b_{0}$ and $b_{1}$ that minimize Q:

$$-2\sum(Y_{i} - \beta_{0} - \beta_{1}X_{i}) = 0$$

$$-2\sum X_{i}(Y_{i} - \beta_{0} - \beta_{1}X_{i}) = 0$$

- Proerties of Least Squares Estimators

Guass-Markov theorem:

> Under the conditions of regression model, the least squares estimators b0 and b1 are unbiased and have minimum variance among all unbiased linear estimators

- Point Esitmation of Mean Response
	- estimate the regression function as follows:

	$$\hat{Y} = b_{0} + b_{1}X$$ 

- Residuals
	- residual: the differenc between the observed value $Y_{i}$ and the corresponding fitted value $\hat{Y_{i}}$

$$e_{i} = Y_{i} - \hat{Y}_{i}$$

- Properties of Fitted Regression Line
	- $\sum e_{i} = 0$
	- $\sum e_{i}^{2}$ is a minimum
	- $\sum Y_{i} = \sum \hat{Y}_{i}$
	- $\sum X_{i} e_{i} = 0 $
	- $\sum \hat{Y}_{i}$e<sub>i</sub> = 0
	- the regression line always goes through the point $(\bar{X}, \bar{Y})$

#### 1.7 Estimation of Erro Terms Variance $\sigma^{2}$

- Point Estimator of $\sigma^{2}$
	- Single population
		- sum of squares: $\displaystyle\sum_{i=1}^{n}(Y_{i}-\bar{Y})^2$ 
		- degrees of freedom (df): n - 1, because one degree of freedom is lost by using $\bar{Y}$ as an estimate of the unknown population mean $\mu$
		- sample variance/mean square: $s^2 = \frac{\displaystyle\sum(Y_{i}-\bar{Y})^2}{n-1}$
	- Regression model
		- deviation/residual: $Y_{i} - \hat{Y}_{i}$ = e<sub>i</sub>
		- error/residual sum of squares:
			- $SSE = \displaystyle\sum_{i=1}^{n}(Y_{i} - \hat{Y}_{i})^{2}$
			- $SSE = \displaystyle\sum_{i=1}^{n}e_{i}^{2}$
		- degrees of freedom: n - 2, because two degrees of freedom are lost due to estimating $\beta_{0}$ and $\beta_{1}$ to get $\hat{Y}_{i}$
		- MSE (error/residual mean square): $s^{2} = MSE = \frac{SSE}{n-2}$


#### 1.8 Normal Error Regression Model

- Model
	- same with simple linear regression model
	- except it assumes that the error $\varepsilon_{i}$ are normally distributed
- Estimation of Parameters by Method of Maximum Likelihood

Method of maximum likelihood chooses as estimates those values of the parameters that are most consistent with the sample data.

```
A normal distribution with SD = 10, mean is unknown
A random of sample n = 3 yields the results 250, 265 and 259
The likelihood value (L) is the product of the densities of the normal distribution

If we assue μ = 230, L(μ = 230) = 0.279*10E-9 
R code: prod(dnorm(c(250,265,259), 230, 10))
If we assue μ = 259, L(μ = 259) = 0.0000354
R code: prod(dnorm(c(250,265,259), 259, 10))

So, L(μ = 259) > L(μ = 230)

The method of maximum likelihood is to estimate prarametes to get maximum L.
It can be shown that for a normal population,
the maximum likelihood estimator of μ is the smaple mean
```

Fro regression model, the likelihood function for n observations is 

$$L(\beta_{0}, \beta_{1}, \sigma^{2}) = \displaystyle\Pi_{i=1}^{n}\frac{1}{(2\pi\sigma^{2})^{1/2}}exp[-\frac{1}{2\sigma^{2}}(Y_{i} - \beta_{0} - \beta_{1}X_{i})^{2}]$$

$$L(\beta_{0}, \beta_{1}, \sigma^{2}) = \frac{1}{(2\pi\sigma^{2})^{1/2}}exp[-\frac{1}{2\sigma^{2}}\displaystyle\sum_{i=1}^{n}(Y_{i} - \beta_{0} - \beta_{1}X_{i})^{2}]$$

### Chapter 2 Inferences in Regression and Correlation Analysis

#### 2.1 Inferences Concerning $\beta_{1}$

