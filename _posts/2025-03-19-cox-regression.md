---
layout: post
title: survival analysis and cox-regression
date: 2025-03-19
tags: ["statistics"]
---

More details can be found in my notebook
<https://zjuwhw.github.io/notebook-surivialR/>

-   Survival function, the probability of surviving up to a point t:
    *S*(*t*) = *p**r*(*T*&gt;*t*), 0 &lt; *t* &lt; ∞
-   Hazard function is the instantaneous (瞬间) failure rate:
    $h(t) = \lim\limits\_{\delta \to \infty}\frac{pr(t&lt;T&lt;t+\delta|T&gt;t)}{\delta}$
-   Cumulative distribution function (CDF):
    *F*(*t*) = *p**r*(*T*≤*t*) = 1 − *S*(*t*), 0 &lt; *t* &lt; ∞
-   Probability density function (PDF):
    -   $f(t) = \frac{d}{dt} F(t) = \frac{d}{dt}\[1-S(t)\]=-\frac{d}{dt}S(t)$
    -   *f*(*t*) = *h*(*t*)*S*(*t*)
-   cumulative hazard function, the area under the hazard function up to
    time t:
    -   *H*(*t*) = ∫<sub>0</sub><sup>*t*</sup>*h*(*u*)*d**u*
    -   *H*(*t*) =  − *l**o**g*\[*S*(*t*)\]

Cox-regression

*h*<sub>1</sub>(*t*) = *ψ**h*<sub>0</sub>(*t*); *ψ* = *e*<sup>*z**β*</sup>

-   *β*: the effect size for the covariate

-   *h*<sub>0</sub>(*t*): baseline hazard function; “baseline” means z=0

-   *z* is the covariate

-   *z**β* is called “linear predictor” (log-hazard score)

-   *ψ* = *e*<sup>*z**β*</sup> is hazard ratio

-   baseline cumulative hazard function:
    *H*<sub>0</sub>(*t*) = ∫<sub>0</sub><sup>*t*</sup>*h*<sub>0</sub>(*t*)*d**t*

-   baseline survival function:
    *S*<sub>0</sub>(*t*) = *e**x**p*\[−*H*<sub>0</sub>(*t*)\]

-   survival function for a particular individual with covariate value
    z:
    *S*(*t*|*z*) = \[*S*<sub>0</sub>(*t*)\]<sup>*e**x**p*(*z**β̂*)</sup>

-   absolute risk at time t with covariate value z: 1 − *S*(*t*|*z*)
