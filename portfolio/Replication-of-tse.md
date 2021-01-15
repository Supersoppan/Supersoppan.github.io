---
layout: post
Title: Replication of Tse
tags: [jekyll theme, jekyll, tutorial]
math: true
---
# Replication of Tse

## 1. Introduction
Replication in economics is primarily done to see if a model or method is applicable for further use
outside the specific data set. This paper aims to analyse Tse’s (1998) manner of estimating CV of the
exchange rate and verifying whether we arrive at the same inconclusive results of Tsui and Ho (2004)
who argue that there exists a significant difference between fractionally integrated and stable models.
They also augment Tse’s (1998) research with additional currency pairs and by splitting the data set in
multiple periods, finding that there exists asymmetric volatility in the exchange rate.
The remaining part of this paper consists of 3 sections. Section 2 gives a theoretical background to the
models used in the analysis and a brief description of the data. This is followed by Section 3 that is
divided in 3 subsections, each for 3 time periods used in the analysis. Finally, a section with
conclusions ends this replication assignment with a discussion on our findings and a comparison with
the previous literature.
## 2. Estimation Process
To continue the process of estimating CV, we firstly introduce (G)ARCH models in various settings,
i.e, controlling for integration and asymmetric powers and indicate their differences.
An Overview on GARCH
After observing the existence of volatility clustering in time series, Robert Engle in 1982 introduced
the ARCH (q) model account for this behaviour. However, as in practice, large q lags are required to
capture time volatility, thus a more generalized approach was introduced to allow for the conditional
variance to depend upon its own lags, i.e., Generalized ARCH ( p,q ), see eq. 1 - 3 (Westerlund, 2019).

$$ y_t = μ + ε_t (1) $$

$$ε_t = \sqrt{h_tv_t} (2) $$

$$h_t = α_0 + α_1ε^2_{t-1}+ ...α_q ε^2_{t-h}+\beta_1h_{t-1}+ .. \beta_ph_{t-p} (3) $$

Equation (1) denotes mean equation for the time-series of interest, (2) is variance equation for errors,
whilst \\\( v_t \sim iid(0,1) \\\), lastly (3) shows the full ARMA composition of \\\(h_t\\\)  in the error term. Sum of both
α or β coefficients should be less than 1 for stationarity. 
### An Overview on APARCH
The asymmetric-power ARCH (APARCH) model is a set of models introduced in 1993 by Engle, et
al. The APARCH models, while combining other models in one framework, additionally captures
asymmetry in return volatility. That is, volatility tends to increase more when returns are negative, as
compared to positive returns of the same magnitude (Gentle, 2014). For this model, only variance
equation differs as we can see in (4) (Tsui and Ho, 2004):


You can [download this paper](https://supersoppan.github.io/portfolio/Replicaiton-of-tse.pdf) here.

<a href="/portfolio/pdf/Replication-of-tse.pdf" target="_blank">PDF.</a>