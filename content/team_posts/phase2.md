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

# Phase 2

After receiving feedback on Phase 1 of the project, our group decided to make major revamps to our project to expand the scope beyond currency exchange rates. Using the original idea, we kept one persona designated to analyze how policy will affect exchange rates in addition to stock indexes and HDI. The other two personas we created for people also interested in drafting policy, specifically a lobbyist and a student researcher. Furthermore, we added even more datasets on international data such as education and foreign aid investments

Additionally we added the information and screenshots regarding the new data sources we are using. These include:
- new monetary policy sources
- new data regarding education and millitary spending



### Economic Models

#### Correlation Plot for Model 1



![img](https://i.ibb.co/0VB61zXp/Screenshot-2025-05-27-at-9-17-45-PM.png)

As part of creating the 3 machine learning models for the first persona, we needed to first display our correlations for the data based on our features. For predicting the S&P 500 off of different monetary policies and Net Exports, we created 4 different plots
to show the linear trends by graphing the Normalized S&P predicted value on the Y and the normalized feature on the X . 
We used the following features to train the models:
- Exports Import Data 
- Average Treasury Securities Data  
- Average Discount Rate Data 
- Federal Reserve Balance Data  
As you can see, there is a strong linear trend for all 3 of these features and a weaker trend for the average discount Rate (which still indicates a slight linear trend). 
![img](https://i.ibb.co/YF9NhwJT/Screenshot-2025-05-27-at-9-45-52-PM.png)

After completing a linear regression, we actually found an extremely high $r^2$ value .97 and an MSE of .028, indicating a strong model.

 
#### Correlation Plot for Model 2

![img](https://i.ibb.co/0ySTC49j/Screenshot-2025-05-27-at-9-45-03-PM.png)
Again, we used the same features to view the trends between the EUR/USD rates and the corresponding features. As you can see, there is once again linear patterns amongst the four graphs; however, the patterns seem to be weaker, but we haven’t done a linear regression with this data yet as the API was lagging behind due to excessive usage for testing. 

#### Our Choices
 We weren't completely confident in the correlation between our features and our targets, so we decided to do simple plots showing our target values against our features, which proved our concerns to be somewhat unfounded as there seemed to be a clear correlation for both models in the economic portion of Persona 1

#### Preparing for our model
Because the data for all of the sources came from the same data source, we created a function that essentially returned the cleaned dataframe based off the input code for FRED (the database we got the data from). After this, we found the lower and upper bounds for the tomes of all the data and chose the smallest range so that all the data would be trained over the same historic range. After merging the frames together on the date column, we got rid of the values that were historically outliers or data that resulted in skewed charts until we saw the time period with a linear pattern. The datapoints tended to report the the years 2000-2010 as 0 for many values, and thus we had to exclude them from the plot even if all the datasets contained values for those years. Overall, the data seems to set us up for two strong models as long as we handle the assumptions well. 

![img](https://i.ibb.co/nNMfxfT3/Screenshot-2025-05-27-at-10-16-11-PM.png)
## Residual Plot
As we already built a model for the first economic model, we decided to look at the residual plot to prepare ourselves for the next phase and meeting our assumptions. As you can tell, the residual plots have given us revealed some heteroscedasticity; however these are a products of the High leverage **X-Outliers** as there are some X coordinates that don't match up with the other points. We may need to adjust for this later on.