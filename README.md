# Multiple Linear Regression Modeling for King County Home Prices

<p>Phase 2 Project for Flatiron Online Data Science Bootcamp 

Prepared and presented by: Leah Pope (full time Data Science student)

Presentation URL: [here](thepdflink_tdb)

Presentation Video URL: [here](thevidlink_tbd)

![king_county_map](images/KC_simplemap_Oct2013.jpg)



# Introduction

The goal of this project is to answer questions about housing in King County, a county in Washington state. The Stakeholders for my project are Buyers looking for scenic homes in King County. These Buyers want to know: 
* where to find scenic homes in King County
* what home prices could look like in the near future

I used multiple linear regression modeling to perform analysis on the provided dataset, kc_house_data.csv. I specifically wanted to explore X, Y, and Z.


# Data Description

Data Set Used:

* kc_house_data.csv
    * Contains 2015-2015 Housing Sales data for King County, ~20,000 records.


# EDA Questions Explored
## Question 1: Where are scenic homes located (geographically and zipcode)
### [Notebook](./notebooks/general_eda.ipynb)


## Question 2: What Types of scenic homes are in King County? 
### [Notebook](./notebooks/general_eda.ipynb)


## Question 3: Is there a difference in Price between Regular and Scenic homes?
### [Notebook](./notebooks/general_eda.ipynb)


# Modeling
## Can we predict price using this dataset?
### [Notebook](./notebooks/final_modeling.ipynb)



# Next Steps/Future Work

Futher analysis into the following areas could yield additional insights.

* __King County government officals as Stakeholders__  I used the persona of "Scenic Home Buyers" to frame my stakeholder questions. A great future work idea is to use personas of King County government officals to frame stakeholder questions. I'm thinking specifically of Residential property tax assessors and county/city planning officals that want to learn about economic factors/data related to Residential property. Here are some example question I would like to explore:
    * Improvement Trends: What percentage of homes are being renovated?  What types of homes (large/small/historic/older) are being renovated? 
    * Tax Assessment Insights: Are homes that are larger than neighboring homes getting a 'tax break' in being compared to smaller properties?
    * Home Quality Insights: Are there differences home quality between zip codes/county subregions

* __Model for each County Subregion__ I found a resource that listed 22 Subregions for King County, with title indicating a mix of Urban and Rural areas. I would like to create models for each Subregion instead of a single model trying to predict across a wide range of residential areas.

*__Additional Scenic Home questions__ I would like to explore if there are differences between scenic homes and neighboring homes.
    * living area and lot size of scenic homes with their 15 nearest neighboring homes (_sqft_living15_ and _sqft_lot15_)
    * grade/condition of scenic homes with other homes in same zipcode

* __Validate Waterfront NAN values__  I did a quick search for free APIs that would allow me to check the distance from lat/long coordinates to the nearest coastline. I did find a for-fee API [KB Geo's Distance to Coast Web Service](https://www.kbgeo.com/). It might be interesting/valuable to reverse geocode the lat/long of homes with Unknown/nan  __waterfront__  values and see if  any of them are actually waterfront properties.


# For More Information
* Review the non-technical presentation [here](link
* View the non-technical presentation video [here](link)
* Read the blog post (TBD) [here](link)
* Contact the author [Leah Pope](https://www.linkedin.com/in/leahspope/)


# Repository Structure
```
--notebooks
----data_cleaning.ipynb
----general_eda.ipynb
----final_modeling.ipynb
----future_work.ipynb
--data
----kc_house_data.csv
----proc_kc_house_data.csv
----prepped_for_price_prediction.csv
```