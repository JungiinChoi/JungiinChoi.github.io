---
layout: project
title: 'SNU Shuttle Bus Latency<br> Survival Analysis'
caption: Survival Analysis Final Project
description: >
  SNU shuttle bus Latency survival analysis and prediction
date: 1 Dec 2019
image: 
  path: /assets/img/projects/survival_title.PNG
  srcset: 
    1920w: /assets/img/projects/survival_title.PNG
    960w:  /assets/img/projects/survival_title.PNG
    480w:  /assets/img/projects/survival_title.PNG
links:
  - title: Link
    url: https://qwtel.com/
sitemap: false
---

# SNU Shuttle Bus Latency<br> Survival Analysis


# Abstract


The purpose of this study is to quantitatively predict the waiting time by identifying the factors that determine the shuttle bus waiting time by conducting a survival analysis based on the waiting time of the Seoul National University shuttle bus, and ultimately to make a reasonable choice for the shuttle bus user. to provide a valid basis.


The data used in this study is a part of the '19-1 Transportation Survey Census' provided by the 61st Seoul National University Student Association, and records the observation values related to the shuttle bus from May 20-24/27-31. am. To facilitate survival analysis, we assumed the independence between the waiting time of the shuttle bus for each time index and the independence between the censoring time and the waiting time.


 Using the Kaplan-Meier Method, it was checked how the survival function changed according to the bus type (administrator shuttle bus, new engineering building shuttle bus), congestion level, and day of the week, and whether there was a significant difference was tested through log-rank test. . In addition, we checked whether the Weibull distribution assumption is appropriate for the survival function, and through this, the regression function was estimated by fitting the Weibull AFT model. In addition, the Cox-PH model was also fitted to estimate the regression function, and it was confirmed which variables were considered significant. Considering that congestion is a time-varying variable, the Time-Varying Covariate Cox-PH model was also fitted together, and the most suitable model was selected through AIC.
 
 
Through the above analysis, it was found that most of the shuttle bus wait times are around 5 to 15 minutes, and the probability of waiting more than 20 minutes is close to zero. It was confirmed that the waiting time when boarding the engineering shuttle was shorter than that of taking the administrator shuttle, and it was confirmed that the day of the week did not affect the waiting time, and the higher the congestion, the longer the waiting time. Based on the above results, the regression model was fitted with variables such as the type of shuttle bus and the degree of congestion, and as a result of comparing the AIC, it can be concluded that the model in which the waiting time is determined by the degree of congestion (0,1,2,3) is the most suitable. there was.

Therefore, it was found that the waiting time of the shuttle bus can be roughly predicted by understanding the congestion level at the time of waiting in line, and that it is not significantly affected by the type of bus and the day of the week. Since the distribution of waiting time according to congestion is quantitatively provided by the AFT model, it is expected that this will provide a basis for making a more rational choice between boarding the shuttle bus and other options.

figcaption
{:.figcaption}
