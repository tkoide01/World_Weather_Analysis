# World_Weather_Analysis
Collect and analyze weather data across cities worldwide to provide real-time suggenstions for clinent's ideal hotels.

## Overview of the Project
This new assignment consists of three technical analyses. You will submit the following deliverables:

Deliverable 1: Retrieve Weather Data

Deliverable 2: Create a Customer Travel Destinations Map

Deliverable 3: Create a Travel Itinerary Map



Results:
Deliverable 1: Retrieve Weather Data


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
   5. Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a   hotel in the city.
 

## Resources
- Data Source: city_data.csv, ride_data.csv
- Software: Python 3.6.1, Jupytor Note Book

## Results
  Based on the two technical analysis, we can infer below information.
  
  1. The ride-sharing summary DataFrame by city type: The below summary DataFrame provides; the number of Total Rides, the number of Total Drivers, the Total Fares, the Average Fare per Ride, and the Average Fare per Driver for each city type.
  
      ![](analysis/PyBer_fare_summary_dataframe.png)
     
  - Total Rides column shows that total number of rides in Urban is 1,625, which is 2.6 times more compared to that of  Surburban city type, and 13 times more of Rural city type.
  - Total Drivers column shows that total Driver count in Urban is 2,405, which is 4.9 times more compared to that of  Surburban city type, and 30.83 times more of Rural city type.
  - The order of Totral Fares from the highest to lowest is proportionate to the number of Total Rides among Urban, Surburban, and Rural area.
  - The Average Fare per Ride in Rural is $34.62, which is 1.1 times more compared to that of Suburban, and 1.4 times more of Urban.
  - The Average Fare per Driver in Rural is $55.49, which is 1.4 times more compared to that of Suburban, and 3.3 times more of Urban.
  2. A multiple-line chart of total fares for each city type provides the trend of Total Fares ($USD) of each City Type plotted with Date as X-axis. Also, the chart displays the result between the beginning of January to the end of April.
  
      ![](analysis/PyBer_fare_summary.png)
  
  - While, Rural city type Total Fare line chart does not fractuate more than the range between 0 to 500, both Urban and Suburban city types have its peak around the end of February. 
  - Also, both Urban and Suburban show huge dip in their Total Fare in the beggining of April.
  
## Summary
   Based on the results, we can draw followings three business recommendations to the CEO.

  1. Plan special promotions for both Drivers and Riders to improve the supply and demand balance of ride based on the trend we see in the multiple-line chart.
    
     + Given Urban and Rural are experiencing the dip in their Total Fare around the beginning of the April, we should plan special discount or benefit system based on the number of ride a rider utilize to boost the demand during this time period.

     + Also, in order to maintain the supply of driver during the peak time, we should encourage drivers to drive more around the end of February by giving bonus based on the number of ride they provide during this time period to maximize the Total Fare.
  
  2. Decrease the number of drivers in Urban area to avoid cannibalizing its demand amont other drivers.
    
     + Based on the ride-sharing summary DataFrame, we see that Average Fare per Driver in Urban city type is $16.57 and critically lower compared to Suburban and Rural city types. In addition, while other two city types have less number of Total Drivers compared to their Total Rides number, the Total Drivers outnumbers the Total Rides in Urban. This suggets that demand of ride-sharing in Urban city type is not high enough to meet the current number of Drivers we have there. 

     + In order to avoid cannibalization of demand and inneficient use of personnel budget in having excess number of Drivers, we should decrease the number of drivers we hire in the Urban.

  3. Increase the number of drivers in Rural area to cover the missing opportunity in potential riders.
    
     + Based on the ride-sharing summary DataFrame, we see that both Average Fare per Ride and Average Fare per Driver are both highest in the rural area. The fact that Rural's Average Fare per Ride is higher than the other two city types means that each driver is driving longer distance and also longer time for each ride. Which means, the drivers in Rural are more likely to be occupied when there is potential rider seeking for a ride in Rural. 

     + Therefore, we should increase the number of driver in rural area by 1.4 so that Average Fare per Driver will not decline below the Suburban's Average Fare per Driver and see if increasing the supply in driver may lead to increase in the Total Rides and also the Total Fares from Rural city type.
  
