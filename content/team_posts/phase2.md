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
showAuthorsBadges: true
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

### HDI Model

For our second persona, we planned on creating a linear regression model to predict HDI (Human Development Index) based on 3 features: educational spending as a percentage of total spending, foreign aid spending, and military spending. 

![img](https://i.ibb.co/k606n9cG/Screenshot-2025-05-27-at-11-22-04-PM.png)

We plotted the HDI index for every country to get a general idea of the trends of the data. The API we used didn’t have consistent intervals (ie. data was annual for the last 3 years than intervals in 5 or 10 with many missing data points in the earlier years for most countries). However the data seems to follow a slight trend upwards, which would make sense because countries should develop over time. 

We then explored each of our features and their correlation with HDI. We used scatterplots to find a general sense of the correlation and linearity of the relationship between percentage of total spending on educational spending and a country’s HDI index. 

![img](https://i.ibb.co/GQ0DxBCc/Screenshot-2025-05-27-at-11-22-42-PM.png)

These plots show a linear correlation, however the correlation is much weaker in the later years. This makes sense because many factors contribute to predicting a country’s HDI; however, there is still a significant correlation and we plan on using this as a feature.

For our second feature we planned on looking at foreign aid spending as a predictor for a country’s HDI. The data we found categorized foreign aid spending by category (ie. Export Credits, Grants, Development Assistance) and by country. We started by plotting by year the foreign aid compared to HDI, and the scatterplots show a low correlation between the features.  

![img](https://i.ibb.co/TB7LSQkK/Screenshot-2025-05-27-at-11-23-23-PM.png)
![img](https://i.ibb.co/fVLs6bQ3/Screenshot-2025-05-27-at-11-24-01-PM.png)
![img](https://i.ibb.co/C585vdw8/Screenshot-2025-05-27-at-11-24-22-PM.png)

We also explored the relationship between different categories of foreign aid spending and its relationship with HDI. This also didn’t have strong correlation for each of the categories. Additionally all of this data was for European countries specifically, so it wouldn't be as comprehensive for a global model.

![img](https://i.ibb.co/wZjdV1YK/Screenshot-2025-05-27-at-11-24-39-PM.png)

For our third feature we planned on finding the relationship between military spending as a percentage of GDP and the HDI of a country. However, this data also didn’t seem to have a high correlation.

![img](https://i.ibb.co/zhpvh70F/Screenshot-2025-05-27-at-11-24-55-PM.png)
![img](https://i.ibb.co/whcjKrff/Screenshot-2025-05-27-at-11-25-09-PM.png)

One reason these features may not have a strong correlation with HDI is because HDI is a complicated metric that is based on many different factors. Additionally, it's difficult to predict a country’s HDI on the basis of attributes of their foreign policy and not other attributes of the country (GDP, region). Moving forward, we plan on finding out how these features affect our final ML model's accuracy and potentially find more datasources to predict the HDI. 



## ER Diagrams
ER Diagrams, or Entity Relationship Diagrams, are a useful step in brainstorming for the structure of a relational database. In our case, we wanted to find the best way to connect data sources for features used by all of our user personas with minimal redundancy, which resulted in the following structure. The structure may be modified in the future, but our current database was formed using these 4 diagrams.

**Sun Yeu**
![img](https://i.ibb.co/jPLq6j9N/Screenshot-2025-05-27-at-10-52-25-PM.png)

**Eleanore Goosens**
![img](https://i.ibb.co/tTspPJdQ/Screenshot-2025-05-27-at-10-55-42-PM.png)

**Andrew Thornton**
![img](https://i.ibb.co/R4NXCTwN/Screenshot-2025-05-27-at-10-57-49-PM.png)


