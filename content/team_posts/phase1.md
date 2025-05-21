---
title: "Project - Phase I"
date: 2024-05-14
draft: false
description: "Our Idea"
slug: "phase1post"
tags: ["project", "Setup"]
authors:
  - "guhamahesh"
  - "mark_fontenot"
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
As a foreign investor, I want to predict how currency exchange rates will change in   response to tariffs. I want to know when I should buy and sell stock so I can maximize gains in a currency that is value to me, pounds.     
As a foreign investor, I want to see how elections will alter exchange rates based on the economic policies of a right vs left party so that I know what to expect when a country has a change in power.    
As a foreign investor, I want to know how changing interest rates will affect the economies of foreign countries so I can predict the demand of goods in these countries.    
As a foreign investor, I want a general idea of which currencies will prevail the strongest or fall the weakest so in the coming months I am prepared for these changes.    

-add personas-

## Candidate Data Sources

So far, we have been able to retreive API data regarding the following statistics from FRED across a large span of time:

- Three different types of interest rates that the EU uses for Monetary Policy (numerical)
  - The Main Refinancing Rate
  - The Deposit Facility Rate
  - The Marginal Facility Rate
    ![image](https://i.ibb.co/dwTqw4V4/Screenshot-2025-05-20-at-4-16-29-PM.png)
- Conversion Rates Between Currencies (numerical)
  - USD to Chinese Yuan
  - USD to Euro
  - USD to British Pound
    We plan on using the USD conversion rates to find the respective historical EU exchange rates
    ![image](https://i.ibb.co/Pvf19JB2/Screenshot-2025-05-20-at-4-22-23-PM.png)
- The main source of money for Foreign Aid (categorical)
  ![image](https://i.ibb.co/twzFWy3K/foreign-Aid-Fin-Source.png)

  We also plan on retreiving data regarding **tariffs\* and current **wars** and **conflict\*\*
