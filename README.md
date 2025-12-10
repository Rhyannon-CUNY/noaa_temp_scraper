# NOAA temperature scraper for last 100 years by state

## About

This code uses NOAA(National Oceanic and Atmospheric Administration)'s National Centers for Environmental Information [API](https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/statewide/time-series/service-api)) to bulk donwload minimum and maximum temperatures for all months for the last 100 years by state. 

The purpose is to compile state-level data and calculate the minimum and maximum temperature by season (spring: March-May; Summer: June-August; Fall: September-November; Winter: December-February) and create a searchable JSON database. 

This is a building block for creating an interactive climate change lookup that shows personalized values for the reader based on the state they are from and the year they were born to see the impact of climate change in their home state in their life time.

## Data

The NOAA data is oragnized by state, county etc. This code extracts for state-level data.

API serach parameters include:
* state code
* start year
* end year
* month/months/all months
* maximum temperature
* minimum temperature
* average temperature
  etc..

## Process

`getTempData`

The code uses the base url for NOAA's "Climate at a Glance" API structure, sets the time frame to 1925-presentand loops through the list of state codes to pull monthly maximum and minimum temperature values and saves it to a csv by state. 
