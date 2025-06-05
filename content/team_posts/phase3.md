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

#### QQ Plots:
![image](https://i.ibb.co/spdZ8JRx/Screenshot-2025-06-04-at-10-40-37-PM.png)
Before testing other assumptions, we decided to check for normality in the residuals. As you can see in the six residual QQ plots, the points generally lie close to a straight line, with minimal variability around the line. This suggests that the residuals are approximately normally distributed.

#### Assumption Plots
##### SP500 Before
![image](https://i.ibb.co/6RNxngw7/Screenshot-2025-06-05-at-8-38-59-PM.png)
##### SP500 After
![image](https://i.ibb.co/Hf4JkP1L/Screenshot-2025-06-05-at-8-39-04-PM.png)
As you can see in the first plot, we had very clear patterns in our residual plots and an extremely skewed residual histogram. This is not ideal as it means that our model doesn't meet any of our standards:
- There is no linearity as the residuals are not evenly distributed around 0
- There is no homoscedasticity as the variables are clustered around 0
- There is also heavy autocorrelation as the top right graph clearly moves in a pattern with time.
**However**, after we added 6 different time lag features, the second plot showed much more promising trends
It is important to acknowledge that there is still very clear patterns, but there is a *very* clear improvement over the original. The residuals are much more concentrated around 0 and there is less of a pattern with date/time. Additionaly, the plot portrays a bit more homoscedasticity.

**For the model which uses these same features to predict currency exchanges, there would be too many plots to show effectively, so we aggregated them and showed the averages.**
##### Currencies Before
![image](https://i.ibb.co/nsmvR9Sy/Screenshot-2025-06-05-at-8-38-52-PM.png)
##### Currencies After
![image](https://i.ibb.co/P7BcW3T/Screenshot-2025-06-05-at-8-38-44-PM.png)
 As you can see, the same 6 lag strategy worked very effectively on the Currency data as well. In the first plot, there is a large amount of spread about the histogram in addition to clear homoscedasticity and autocorrelation. The second plot seems to mostly mitigate these with the six lags however.


### Our Integrated ML Model
#### *important to note that these are three stitched screenshots, not one page*
![image](https://i.ibb.co/ycgMLzGY/Screenshot-2025-06-05-at-8-51-35-PM.png)
Here, you can see us selecting our features for both of our ML models (One predicting SP500 and exchanges with Monetary Policy and the other predicting GDP Per Capita with Fiscal Policy)
The frontend has quite a bit of room to be more visually pleasing, but the pages are functional as of now.

## Flask API Routes

Our team has implemented a variety of Rest API Routes that are used across our application. As seen in the table, we have incorportated GET, POST, PUT, and DELETE routes that provide many functionalities to our app.
![image](https://i.ibb.co/1tqW8PfL/Screenshot-2025-06-06-at-12-15-27-AM.png)

"GET" Routes were espeically useful for filtering data from the database. Using queries containing MYSQL code, we were able to use SELECT statements with conditions to display specific policies the databse. Users are then able favorite policies for further research on a different page.
![image](https://i.ibb.co/9HwNvxFw/Screenshot-2025-06-06-at-12-17-13-AM.png)

The "POST" and "Delete" route can also be used here to modify which policies are added and removed from the Favorite_Policies table. Using a foreign key and JOIN command to link the two tables.

## Streamlit

So far, our team has put together three working personas with mostly complete functionality. Each persona contains at least two interactive pages.