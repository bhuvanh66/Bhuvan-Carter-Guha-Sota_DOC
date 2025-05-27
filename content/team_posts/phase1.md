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

So far, we have been able to retreive API data regarding the following statistics from FRED across a large span of time:

- Three different types of interest rates that the EU uses for Monetary Policy (numerical)
  With these sources, we can train the model to predict exchange rates based off **EU monetary policy**

  - The Main Refinancing Rate
  - The Deposit Facility Rate
  - The Marginal Facility Rate

    ![image](https://i.ibb.co/dwTqw4V4/Screenshot-2025-05-20-at-4-16-29-PM.png)

- Conversion Rates Between Currencies (numerical)
  These sources will essentially give us the labels for the AI data so that we can actually train the model
  - USD to Chinese Yuan
  - USD to Euro
  - USD to British Pound
    We plan on using the USD conversion rates to find the respective historical EU exchange rates
    ![image](https://i.ibb.co/Pvf19JB2/Screenshot-2025-05-20-at-4-22-23-PM.png)
- The main source of money for Foreign Aid (categorical)
  We plan on training the AI to check how the source of the foreign aid that EU provides affects currency exchange as well
  ![image](https://i.ibb.co/twzFWy3K/foreign-Aid-Fin-Source.png)

  We also plan on retreiving data regarding **tariffs** and current **wars** and **conflict** as these are very notable factors that affect exchange rates
