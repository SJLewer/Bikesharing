# Bikesharing
## Project Overview
Citi Bike in New York City is the largest bike-sharing program in the nation and has been very successful.  Could Citi Bike's success be replicated in Des Moines, IA?  This project will begin the feasiblity analysis by learning about Citi Bike customers.

### Data Preparation
The dataset for this analysis is August 2019 New York City Citibike trip data available on-line at: https://www.citibikenyc.com/system-data.  The datatype for two fields needs to be changed:  tripduration from an integer to datetime and gender from an integer to a string.  To retain the original data, two new fields ("triptime" and "genderstr") were created for the revised datatypes.

![bike_df_orig](https://user-images.githubusercontent.com/90986041/147122161-2a0377a4-4f86-43e2-a453-40e912c2076e.png)
![bike_df_update](https://user-images.githubusercontent.com/90986041/147122177-b19cfa99-53eb-4437-9777-3af8cbdf51bc.png)


## Results
### Where are the NYC Citi Bike stations?  Which ones are the busiest?
![stations](https://user-images.githubusercontent.com/90986041/147122892-a828d1ca-4272-4130-84cb-ee22d91c749b.png)

### How long are customers renting a bike?  Does gender impact the length of the bike ride?
![triptime](https://user-images.githubusercontent.com/90986041/147123013-c54bd5c2-afd0-4928-ab32-82dd06134719.png)
![tripgender](https://user-images.githubusercontent.com/90986041/147123020-850ec217-3f0b-4404-a50d-f81ddc0236c7.png)

### What are the customer types?
![customer type](https://user-images.githubusercontent.com/90986041/147123103-fb99077f-957b-4317-aad7-c43801faa037.png)

### What is the gender mix of the subscribers vs. customers?  Does the mix vary by weekday?
![gmixbyweekday](https://user-images.githubusercontent.com/90986041/147123217-afbafe81-bdf9-4813-99e9-cc0e216911d5.png)

### What are the peak days and times for bike riding?  Does gender impact the peak days and times?
![Peakheatmap](https://user-images.githubusercontent.com/90986041/147123296-76d6964f-f2da-4c54-b59f-ba263f5cfc1a.png)
![peakheatgender](https://user-images.githubusercontent.com/90986041/147123346-366e6856-a8cd-4bcc-b4a1-d38b158cf765.png)

### What is the most common age of the bike riders?
![rider age](https://user-images.githubusercontent.com/90986041/147123544-bcb3cac6-d50f-41fe-8eec-d8ce88321924.png)

Link to Tableau Public site: https://public.tableau.com/app/profile/sara.lewer/viz/NYCCitibikeAnalysis_16398338949320/BikeSharing

## Summary
Des Moines' population average age (34 years) is within the range of the most common age of Citi Bike customers.  This is encouraging and supports continued analysis to answer more questions.  

The Aug 2019 dataset can be used to answer questions about the bikes:
1. _Are bike rentals one-way or roundtrip?_  Use the bikeid, start station id, end station id, along with a new calculated field to determine "one-way" (start and end station id not equal) and "round-trip (start and end station ids are the same).  Plot in a pie chart.

1. _How many bikes are in Citi Bike's fleet?_ Use the count of bikeids for a text report

1. _How many bikes are at each station?_ Use count of bikeid, start station id, start station longitude, and start station latitude.  Plot station ids on a map with markers sized by the number of bikes.

Additional data gathering will be needed to answer other questions such as: 
* Most of Citi Bike's customers appear to be commuting in the heart of downtown NYC during business commute times.  Is downtown Des Moines bike-friendly?  
* How many bike rentals are needed to financially break even?  
___
## Resources:
_Dataset for analysis_:  August 2019 New York City Citibike trip data https://www.citibikenyc.com/system-data

_Applications_:
* Python with Pandas
* Tableau Public

_Analyst_: S. Lewer
