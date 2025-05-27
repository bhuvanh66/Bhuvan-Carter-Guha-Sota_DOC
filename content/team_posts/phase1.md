---
title: "Project - Phase I"
date: 2025-05-15
draft: false
description: "Our Idea"
slug: "phase1post"
tags: ["project", "Setup"]
authors:
  - "Guha Mahesh"
  - "BhuvanHospet"
  - "SotaShimizu"
  - "CarterVargas"
showAuthorsBadges: true
---

# App Name TBD

## Project Description

Public policy is ubiquitous in life and affects almost every aspect of society. Policy makers and government officials play an essential role in passing legislation that alters the economy, education, and aid to foreign countries. Our team has created an app that will assist in the development and implementation of such policy and allow any person interested in international policy, whether that be a lobbyist, research student, or member of government to experiment with various policies. Features of our app include allowing users to draft their own policies regarding foreign aid and education investments and predicting how such actions will affect stock market indexes and values of currencies. Additionally, a data collection feature will allow the user to take notes from a speaker and input ideas. These ideas can be further refined and inputted into the app to determine the best course of action to get the policy proposed. Our app will include 3 machine learning models trained on historical legislative data to make predictions about the outcomes of these policies and draw valuable insights in their effects.


## Personas

**Andrew Thornton** 
Age: 28
Occupation: PHD Candidate at KU Leuven 
Location: Leuven, Belgium
Bio: Andrew is studying policy at university and wants to come up with new ideas for legislation.

- As a student, I want to retrieve historical data on policies passed in the EU.
- As a student, I want to draft my own policy and determine the best course of action for making it implementable in society.
- As a student, I want to compare this policy to historical data and find more information on similar policies.
- As a student, I want to observe what the best practice would be to spread this policy quickly.


**Sun Yue** 
Age: 46 
Location: Paris, France
Occupation: Member of the European Parliament 
Bio: Sun is a Spanish policy maker who is looking to pass legislation that will benefit the European Union as a whole.


- As an MEP, I want to view historical economic data of the Euro and compare how its value has changed over time.
- As an MEP, I want to determine how foreign aid, education spending, and military spending is affecting HDI.
- As an MEP, I want to test potential legislative policies regarding interest rates to see how it will affect the stock market index.
- As an MEP, I want to pass legislation that will only strengthen the value of the Euro.
- As an MEP, I want to analyze imports and exports between countries.


**Eleanore Goossens** 
Age: 45
Location: Paris, France
Occupation: Lobbyist
Bio: Eleanore is a lobbyist interested in keeping track of conversations and key policy ideas that have come up in recent years, and seeing their implications over time.


- As a lobbyist, I want to keep track of previous conversations I had with key politicians regarding policy.
- As a lobbyist, I want to view the historical growth of different energy sources in the EU over the last couple of years.
- As a lobbyist, I want to see the relationship between the
- As a lobbyist, I want to generate graphs that can be used to illustrate historical trends.


## Candidate Data Sources

So far, we have been able to retreive API data regarding the following statistics about Monetary Policy from FRED across a large span of time:

  - Exports Import Data 
  - Average Treasury Securities Data  
  - Average Discount Rate Data 
  - Federal Reserve Balance Data  
Additionally, we have utilized the yfinance Python Library to access the historical closing price of the SP500 market index marked under \['close'] in the below picture.

    ![image](https://i.ibb.co/zWXjMgxp/Screenshot-2025-05-27-at-10-33-03-PM.png)

- Conversion Rates Between Currencies (numerical)
  These sources will essentially give us the labels for the AI data so that we can actually train the model
  - USD to Chinese Yuan
  - USD to Euro
  - USD to British Pound
  - Many other currencies
    ![image](https://i.ibb.co/Pvf19JB2/Screenshot-2025-05-20-at-4-22-23-PM.png)
For training a model which predicts policy's based off previous foreign policies

- The main source of money for Foreign Aid (categorical)
- Money spent on education
- Money spent on Millitary
  ![image](https://i.ibb.co/N26XQnx9/Screenshot-2025-05-27-at-10-39-19-PM.png)
  ![image](https://i.ibb.co/twzFWy3K/foreign-Aid-Fin-Source.png)

