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

With the conclusion of phase 4, we have finally finished our app, Policy Playground. We have put many combined hours into this project and are very proud of the application we have created. Our two ML models have been fully developed as well as our database structures and functioning Rest API routes.

One our first phase 4 implementations included adding multiple users to each personas. Now a user has the ablity to login as three different people for each of the three personas. This makes me user feel unique and individual as features like saved notes and policies are only accessible for the respective user who interacted with or created such policy.

![image]""

#### Policy Maker

Additionally, we have fully optimized our two ML models to make them as accurate as possible. We integrated the data from phase 3 into the databse for phase 4 and created additioanl routes that allow a new user persona, the admin, to train the data. Further routes allow the user to test these models on the various fiscal and monetary policies. We added various graphs to visually display this informjation.

When a user is satisfied the policy they have tested, they now have the ability to save this policy and publish it. Published policies can then be accessed by the Economist Persona. To do this we had to expand our database with additioanl tables such as SavedPolicy and added more routes. Modifying published polices and deleting them is also possible for the Policy Maker through PUT and DELETE routes. One of the major feedbacks we received from Phase 3 was not enough cohesion and interconnectedness between the Economist and Policy Maker Personas. By adding these functionality features, we made these two personas much more intertwined.

![image]

#### Economist

To expand on the economist, we added another simple machine learning model using cosine similarity. When a user favorites a policy and selects it on the *View Favorite Policy* page, information is displayed on the 5 policies that are most similar to it. This model was trained on three numeric features, budget spending, duration of enforcement in months, and population size that it will be affecting. This addition makes the economist role of analyxing policy more insightful through the ability of comparison. The fake data generated for this persona remains mostly the same with the addtion of those three features mentioned prior.

![]

Other additons to this persona included adding a *Politician Contact Information* button that brings up more information on a policy and more filter cirteria to the *Historical Data Viewer* page.

[]

#### Lobbyist

The lobbyist had also undergone major changes from Phase 3. Again, to make this persona more aligned to the Policy Maker persona, we added the ability for the user to adjust sliders on based features that are directly related to the monetary and fiscal policies. When the Lobbyist creates this note, the same model is used to also produce graphs that are visible by the lobbyist.

[] image

### Front End Final Details.

Our team has also put in major work to improving the interface and visuals of our application. We completly revamped our color theme with the additon of animations to page headers and new fonts. Despite being limited Streamlit, we used CSS and HTML to make our app look as clean as possible. We strived to make our pages look unique and interesting, but also contain a overlying theme.

### Conclusion

Overall, we are very proud of the work we have put into this project. We felt we really transformed Policy Playground from a sundry of functionalities to one cohesive and fully implemented application. 













