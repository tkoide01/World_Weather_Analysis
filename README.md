# World_Weather_Analysis
Collect and analyze weather data across cities worldwide to provide real-time suggenstions for clinent's ideal hotels.

## Overview of the Project
This new assignment consists of three technical analyses. You will submit the following deliverables:

Deliverable 1: Retrieve Weather Data

Deliverable 2: Create a Customer Travel Destinations Map

Deliverable 3: Create a Travel Itinerary Map


There are three main parts in the analysis of the data.
1. Collect the Data
  - Use the NumPy module to generate more than 1,500 random latitudes and longitudes
  - Use the citipy module to list the nearest city to the latitudes and longitudes
  - Use the OpenWeatherMap API to request the current weather data from each unique city in your list
  - Parse the JSON data from the API request
  - Collect the following data from the JSON file and add it to a DataFrame:
     + City, country, and date
     + Latitude and longitude
     + Maximum temperature
     + Humidity
     + Cloudiness
     + Wind speed
2. Exploratory Analysis with Visualization
  - Create scatter plots of the weather data:
     + Latitude versus temperature
     + Latitude versus humidity
     + Latitude versus cloudiness
     + Latitude versus wind speed
  - Determine the correlations for the following weather data:
     + Latitude and temperature
     + Latitude and humidity
     + Latitude and cloudiness
     + Latitude and wind speed
  - Create a series of heatmaps using the Google MAps and Places API that showcases the following:
     + Latitude and temperature
     + Latitude and humidity
     + Latitude and cloudiness
     + Latitude and wind speed 
3. Visualize Travel Data
   Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences. Complete these steps:
   1. Filter the PAndas DataFrame based on user inputs for a minimum and maximum temperature.
   2. Create a hearmap for the new DataFrame.
   3. Find a hotel from the cities' coordinates using Google's Maps and Places API, the Search Nearby feature.
   4. Store the name of the first hotel in the DataFrame.
   5. Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.
 

## Resources
- Data Source: city_data.csv, ride_data.csv
- Software: Python 3.6.1, Jupytor Note Book
