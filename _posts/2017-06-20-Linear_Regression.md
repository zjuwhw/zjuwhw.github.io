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
	- covariance$\sigma(\varepsilon_{i}, \varepsilon_{j}) = 0$, for all i, j; $i \neq j$

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
	- $\sum \hat{Y}_{i}e_{i} = 0$
	- the regression line always goes through the point $(\bar{X}, \bar{Y})$

#### 1.7 Estimation of Erro Terms Variance $\sigma^{2}$

#### 1.8 Normal Error Regression Model