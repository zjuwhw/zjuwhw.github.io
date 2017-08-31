---
layout: post
title: mean, variance and correlation
date: 2017-08-25
tags: ["statistics"]
---

### the measures of one variable

<table style="width:100%;">
<colgroup>
<col width="12%" />
<col width="31%" />
<col width="20%" />
<col width="26%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">statistic</th>
<th align="left"><span class="math inline"><em>X</em></span></th>
<th align="left"><span class="math inline"><em>X</em> + <em>c</em></span></th>
<th align="left"><span class="math inline"><em>c</em> × <em>X</em></span></th>
<th align="left"><span class="math inline">$scale(X) = \frac{X-mean(X)}{SD(X)}$</span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">mean(X)</td>
<td align="left"><span class="math inline">$\frac{\sum{x_i}}{n}$</span></td>
<td align="left">mean(X) + c</td>
<td align="left"><span class="math inline"><em>c</em> × <em>m</em><em>e</em><em>a</em><em>n</em>(<em>X</em>)</span></td>
<td align="left">0</td>
</tr>
<tr class="even">
<td align="left"><span class="math inline"><em>S</em><em>S</em><sub><em>X</em></sub></span></td>
<td align="left"><span class="math inline">$\sum{(x_i - \bar{x})^2} = \sum{x_i^2} - n\bar{x}^2$</span></td>
<td align="left"><span class="math inline"><em>S</em><em>S</em><sub><em>X</em></sub></span></td>
<td align="left"><span class="math inline"><em>c</em><sup>2</sup> × <em>S</em><em>S</em><sub><em>X</em></sub></span></td>
<td align="left">n-1</td>
</tr>
<tr class="odd">
<td align="left">Var(X)</td>
<td align="left"><span class="math inline">$\frac{\sum{(x_i - \bar{x})^2}}{n-1}$</span></td>
<td align="left">Var(X)</td>
<td align="left"><span class="math inline"><em>c</em><sup>2</sup> × <em>V</em><em>a</em><em>r</em>(<em>X</em>)</span></td>
<td align="left">1</td>
</tr>
<tr class="even">
<td align="left">SD(X)</td>
<td align="left"><span class="math inline">$\sqrt{\frac{\sum{(x_i - \bar{x})^2}}{n-1}}$</span></td>
<td align="left">SD(X)</td>
<td align="left"><span class="math inline"><em>c</em> × <em>S</em><em>D</em>(<em>X</em>)</span></td>
<td align="left">1</td>
</tr>
</tbody>
</table>

### the measures of two variables

<table style="width:100%;">
<colgroup>
<col width="12%" />
<col width="31%" />
<col width="20%" />
<col width="26%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">statistic</th>
<th align="left"><span class="math inline"><em>X</em>, <em>Y</em></span></th>
<th align="left"><span class="math inline"><em>X</em> + <em>c</em>, <em>Y</em></span></th>
<th align="left"><span class="math inline"><em>c</em> × <em>X</em>, <em>Y</em></span></th>
<th align="left"><span class="math inline"><em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>X</em>),<em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>Y</em>)</span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span class="math inline"><em>S</em><em>S</em><sub><em>X</em><em>Y</em></sub></span></td>
<td align="left"><span class="math inline">$\sum(x_i-\bar{x})(y_i-\bar{y}) = \sum{x_iy_i - n\bar{x}\bar{y}}$</span></td>
<td align="left"><span class="math inline"><em>S</em><em>S</em><sub><em>X</em><em>Y</em></sub></span></td>
<td align="left"><span class="math inline"><em>c</em> × <em>S</em><em>S</em><sub><em>X</em><em>Y</em></sub></span></td>
<td align="left"><span class="math inline">(<em>n</em> − 1)×<em>C</em><em>o</em><em>r</em>(<em>X</em>, <em>Y</em>)</span></td>
</tr>
<tr class="even">
<td align="left">Cov(X,Y)</td>
<td align="left"><span class="math inline">$\frac{\sum(x_i-\bar{x})(y_i-\bar{y})}{n-1}$</span></td>
<td align="left">Cov(X,Y)</td>
<td align="left"><span class="math inline"><em>c</em> × <em>C</em><em>o</em><em>v</em>(<em>X</em>, <em>Y</em>)</span></td>
<td align="left">Cor(X,Y)</td>
</tr>
<tr class="odd">
<td align="left">Cor(X,Y)</td>
<td align="left"><span class="math inline">$\frac{\sum(x_i-\bar{x})(y_i-\bar{y})}{\sqrt{\sum(x_i-\bar{x})^2 \times \sum(y_i-\bar{y})^2}}$</span></td>
<td align="left">Cor(X,Y)</td>
<td align="left">Cor(X,Y)</td>
<td align="left">Cor(X,Y)</td>
</tr>
</tbody>
</table>

