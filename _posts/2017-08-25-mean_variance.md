---
layout: post
title: mean, variance, covariance and correlation
date: 2017-08-25
tags: ["statistics"]
---

## Descriptive statistics

### one variable



|statistic|$X$|$X+c$|$c \times X$| $scale(X) = \frac{X-mean(X)}{SD(X)}$|
|:--|:--:|:--:|:--:|:--:|
|mean|$\frac{\sum{x_i}}{n}$|mean(X) + c|$c \times mean(X)$|0|
|SS (Sum of Squares)|$\sum{(x_i - \bar{x})^2} $<br> $=\sum{x_i^2} - n\bar{x}^2$|$SS_X$|$c^2 \times SS_X$|n-1|
|Var (Variance)|$\frac{\sum{(x_i - \bar{x})^2}}{n-1}$|Var(X)|$c^2 \times Var(X)$|1|
|SD (Standard Deviation)|$\sqrt{\frac{\sum{(x_i - \bar{x})^2}}{n-1}}$|SD(X)|$c \times SD(X)$|1|



### two variables

|statistic|$X,Y$|$X+c,Y$|$c \times X,Y$|$scale(X), scale(Y)$|
|:--|:--:|:--:|:--:|:--:|
|SS (Sum of Squares)|$\sum(x_i-\bar{x})(y_i-\bar{y})$<br> $= \sum{x_iy_i - n\bar{x}\bar{y}}$|$SS_{XY}$ |$c \times SS_{XY}$|$(n-1) \times  Cor(X,Y)$|
|Cov (Covariance)   |$\frac{\sum(x_i-\bar{x})(y_i-\bar{y})}{n-1}$ |Cov(X,Y)|$c \times Cov(X,Y)$|Cor(X,Y)|
|Cor (Correlation)   |$\frac{\sum(x_i-\bar{x})(y_i-\bar{y})}{\sqrt{\sum(x_i-\bar{x})^2 \times \sum(y_i-\bar{y})^2}}$|Cor(X,Y)|Cor(X,Y)|Cor(X,Y)|


## Random Variables

### expected value or mean:

$$E(X) = \sum x_if(x_i)$$

### variance

$$Var(X) = \sum (x_i - \mu)^2 f(x_i) $$

$$ Var(X)= E((X-E(X))^2) = E(X^2) - (E(X))^2$$

### covariance

$$Cov(X,Y) = \sum(x_i - \mu_x)(y_i - \mu_y)f(x_i, y_i)$$

$$Cov(X,Y) = E((X-E(X))(Y-E(Y))) = E(XY) - E(X)E(Y)$$

## SLR (simple linear regression)

the normal error regression model:

$$Y = \beta_0 + \beta_1X + \epsilon$$

the estimation of regression function:

$$\hat{Y_i} = b_0 + b_1X_i\text{, with }b_1 = \frac{SS_{XY}}{SS_X}, b_0 = \bar{Y} - b_1\bar{X}$$

the sampling distributon

$$b_1  \sim N(\beta_1,\sigma^2(b_1))\text{, so } \frac{b_1 - \beta_1}{\sigma(b_1)} \sim N(0,1)\text{, with }\sigma^2(b_1) = \frac{\sigma^2}{SS_X}$$

$$\frac{b_1 - \beta_1}{s(b_1)} \sim t(n-2)\text{, with }s^2(b_1) = \frac{MSE}{SS_X}$$

