---
layout: project
title: 'Time Series Analysis Final Project'
caption: >
  Prediction of suicide rate in South Korea using ARIMA model fitting and causality analysis using Vector Autoregression model.
description: >
  ARIMA (Auto-regressive Integrated Moving Average) model was fitted through time series analysis of Korea suicide rate data, and prognosis prediction was performed based on the fitted model. Normality was confirmed in the primary differential data, and the model was fitted based on auto.arima, AIC, and BIC. 
  As a result, it was confirmed that all three ARIMA models selected as the three criteria showed similar predictive values. By fitting a vector autoregression (VAR) model, we also confirmed the causal relationship between the suicide rate and the rate of people with depression.
date: 1 Jun 2020
image: 
  path: /assets/img/projects/time_series.PNG
  srcset: 
    1920w: /assets/img/projects/time_series.PNG
    960w:  /assets/img/projects/time_series.PNG
    480w:  /assets/img/projects/time_series.PNG
links:
  - title: Link
    url: https://qwtel.com/
sitemap: false
---

**AIC, BIC reference model fit and model diagnosis**

![SARIMA fitting](../assets/img/projects/time_series_modelfit.PNG){:width="600" height="398" loading="lazy"}

Observed and ARIMA fitted number of depression patients
{:.figcaption}

Similarly, for depression data, p=0,1,2 / d=0,1 / q=0,1,2 / P=0,1,2 / D=0 to find the most appropriate model based on AIC and BIC criteria. ,1 / Q=0,1,2 The multiplicative seasonal model ( ARIMA(p,d,q)(P,D,Q)[12] ) is fit for a total of 324 cases, and the most We have identified which models have small AIC and BIC. As a result, the model that minimizes AIC is
 
It was found that ARIMA(2,1,1)(1,0,1)[12] and the model that minimizes BIC is ARIMA(0,1,1)(1,0,0)[12]. Residual analysis was also performed on this fitted model, and it can be seen that the graph above is a plot fitted based on actual depression data and AIC, showing a similar trend.


 As a result of the residual analysis, in the case of the ARIMA(2,1,1)(1,0,1)[12] model set based on AIC, it was confirmed that there was no special pattern in the residuals through the residual plot, ACF, and residual histogram, and Ljung The p-value of the -box test was also 0.5663, confirming that the residuals satisfy the assumption of independence. However, it can be confirmed that both extremes of the Q-Q plot are far from the normal distribution, and the p-value of the Shapiro-Wilk test is also very small, 0.0077, indicating that the residuals do not satisfy the assumption of normality for this model.
 
**Suicide Rate and Depression Causality Test**

Suicide and depression are closely related, and if the two have causality, data on the proportion of depressed patients can be used to predict the suicide rate. The causal relationship between suicide rate and depression was checked using VAR (Vector Autoregression) model.

First, looking at the types of causality, Granger causality means that when there are two time series A and B, if A causes B granger, it is more significant to predict using the past value of A in predicting B. That is, the change in B can be predicted from the change in A. Instantaneous causality is that predicting the current A value using the current B value rather than the past value gives more information.

$$
E(y_{1,t}|y_{1,t-1},y_{2,t-1},\dots) \neq E(y_{1,t}|y_{2,t},y_{1,t-1},y_{2,t-1},\dots)
$$

Instantaneous casuality
{:.figcaption}

$$
E(y_{1,t}|y_{1,t-1},y_{2,t-1},\dots) \neq E(y_{1,t}|y_{2,t},y_{1,t-1},y_{2,t-1},\dots)
$$

VAR(p) Model
{:.figcaption}



**Results**

The biggest significance of the project is that it drew meaningful results by approaching the qualitative problem of suicide rate from a quantitative point of view. Suicide is a very personal choice, and the causes and motives vary from person to person. Also, depression, which accounts for the largest proportion of suicide motives, is a psychological disease, and it is difficult to explain both the cause and process. 

The greatest significance is that regularity over time was discovered based on the numerical indicators (suicide rate and number of depressed patients) of the study subjects combined with these complex factors. In addition, the causality test was conducted to show a deeper correlation from the results rather than the time series analysis, and new correlations were found in the testing process.