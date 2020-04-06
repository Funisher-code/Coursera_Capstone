---

---

# PoC of Recommender System for safe and efficient Food Deliveries during Infectious Disease induced Lockdowns

Course "IBM Data Science"
Capstone Project, April 2020 by [Markus Mächler](https://www.linkedin.com/in/markus-maechler/)

## Introduction

<img src="C:\Users\marku\OneDrive\Desktop\Coursera\IBM Data Science\09 - Applied Data Science Capstone\projects\Coursera_Capstone\corona_cases_total_numbers.png" alt="" style="zoom:25%;" align="right"/>Like many other countries all over the world, Switzerland is trying "flatten the curve" of COVID-19 infected people in order to make sure, that the local health system doesn't collapse. The **goal** of all the measures taken is to **prevent hospitals from having to treat a larger number of severe cases at the same time that they have the capacities for**.

In Switzerland we've been experiencing some major growth of COVID-19 cases in the last weeks. At the time I'm writing this introduction (April 5th 2020), despite drastic measures Switzerland still resides in the Top 10 countries considering total numbers of confirmed cases worldwide (see picture on the right[^1]).

The numbers for Switzerland become even more dramatic if you correct them for the number of inhabitants in each country. The Swiss having only about 8 million inhabitants, this translates to over 250 confirmed cases per 100'000 inhabitants. This is more than Italy and only slightly less than Spain.

**So corrected for the number of inhabitants, the Top 3 in the beginning of April 2020 are actually Spain, Switzerland and Italy.**

In this context, it makes more than sense for the federal government to call the situation "extraordinary".

> The Federal Council has categorised the situation in Switzerland as **extraordinary** under the terms of the Epidemics Act. It has issued a series of measures aimed at the population, organisations and institutions, and the cantons. These measures are designed to curb the spread of the new coronavirus, protect people at especially high risk, and assure the provision of care and therapeutic products to the public. [^2]

As a matter of fact there's currently a "lockdown" in place  and having seen from real world examples in China and Italy, the lockdown makes sense. As a part of that, all shops need to be closed. However, there are important exceptions:.

> The ban does not apply to the following establishments and events:
>
> - Food stores and other shops selling articles for everyday use (e.g. kiosks and petrol station shops)
> - Takeaway establishments, staff canteens, meal delivery services and restaurants for hotel guests
> - Pharmacies, drugstores and shops selling medical aids (e.g. eyeglasses and hearing aids)
> - ...[^2]

Everybody needs to stay at home unless it is absolutely necessary. Again, the federal government has provided clear exceptions.

> Stay at home. Only leave the home if absolutely necessary. That means:
>
> - If you have to purchase groceries.
> - If you have to go to the doctor’s or the pharmacy.
> - If you have to help someone.
> - If you are unable to work from home and you have to go to work.[^2]

The risk of  becoming a severe case and needing hospitalization is much higher for people over the age of 65 and/or having chronic illnesses and also other factors. The situation creates a dilemma for the people at risk. For "flattening the curve" to work, **people at risk should not leave home at all. If possible not even for basic shopping like getting food**.

In the small town where I live, I was able to sign up for a **neighborhood help program** so as a **helper** I can go shopping for people at risk. Again, for it to make sense, helpers should shop in the vicinity and also deliver in the vicinity of their homes. This safes both time as well as helps lowering the risk of spreading the virus infections over a big area.

Of course, we also have **another problem of economical nature**. There's bakeries, cafes, restaurants... that are either closed or only allowed to provide take-away service. Despite the financial aid the government provides, those businesses will not be able to survive if they see drops in numbers of customers for too long.

Wouldn't it be great to solve all those problems together? Namely:

1. keep people at risk **safe but not hungry**
2. keep shops and restaurants **up and running**
3. use helpers as **efficiently and safely** as possible

The purpose of this project is creating a small POC (proof of concept) to help tackling our three problems by creating a simple but efficient recommender system that could be used to place actual orders.

## Data

... *where you describe the data that will be used to solve the problem and the source of the data.*

In our scenario we have three parties:

1. **customer** = person at risk ordering items
2. **shop** = provider of the items e.g. take away restaurant, shop where items are to be purchased
3. **helper** = home (or actual position) of helper that picks up the goods at the shop and delivers them to the customer

#### Location Data

For every order, **location data of all the three parties** is absolutely necessary. For this POC I'm using the following data sources.

- customers: **hypothetical positions in Zurich**
- shops: **Foursquare location data** acquired via API in the vicinity of people at risk
- helpers: **hypothetical positions in Zurich**

#### Additional Data

Then, also additional data will be important to make good recommendations for both shops and helpers.

customers:

- preferences like type of food (hypothetical)

shops:

- covid-19 conform take away service (hypothetical)
- rating (Foursquare API)
- type (Foursquare API)

helpers:

- rating (hypothetical)
- last test COVID-19 negative (hypothetical)
- immunity COVID-19 (hypothetical)
- availability status (hypothetical)

## Methodology

...*Methodology section which represents the main component of the report where you discuss and describe any exploratory data analysis that you did, any inferential statistical testing that you performed, if any, and what machine learnings were used and why.*

We have the following problems...

1. ...keep people at risk **safe but not hungry**
2. ...keep food producers **up and running**
3. ...use helpers as **efficiently** as possible

In a simplified manner:

- People at risk want to eat.
- Let people at risk query food stations only in the vicinity of their homes.
- Match resulting orders with helpers both close to the ppl at risk as well as the food stations.





## Results





Results section where you discuss the results.

## Discussion



Discussion section where you discuss any observations you noted and any recommendations you can make based on the results.

## Conclusion 

Iterative

centralized or not

extend to other items such as medication, contact lenses...

embed in a order system where helpers get requests and are able to accept or deny orders and shops also get notified. Depending on the shop either the helpers go shopping or there is staff in the shops that prepares the order and the helpers simply fetch and deliver it.

blacklists of helpers and customers



Footnotes

[^2]: https://www.bag.admin.ch/bag/en/home/krankheiten/ausbrueche-epidemien-pandemien/aktuelle-ausbrueche-epidemien/novel-cov/massnahmen-des-bundes.html#-14035597
[^1]:https://gisanddata.maps.arcgis.com/