|statistic|$X,Y$|$X, scale(Y)$|$scale(X), Y$|$scale(X),scale(Y)$|
|:--|:--:|:--:|:--:|:--:|
|$b_1$|$\frac{\sum(x_i-\bar{x})(y_i - \bar{y})}{\sum{(x_i-\bar{x})^2}}$|$\frac{b_1}{SD(Y)}$|$b_1SD(X)$|$b_1\frac{SD(X)}{SD(Y)} = Cor(X,Y)$
|$\hat{Y_i}$|$b_0+b_1X_i = \bar{y}+\frac{\sum(x_i-\bar{x})(y_i - \bar{y})}{\sum{(x_i-\bar{x})^2}}(x_i - \bar{x})$|$\frac{\hat{y_i}-\bar{y}}{SD(y)}$|$\hat{Y_i}$|$\frac{\hat{y_i}-\bar{y}}{SD(y)}$|
|SSTO($SS_Y$)|$\sum(Y_i - \bar{Y})^2$|$\frac{SSTO}{Var(Y)}$|SSTO|$\frac{SSTO}{Var(Y)}$|
|SSE|$\sum(Y_i - \hat{Y_{i}})^2$|$\frac{SSE}{Var(Y)}$|SSE|$\frac{SSE}{Var(Y)}$|
|MSE|$\frac{\sum(Y_i - \hat{Y_i})^2}{n-2}$|$\frac{MSE}{Var(Y)}$|MSE|$\frac{MSE}{Var(Y)}$|
|SSR|$\sum(\hat{Y_i}-\bar{Y})^2$|$\frac{SSR}{Var(Y)}$|SSR|$\frac{SSR}{Var(Y)}$|
|$R^2$|$1-\frac{SSE}{SSTO} = \frac{SSR}{SSTO} = Cor(X,Y)^2$|$R^2$|$R^2$|$R^2$|
|$s(b_1)$|$\sqrt{\frac{MSE}{SS_X}}$|$\frac{s(b_1)}{SD(Y)}$|$s(b_1)SD(X)$|$s(b_1)\frac{SD(X)}{SD(Y)}$
|t|$\frac{b_1}{s(b_1)} = \frac{SS_{XY}}{\sqrt{MSE}\sqrt{SS_X}} = \pm\sqrt{(n-2)\frac{R^2}{1-R^2}}$|t|t|t|

## Notes

###  *t*<sup>2</sup> and *R*<sup>2</sup>

$t^2 = \\frac{b\_1^2}{s(b\_1)^2} = \\frac{\\frac{SS\_{XY}^2}{SS\_X^2}}{\\frac{MSE}{SS\_X}} = \\frac{SS\_{XY}^2}{MSE \\times SS\_X} = (n-2)\\frac{SS\_Y}{SSE}R^2 = (n-2)\\frac{R^2}{\\frac{SSE}{SS\_Y}} = (n-2)\\frac{R^2}{1-R^2}$

When n is large, t(n-1) --&gt; N(0,1), so *t*<sup>2</sup> --&gt;
*χ*<sub>1</sub><sup>2</sup>.

###  terminology

-   SSTO: total sum of squares
-   SSE: error/residual sum of squares
-   SSR: regression sum of squares
-   MSE: error/residual mean squares
-   *b*<sub>1</sub>: the point estimator of *β*<sub>1</sub>, effect size
-   *s*(*b*<sub>1</sub>): the standard error of *b*<sub>1</sub>, the
    estimated variance of *b*<sub>1</sub>

## R code example

    lm_example = function(x,y){
      xmin = min(x); xmax = max(x)
      fit_lm = lm(y~x)
      b0 = fit_lm$"coefficient"[1]
      b1 = fit_lm$"coefficient"[2]
      yhat = x*b1 + b0
      yhat1 = yhat[1]
      SSTO = sum((y - mean(y))^2)
      SSE = sum(fit_lm$residuals^2)
      MSE = SSE/(length(y)-2)
      SSR = sum((yhat - mean(y))^2)
      R = cor(x,y)
      Rsq = 1 - SSE/SSTO
      s_b1 = summary(fit_lm)$coefficients[2,2]
      t = summary(fit_lm)$coefficients[2,3]
      p = summary(fit_lm)$coefficients[2,4]
      #plot(x,y)
      #lines(c(xmin, xmax),c(b0+xmin*b1, b0+xmax*b1),col="red")
      data = data.frame(b1,yhat1,SSTO,SSE,MSE,SSR,R,Rsq,s_b1,t)
      return(data)
    }
    x = trees$Height
    y = trees$Girth
    data = cbind(t(lm_example(x,y)),t(lm_example(x,scale(y))),t(lm_example(scale(x),y)),t(lm_example(scale(x),scale(y))))
    colnames = c("x_y","x_scy","scx_y","scx_scy")
    data

    ##                 x           x           x          x
    ## b1      0.2557471  0.08149644   1.6295728  0.5192801
    ## yhat1  11.7139043 -0.48897864  11.7139043 -0.4889786
    ## SSTO  295.4374194 30.00000000 295.4374194 30.0000000
    ## SSE   215.7721895 21.91044621 215.7721895 21.9104462
    ## MSE     7.4404203  0.75553263   7.4404203  0.7555326
    ## SSR    79.6652299  8.08955379  79.6652299  8.0895538
    ## R       0.5192801  0.51928007   0.5192801  0.5192801
    ## Rsq     0.2696518  0.26965179   0.2696518  0.2696518
    ## s_b1    0.0781583  0.02490594   0.4980101  0.1586960
    ## t       3.2721686  3.27216859   3.2721686  3.2721686