### SLR (simple linear regression)

the normal error regression model:

*Y* = *β*<sub>0</sub> + *β*<sub>1</sub>*X* + *ϵ*

the estimation of regression function:

$$\\hat{Y\_i} = b\_0 + b\_1X\_i\\text{, with }b\_1 = \\frac{SS\_{XY}}{SS\_X}, b\_0 = \\bar{Y} - b\_1\\bar{X}$$

the sampling distributon

$$b\_1  \\sim N(\\beta\_1,\\sigma^2(b\_1))\\text{, so } \\frac{b\_1 - \\beta\_1}{\\sigma(b\_1)} \\sim N(0,1)\\text{, with }\\sigma^2(b\_1) = \\frac{\\sigma^2}{SS\_X}$$
$$\\frac{b\_1 - \\beta\_1}{s(b\_1)} \\sim t(n-2)\\text{, with }s^2(b\_1) = \\frac{MSE}{SS\_X}$$

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="29%" />
<col width="19%" />
<col width="19%" />
<col width="19%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">statistic</th>
<th align="left"><span class="math inline"><em>X</em>, <em>Y</em></span></th>
<th align="left"><span class="math inline"><em>X</em>, <em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>Y</em>)</span></th>
<th align="left"><span class="math inline"><em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>X</em>),<em>Y</em></span></th>
<th align="left"><span class="math inline"><em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>X</em>),<em>s</em><em>c</em><em>a</em><em>l</em><em>e</em>(<em>Y</em>)</span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span class="math inline"><em>b</em><sub>1</sub></span></td>
<td align="left"><span class="math inline">$\frac{\sum(x_i-\bar{x})(y_i - \bar{y})}{\sum{(x_i-\bar{x})^2}}$</span></td>
<td align="left"><span class="math inline">$\frac{b_1}{SD(Y)}$</span></td>
<td align="left"><span class="math inline"><em>b</em><sub>1</sub><em>S</em><em>D</em>(<em>X</em>)</span></td>
<td align="left"><span class="math inline">$b_1\frac{SD(X)}{SD(Y)} = Cor(X,Y)$</span></td>
</tr>
<tr class="even">
<td align="left"><span class="math inline">$\hat{Y_i}$</span></td>
<td align="left"><span class="math inline">$b_0+b_1X_i = \bar{y}+\frac{\sum(x_i-\bar{x})(y_i - \bar{y})}{\sum{(x_i-\bar{x})^2}}(x_i - \bar{x})$</span></td>
<td align="left"><span class="math inline">$\frac{\hat{y_i}-\bar{y}}{SD(y)}$</span></td>
<td align="left"><span class="math inline">$\hat{Y_i}$</span></td>
<td align="left"><span class="math inline">$\frac{\hat{y_i}-\bar{y}}{SD(y)}$</span></td>
</tr>
<tr class="odd">
<td align="left">SSTO(<span class="math inline"><em>S</em><em>S</em><sub><em>Y</em></sub></span>)</td>
<td align="left"><span class="math inline">$\sum(Y_i - \bar{Y})^2$</span></td>
<td align="left"><span class="math inline">$\frac{SSTO}{Var(Y)}$</span></td>
<td align="left">SSTO</td>
<td align="left"><span class="math inline">$\frac{SSTO}{Var(Y)}$</span></td>
</tr>
<tr class="even">
<td align="left">SSE</td>
<td align="left"><span class="math inline">$\sum(Y_i - \hat{Y_{i}})^2$</span></td>
<td align="left"><span class="math inline">$\frac{SSE}{Var(Y)}$</span></td>
<td align="left">SSE</td>
<td align="left"><span class="math inline">$\frac{SSE}{Var(Y)}$</span></td>
</tr>
<tr class="odd">
<td align="left">MSE</td>
<td align="left"><span class="math inline">$\frac{\sum(Y_i - \hat{Y_i})^2}{n-2}$</span></td>
<td align="left"><span class="math inline">$\frac{MSE}{Var(Y)}$</span></td>
<td align="left">MSE</td>
<td align="left"><span class="math inline">$\frac{MSE}{Var(Y)}$</span></td>
</tr>
<tr class="even">
<td align="left">SSR</td>
<td align="left"><span class="math inline">$\sum(\hat{Y_i}-\bar{Y})^2$</span></td>
<td align="left"><span class="math inline">$\frac{SSR}{Var(Y)}$</span></td>
<td align="left">SSR</td>
<td align="left"><span class="math inline">$\frac{SSR}{Var(Y)}$</span></td>
</tr>
<tr class="odd">
<td align="left"><span class="math inline"><em>R</em><sup>2</sup></span></td>
<td align="left"><span class="math inline">$1-\frac{SSE}{SSTO} = \frac{SSR}{SSTO} = Cor(X,Y)^2$</span></td>
<td align="left"><span class="math inline"><em>R</em><sup>2</sup></span></td>
<td align="left"><span class="math inline"><em>R</em><sup>2</sup></span></td>
<td align="left"><span class="math inline"><em>R</em><sup>2</sup></span></td>
</tr>
<tr class="even">
<td align="left"><span class="math inline"><em>s</em>(<em>b</em><sub>1</sub>)</span></td>
<td align="left"><span class="math inline">$\sqrt{\frac{MSE}{SS_X}}$</span></td>
<td align="left"><span class="math inline">$\frac{s(b_1)}{SD(Y)}$</span></td>
<td align="left"><span class="math inline"><em>s</em>(<em>b</em><sub>1</sub>)<em>S</em><em>D</em>(<em>X</em>)</span></td>
<td align="left"><span class="math inline">$s(b_1)\frac{SD(X)}{SD(Y)}$</span></td>
</tr>
<tr class="odd">
<td align="left">t</td>
<td align="left"><span class="math inline">$\frac{b_1}{s(b_1)} = \frac{SS_{XY}}{\sqrt{MSE}\sqrt{SS_X}} = \pm\sqrt{(n-2)\frac{R^2}{1-R^2}}$</span></td>
<td align="left">t</td>
<td align="left">t</td>
<td align="left">t</td>
</tr>
</tbody>
</table>

