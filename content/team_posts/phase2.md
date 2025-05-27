---
title: "Project - Phase 2"
date: 2025-05-26
draft: false
description: "Continuing Our Progress"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
  - "Guha Mahesh"
  - "BhuvanHospet"
  - "SotaShimizu"
  - "CarterVargas"
showAuthorsBadges: false
---

# Predicting Value of Currencies Affected by Legislation




# Economic Models

## Economic Model 1



[img](https://i.ibb.co/0VB61zXp/Screenshot-2025-05-27-at-9-17-45-PM.png)

As part of creating the 3 machine learning models for the first persona, we needed to first display our correlations for the data based on our features. For predicting the S&P 500 off of different monetary policies and Net Exports, we created 4 different plots
to show the linear trends by graphing the Normalized S&P predicted value on the Y and the normalized feature on the X . 
We used the following features to train the models:
- Exports Import Data 
- Average Treasury Securities Data  
- Average Discount Rate Data 
- Federal Reserve Balance Data  
As you can see, there is a strong linear trend for all 3 of these features and a weaker trend for the average discount Rate (which still indicates a slight linear trend). 
[img](https://i.ibb.co/YF9NhwJT/Screenshot-2025-05-27-at-9-45-52-PM.png)
After completing a linear regression, we actually found an extremely high $r^2$ value .97 and an MSE of .028, indicating a strong model.

 
## Economic Model 2

[img](https://i.ibb.co/0ySTC49j/Screenshot-2025-05-27-at-9-45-03-PM.png)
Again, we used the same features to view the trends between the EUR/USD rates and the corresponding features. As you can see, there is once again linear patterns amongst the four graphs; however, the patterns seem to be weaker, but we haven’t done a linear regression with this data yet as the API was lagging behind due to excessive usage for testing. 
