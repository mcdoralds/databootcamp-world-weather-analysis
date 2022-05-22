# databootcamp_world_weather_analysis

# Project Overview
This project's purpose is to create a database of travel destinations and hotels to provide trip planning services for the user. The user inputs their preference of temperature, and our program will return a list of possible cities that fit that criteria as well as hotel recommendations for each city. 

## Background
Client (PlanMyTrip) would like to use our program to provide travelers and vactioners with a dynamic and customized experience. 

## Objective
Collect and analyze weather data across cities worldwide.

## Resources
Python 3.7.13, OpenWeather API, Google Maps API, citipy module

## Procedure

Using the NumPy module, I generated ~1,500 random latitudes and longitudes and used the citipy module to list the nearest city to those coordinates. Then, I used the OpenWeatherMap API to request the current weather data from each unique cityon the list.

From there, I parsed the JSON data from the API request to collect the following information, which then got added to a DataFrame:

- City, country, and date
- Latitude and longitude
- Maximum temperature
- Humidity
- Cloudiness
- Wind speed


# Results
## Analysis

The analysis includes:

- Scatter plots of the following weather data comparions:
  - Latitude versus temperature
  - Latitude versus humidity
  - Latitude versus cloudiness
  - Latitude versus wind speed

- A deeper look into the correlations between the relationships listed above using regression analysis
- A series of heatmaps using the Google Maps and Places API that showcases the relationships above.

Also included are sample maps and itineraries to illustrate the extent to which our program can plan a trip for the customer using readily available information from the internet.

## Findings
- The correlation between the latitude and the maximum temperature is strong to very strong because the r-value is less than –0.7 for the Northern Hemisphere and greater than 0.7 for the Southern Hemisphere, as shown by the plots here. This means that as we approach the equator, 0° latitude, the temperatures become warmer. And when we are further from the equator the temperatures become cooler.
- The correlation between the latitude and percent humidity is very low because the r-value is less than 0.04 for the Northern and Southern Hemispheres for the plots shown here. This means that percent humidity is unpredictable due to changing weather patterns that can increase or decrease percent humidity. 
- The correlation between the latitude and percent cloudiness is very low because the r-value is less than –0.09 for the Northern Hemisphere and less than –0.02 for the Southern Hemisphere for the plots shown here. This means that cloudiness is unpredictable due to changing weather patterns that can increase or decrease percent cloudiness. 
- The correlation between the latitude and wind speed is very low because the r-value is less  than –0.07 for the Northern Hemisphere and less than –0.3 for the Southern Hemisphere for the plots shown here. This means that wind speed is unpredictable due to changing weather patterns that can increase or decrease wind speed.