Notes:

1.  *t*<sup>2</sup> and *R*<sup>2</sup>

$t^2 = \\frac{b\_1^2}{s(b\_1)^2} = \\frac{\\frac{SS\_{XY}^2}{SS\_X^2}}{\\frac{MSE}{SS\_X}} = \\frac{SS\_{XY}^2}{MSE \\times SS\_X} = (n-2)\\frac{SS\_Y}{SSE}R^2 = (n-2)\\frac{R^2}{\\frac{SSE}{SS\_Y}} = (n-2)\\frac{R^2}{1-R^2}$

When n is large, t(n-1) --&gt; N(0,1), so *t*<sup>2</sup> --&gt;
*χ*<sub>1</sub><sup>2</sup>.

1.  terms

-   SS: sum of squares
-   Var: variance
-   SD: standard error
-   Cov: covariance
-   Cor: (Pearson's) correlation coefficient
-   SSTO: total sum of squares
-   SSE: error/residual sum of squares
-   SSR: regression sum of squares
-   MSE: error/residual mean squares
-   *b*<sub>1</sub>: the point estimator of *β*<sub>1</sub>, effect size
-   *s*(*b*<sub>1</sub>): the standard error of *b*<sub>1</sub>, the
    estimated variance of *b*<sub>1</sub>

### R code example

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
