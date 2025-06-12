---
title: "Project - Phase 4"
date: 2025-05-26
draft: false
description: "Our Final Product"
slug: "phase4post"
tags: ["project", "Setup"]
authors:
  - "Guha Mahesh"
  - "BhuvanHospet"
  - "SotaShimizu"
  - "CarterVargas"
showAuthorsBadges: true
---

# Policy Playground

### Our Final Product

With the conclusion of phase 4, we have finally finished our app: *Policy Playground*. We have put many combined hours into this project and are very proud of the application we have created. Our two ML models have been fully developed as well as our database structures and functioning Rest API routes.

One our first phase 4 implementations included adding multiple users to each personas. Now a user has the ablity to login as three different people for each of the three personas. The users all feel unique and individual  features like saved notes and policies are only accessible for the respective user who interacted with or created such policy.


![image]""

#### Policy Maker

Additionally, we have fully optimized our two ML models to make them as accurate as possible. We integrated the data from phase 3 into the database for phase 4 and created additioanl routes that allow a new user persona (The Admin) to train the models. We added routes to allow the user to test these models on the various fiscal and monetary policies. We added various graphs to visually display this information against other similar indicators to compare.

To expand on our work with the two ML models, we included some visualizations to display differences in indicator plots before and after our adjustments. 
##### SP500 Before
![image](https://i.ibb.co/6RNxngw7/Screenshot-2025-06-05-at-8-38-59-PM.png)
##### SP500 After
![image](https://i.ibb.co/Hf4JkP1L/Screenshot-2025-06-05-at-8-39-04-PM.png)

As you can see in the first plot, it fails to meet any of the assumptions and displays heteroscedasticity, autocorrelation, and a lack of a linear pattern. The second pattern displays the residual plots after adjusting for **time**. We added 6 lag values in equal spaces, which greatly reduced the patterns in our resiudal plots. This same adjustment can be seen in our currency models which also greatly benefited as you can see below.
##### Currencies Before
![image](https://i.ibb.co/nsmvR9Sy/Screenshot-2025-06-05-at-8-38-52-PM.png)
##### Currencies After
![image](https://i.ibb.co/P7BcW3T/Screenshot-2025-06-05-at-8-38-44-PM.png)
###### GDP/Capita features against time
![image](https://i.ibb.co/kgKDDWBw/Screenshot-2025-06-06-at-1-08-53-AM.png)
![image](https://i.ibb.co/TxPw6Cpx/Screenshot-2025-06-06-at-1-09-08-AM.png)
![image](https://i.ibb.co/BVps198D/Screenshot-2025-06-06-at-1-09-43-AM.png)

###### GDP/Capita Residual Plots
![image](https://i.ibb.co/j1kw59G/Screenshot-2025-06-06-at-12-54-00-AM.png)
![image](https://i.ibb.co/j9MnRXRC/Screenshot-2025-06-06-at-12-55-16-AM.png)
![image](https://i.ibb.co/nqX1d0WS/Screenshot-2025-06-06-at-12-55-28-AM.png)
![image](https://i.ibb.co/n8CJfh1F/Screenshot-2025-06-06-at-12-55-43-AM.png)
![image](https://i.ibb.co/W426qPRc/Screenshot-2025-06-06-at-12-55-56-AM.png)
![image](https://i.ibb.co/k2LnNh1H/Screenshot-2025-06-06-at-12-56-08-AM.png)
As we mentioned during last phase, we finished training and building our linear regression model and created residual plots. These plots showed the residuals compared to the x values and also included order residual plots for each feature with the additions of Country, and the previous years GDP per Capita. However, we also decided to account for the COVID19 Pandemic during this phase, which increased our accuracy. We did this due to the spike you can see in 2020 due to the pandemic, which likely caused a spike in **Health Spending as a percent of GDP**. For all three features the residual plots show a straight-line connection with an equal number of data points above and below the average. All three plots of the index residuals show some patterns and outliers instead of being completely random. This is likely due to each country's unique circumstances and that these features by themselves can't fully explain a complex factor like GDP per Capita. The model mostly satisfies the conditions of linearity, autocorrelation, and homoscedasticity. However it does not fully meet the requirement of having no multicollinearity; the features show similar patterns –– likely because some countries decided to put more money into their entire government. This means that all three features go up together instead of just increasing one at a time. This is particularly true for spending on health and education as both show similar patterns.

#### More Features for the Policy Maker
When a user is satisfied the policy they have tested, they now have the ability to save this policy and publish it. Published policies can then be accessed by the Economist Persona. To do this, we expanded our database with additional tables such as SavedPolicy and added more routes. The policy maker is also able to delete and modify policies through PUT and DELETE routes. One of the major feedbacks we received from Phase 3 was the lack of cohesion and interconnectedness between the Economist and Policy Maker Personas. By adding these functionality features, we made these two personas more intertwined.

![image]()

#### Economist

To expand on the economist, we added another simple machine learning model using cosine similarity. When a user favorites a policy and selects it on the *View Favorite Policy* page, information is displayed on the 5 policies that are most similar to it. This model was trained on three numeric feature: budget spending, duration of enforcement in months, and the population size that it will be affecting. This addition makes the economist role of analyzing policy more effective through the ability of comparison. The fake data generated for this persona remains mostly the same with the addtion of those three features mentioned prior.

![]

Other additons to this persona included adding a *Politician Contact Information* button that brings up more information on a policy and more filter cirteria to the *Historical Data Viewer* page.

[]

#### Lobbyist

The lobbyist had also undergone major changes from Phase 3. Again, to make this persona more aligned to the Policy Maker persona, we added the ability for the user to adjust sliders on based features that are directly related to the monetary and fiscal policies. When the Lobbyist creates this note, the same model is used to also produce graphs that are visible by the lobbyist.

[] image

### Front End Final Details.

Our team has also put in work to improving the interface and visuals of our application. We completly revamped our color theme with the additon of animations to page headers and new fonts. Despite being limited Streamlit, we used CSS and HTML to make our app look as clean as possible. We strived to make our pages look unique and interesting, while also containing a overlying theme.


### Rest API Matric

We took the feedback from phase 3 and updated our route handler names to be nouns while combining similar ones though GET, POST, PUT, and DELETE method types. Below is our updated matrix that counts for the added routes as well.

![image](https://i.ibb.co/n88Z7G8J/Screenshot-2025-06-12-at-10-57-44-PM.png)

### Conclusion

Overall, we are very proud of the work we have put into this project. We felt we really transformed Policy Playground from a sundry of functionalities to one cohesive and fully implemented application. 













