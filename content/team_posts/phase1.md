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
Occupation: Foreign Investor  
Location: United Kingdom

- As a foreign investor, I want to predict how currency exchange rates will change in response to tariffs. I want to know when I should buy and sell stock so I can maximize gains in a currency that is value to me, pounds.
- As a foreign investor, I want to see how elections will alter exchange rates based on the economic policies of a right vs left party so that I know what to expect when a country has a change in power.
- As a foreign investor, I want to know how changing interest rates will affect the economies of foreign countries so I can predict the demand of goods in these countries.
- As a foreign investor, I want a general idea of which currencies will prevail the strongest or fall the weakest so in the coming months I am prepared for these changes.

**Dillon Brooks**  
Age: 29  
Location: Madrid, Spain  
Occupation: Blue-Collar Worker

Dillon is a middle-class father of two currently living in Madrid, Spain. As he is considering relocating to another country, he wants to understand the financial implications of such a move, particularly how currency fluctuations might affect his savings and long-term stability.

- As a potential migrant, I want to view predictions of future exchange rates between my home country and the EU, so I can better understand how far my savings will go.
- As a potential migrant, I want to compare the strength of the Euro against multiple currencies over time, so I can decide which country is most financially stable to relocate to.
- As a potential migrant, I want to see how major events, such as war or financial crises, historically affected currency value, so I can account for risks before making long-term plans.
- As a potential migrant, I want to track how changes in interest rates might affect the cost of living in Europe, so I can plan my budget more accurately.

**Gerrard Goossens**  
Age: 55  
Location: Brussels, Belgium  
Occupation: Executive for European Shipping Department, Aligurta

Gerrard is an Executive for the European Shipping Department of Aligurta, a Chinese company, and is interested in Euro/Yuan exchange rates. He is in the EU and handles shipments from warehouses in China.

- As a Domestic Importer, I want to predict the best timing to make bulk shipments to the EU by looking at Euro/Yuan price fluctuation given some major current events.
- As a Domestic Importer, I want to avoid selling goods in a non-lucrative area, so I want to figure out if it is better to sell goods in the EU or in China.
- As a Domestic Importer, I want to track tariffs in parallel with exchange rates because they both affect shipping costs.
- As a Company Executive, I want to consider interest rates to borrow money in the most effective way and ship more products to the EU.

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
