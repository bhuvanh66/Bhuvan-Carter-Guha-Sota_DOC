---
title: "Project - Phase 3"
date: 2025-05-26
draft: false
description: "Time to Build"
slug: "phase3post"
tags: ["project", "Setup"]
authors:
  - "Guha Mahesh"
  - "BhuvanHospet"
  - "SotaShimizu"
  - "CarterVargas"
showAuthorsBadges: true
---

# Phase 2

### Changes from Phase 2:

- After speaking with our professors, we cleaned the concepts for our three user personas:
    - We now have switched the student to an Economist
    - We have also cemented the different interactions between the different personas
    - We have fully comitted to our app being Economic Policy related as opposed to all policy.
- We added our wireframes as we didn't have them in our previous blog post
- We corrected our features and targets on the second model to be Fiscal policy such as government spending, and the features are percent of GDP that the government spent on various different sectors


### Features for the Machine Learning Models

#### Model 1: GDP Per Capita (Linear Regression)

#### Model 2: S&P Index and Currency Exchange Rates (Linear Regression)
The features for this model included:
- Federal Discount Rate for the United States
- The Federal Balance Sheet Size (Billions $)
- Treasury Securities Holdings (Billions $)
- The Lagged Months: 1mo, 2mos, 3mos, 6mos, 9mos
We played around with various monetary policy features in addition to Net Export data. However, the net export data didn't match up with the theme of monetary and fiscal policy. Additionally, the federal funds rate seemingly didn't have as much correlation



#### Model 2 Plots

##### QQ Plots:
![image](https://i.ibb.co/spdZ8JRx/Screenshot-2025-06-04-at-10-40-37-PM.png)
Before testing other assumptions, we decided to check for normality in the residuals. As you can see in the six residual QQ plots, the points generally lie close to a straight line, with minimal variability around the line. This suggests that the residuals are approximately normally distributed.
##### Assumption Plots


## S&P 500 Model Diagnostics
<iframe src="{{ "assets/s&p_500_model_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>

## Euro Model Diagnostics
<iframe src="{{ "assets/euro_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>

## Japanese Yen Model Diagnostics
<iframe src="{{ "assets/japanese_yen_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>

## Australian Dollar Model Diagnostics
<iframe src="{{ "assets/australian_dollar_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>

## Chinese Yuan Model Diagnostics
<iframe src="{{ "assets/chinese_yuan_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>

## British Pound Model Diagnostics
<iframe src="{{ "assets/british_pound_diagnostics.html" | relURL }}" width="100%" height="800"></iframe>



 


