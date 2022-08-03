# World_Weather_Analysis

## Project Overview
The purpose of this project was to retrieve weather data from across the globe by randomly generating 2,000 locations using longitude and latitude. Once this data was aggregated, the next step was to create a travel destinations map (based on customer input) and design a travel itinerary map taking those customer inputs into consideration. The weather data used for this project was based on API calls made on Tuesday, August 2nd, 2022. 

## Resources
  * Software: Python with multiple libraries, citipy and gmaps plugins
  * Platform: Jupyter Notebook, via Anaconda
  * Data Sources: OpenWeatherMap.com, Google APIs: Places API, Maps JavaScript API, Directions API

## Summary of Results
Overall the process was seamless and straight forward. All of the API calls performed without issue and the data captured was as expected. Of the 2,000 randomly selected coordinates, citipy located 737 cities (with populations of at least 500 people). Moving forward with this data, two questions were asked of the customer, listed below.
  1. What is the minimum temperature you wish to have on your trip?
  2. What is the maximum temperature you wish to have on your trip?

The answers provided were 70°F and 95°F, respectively. I then filtered the cities that offered maximum temperatures within this range, which reduced the city list to 373. Since this data was intended to provide possible vacation destinations, identifying a hotel within these cities was a must. To accomplish this, an API call was made to Google Places to determine if a hotel was located within 5,000 meters of the given longitude and latitude of each city. Only 26 cities within my list did not have a hotel. This means the customer had 347 cities across the globe that met their temperature requirements. The image below maps those cities.

<sub>Customer Temperature Based Vacation Map</sub>
![WeatherPy_vacation_map](https://github.com/Kelfang/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

The next step within this process was to create an itinerary with four cities that were located within the same country AND could be navigated to and from using driving directions that were sourced by Google's Directions API. This was by far the most challenging aspect of the project. While I was fortunate to have several countries with multiple cities on my list, I was really limited to which countries had reliable driving directions. 

Ultimately, after vetting locations with Google Map's UI, I settled on Great Britain. These four stops traverse the country and allow the traveler to visit places off the beaten path, focusing on the various coastlines. Below is an image of the itinerary I mapped and a link to the driving routes can be found [here](https://github.com/Kelfang/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png).

<sub> Great Britian Travel Itinerary</sub>
![WeatherPy_travel_map_markers](https://github.com/Kelfang/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)


