---
layout: post
title: P-values under null hypothesis
date: 2017-08-10
tags: ["statistics"]
---

P values are also random variables. The distribution of p values under
null hypothesis should be a uniform one.

    set.seed(1)
    y = rnorm(50)
    ps = c()
    for(i in 1:2000){
      x = rnorm(50)
      p = summary(lm(y~x))$coefficients[2,4]
      ps = c(ps, p)
    }
    hist(ps,breaks=seq(0,1,0.05),col=c("red",rep("white",19)), main = "Distribution of P values under null (2000 replications)", freq=FALSE, xlab="P")

![](/images/pvalue-chunk-1-1.png)

[QQ-plot](https://en.wikipedia.org/wiki/Q%E2%80%93Q_plot) can show the p
values follow an uniform distribution.

    library(car)
    qqPlot(ps, distribution="unif")

![](/images/pvalue-chunk-2-1.png)

Proof
=====

<http://vasishth-statistics.blogspot.com.au/2016/04/a-simple-proof-that-p-value.html>
