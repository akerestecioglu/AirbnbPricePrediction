# Airbnb Price Prediction

## Introduction

In this project, the goal is to estimate the price of an AirBnB house using the neighborhood of the house, room-type that house is offering, review rates and availability. In order to do so, the relationship between each parameter and price was visually analyzed. Additionally, there exists a dataset that contains information about the museums in New York and another dataset that has the record of the complaints done to the NYPD in recent years. My intuition is that houses closer (latitude and longitude wise) to museums are popular and therefore they might be more expensive. Also, crime rates are used since people prefer crimeless neighborhoods.

## Outline

1.   Firstly, we'll explore the datasets mentioned above and make some necessary modifications on them.
2.   Then, we are going to reveal the relationships between price and several columns. For this purpose, we'll visualize the data and do some hypothesis testing.
3.   After first two steps, we'll create models wşth different machine learning algorithms and pick the most appropriate one.
4.   Finally, we'll evaluate the results and go back to previous steps to make some improvements if necessary.


## Description of the Datasets

### New York City Airbnb Open Data (https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data/data)

The main dataset that we'll be focusing on is the AirBnB dataset. This dataset is open source and it contains information on airbnb listings all over New York City. It has 48895 rows and 16 columns. Each row contains information about a single rental.

### NYC Museum Dataset (https://data.world/city-of-ny/ekax-ky3z)

Besides, there is the museum dataset which shows the spatial location, telephone numbers, addresses and website URLs of the New York state museums. We are only trying find a correlation between museums and airBnB locations, so we will remove the telephone number and URL columns. The data consists of 131 rows and 8 columns.

### NYPD Complaint Data Historic (https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)

Additional to the datasets above, there is the complaint dataset which consists of 35 columns and 6 billion rows. Column names include information like the date and time of the complaint, which precinct it was made to, the type of the offense, the race, age and sex description of the victim and suspect. Since  calculating a correlation between location of the complaints and the location of the houses, we will ignore most of the information and only keep information about the location. Also, to eliminate complaints which are not actual crimes (just misdemeanors and violations) we will use the ‘type of the offense’ column and select the rows that are associated with felony crimes in the preprocessing section.
