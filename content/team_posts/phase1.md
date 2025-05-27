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
showAuthorsBadges: false
---

# Predicting Value of Currencies Affected by Legislation

## Project Description

Currencies across the world are constantly fluctuating as a result of inflation, foreign market demand, legislative policies, and many other factors. Knowing how these exchange rates change can be critical for international business that affects the price of imported goods for everyday people. Our application will use machine learning to train a model based on how different economic policies have affected these currencies in the past to predict how the Euro will fluctuate with respect to three different currencies: The US Dollar, the Pound Sterling, and the Chinese Yuan. The application will give the user to login as three different personas. The first being a foreign investor investigating how tariffs will affect trade across nations; a domestic importer from the EU looking at how tax rates will affect demand; and a migrant analyzing the implications of expatriating to another country. We will collect data from a variety of sources including FRED, World Bank, and UCDP. Our features will include three types of interest rates, conversion rates, foreign aid, tariffs, and war.


## Personas

**Andrew Thornton** 
Age: 39 
Occupation: German Nato Representative 
Location: Nato Headquarters, Brussels
Bio: Andrew is an advocate for providing foreign aid to countries affected by war and conflict.

- As a German Representative for Nato, I want to provide aid to nations without harming the economies of countries like my own.
- As a Nato Representative for Nato, I want to analyze previous foreign aid policy and evaluate how that affected the economy in the following ten years
- As a German Representative for Nato, I want to draft my own policy and determine the effects it will have
- As a German Representative for Nato, I want to determine which countries are most in need of aid..


**Sun Yue** 
Age: 29 
Location: Brussels, Belgium
Occupation: Member of the European Parliament 
Bio: Sun is a Spanish policy maker who is looking to pass legislation that will benefit the European Union as a whole.

- As an MEP, I want to view historical economic data of the Euro and compare how its value has changed over time.
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
- As a lobbyist, I want to see the relationship between the energy industry in the EU and energy in other countries over time.
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

