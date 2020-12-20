# Global Weather Data Analysis
The goal for part 1 of this project was to use Python to analyze weather data related to maximum temperature, humidity, wind speed, and cloudiness for over 500 randomly selected global cities. An Open Weather Map API call was used to extract the data.  Linear regression was utilized to determine whether a correlation existed between city latitude and maximum temperature, humidity, wind speed or cloudiness.

The goal for part 2 was to perform an analysis with the data from part 1 to determine the ideal vacation spot.  A heatmap was created to visualize this data.  Hotel analysis was then performed for these areas.  A second heatmap with the hotel layer was created for assistance in finding the perfect vacation destination. 

---
## Data Sources
* https://openweathermap.org/api
* https://github.com/Emily-Keymon/Global-Weather-Data-Analysis/blob/master/output_data/cities.csv

---
## Tools Used
* Jupyter Notebook
* Python - Pandas, Matplotlib, NumPy, SciPy, CitiPy, Gmaps, OS, Requests

---
## Tasks
## Part 1 - Weather Analysis
### Generate Cities List
1.  Created a list for holding lat_lngs and cities.
2.  Created a set of random lat and lng combinations.
3.  Identified nearest city for each lat, lng combination; if the city was unique, added it to a cities list.
4.  Printed the city count to confirm sufficient count.

### Perform API Calls
1.  Created starting URL for Weather Map API call.
2.  Created an empty list for city data.
3.  Created counters for record and set counts.
4.  Ran a loop through all the cities in the list.
5.  Grouped cities in sets of 50 for logging purposes.
6.  Create endpoint URL with each city.
7.  Logged the url, record, and set numbers.
8.  Ran an API request for each of the cities.
9.  Parsed the JSON and retrieved data.
10. Parsed out the max temp, humidity, and cloudiness.
11. Appended the city information into city_data list.

### Data Cleanup and Analysis
1.  Converted array of JSONs into Pandas DataFrame.
2.  Viewed record count to ensure more than 500 cities.
3.  Displayed dataframe and checked statistics.
4.  Created a dataframe with the indices of cities that have humidity over 100%.
5.  Made a new dataframe equal to the city data to drop all humidity outliers by index.
6.  Extracted relevant fields from the dataframe.
7.  Exported the City_Data into a csv file.

### Latitude Analysis
1.  Built scatter plot for latitude vs. temperature.  Added analysis date for reference.  Saved the plot as Fig1.png.
2.  Built scatter plots for latitude vs. humidity.  Added analysis date for reference.  Saved the plot as Fig2.png.
3.  Built scatter plots for latitude vs. cloudiness. Added analysis date for reference.  Saved the plot as Fig3.png.
4.  Built scatter plots for latitude vs. wind speed.  Added analysis date for reference.  Saved the plot as Fig4.png.

### Linear Regression Analysis by Hemisphere
1.  Created a function to create Linear Regression plots.
2.  Created Northern and Southern Hemisphere dataframes.
3.  Plotted linear regression for max temp versus latitude for northern hemisphere.
4.  Plotted linear regression for max temp versus latitude for southern hemisphere.
5.  Plotted linear regression for humidity versus latitude for northern hemisphere.
6.  Plotted linear regression for humidity versus latitude for southern hemisphere.
7.  Plotted linear regression for cloudiness versus latitude for northern hemisphere.
8.  Plotted linear regression for cloudiness versus latitude for southern hemisphere.
9.  Plotted linear regression for wind speed versus latitude for northern hemisphere.
10. Plotted linear regression for wind speed versus latitude for southern hemisphere.

## Part 2 - Vacation Analysis
### Humidity Heatmap for Cities in Part 1
1.  Stored csv created in part one into a dataframe.
2.  Configured gmaps.
3.  Created heatmap of humidity.

### Create new DataFrame fitting weather criteria
1.  Narrowed down dataframe to find ideal weather conditions...max temp between 70 and 80, windspeed less than 10 and no cloudiness.

###  Hotel Analysis
1.  Created dataframe to store hotel names along with city, country and coordinates.  
2.  Set parameters to search for a hotel.
3.  Created list of lat and lng from cities data.
4.  Used the search term: "Hotel" and the lat/lng on Google Maps.
5.  Made requests and printed urls.
6.  Converted to JSON.
7.  Got first hotel from the results and stored the names.
8.  Used a template to add the hotel marks to the heatmap.
9.  Added marker layer on top of heat map. 

---
## Analysis
As suspected, the weather becomes warmer the closer you get to the equator (0 degrees latitude). There are some spikes in temperature between 20 degrees and 40 degrees latitude.

Neither humiditiy, cloudiness nor wind speed have direct relationships with the latitude. This applies to both the Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).

There is a negative correlation between temperature and latitude. The further away from the equator (0 degrees latitude), the lower the temperature.

There is a positive correlation between latitude and max temperature. The closer you get to the equator (0 degrees latitude), the higher the temperature.

---
# Scatter Plots

![Fig1](https://user-images.githubusercontent.com/64673015/102723606-ba3a2100-42ce-11eb-8e89-72d0666ed3cc.png)

![Fig2](https://user-images.githubusercontent.com/64673015/102723613-c4f4b600-42ce-11eb-970f-dcba9b182597.png)

![Fig3](https://user-images.githubusercontent.com/64673015/102723619-cde58780-42ce-11eb-8549-316dafe6cd53.png)

![Fig4](https://user-images.githubusercontent.com/64673015/102723624-d5a52c00-42ce-11eb-931c-38d0c0743aff.png)

---
# Linear Regression 
## Max Temperature versus Latitude

![temp v latitude - northern](https://user-images.githubusercontent.com/64673015/102725315-77327a80-42db-11eb-98b5-43e0c3ec95a8.PNG)

![temp v latitude - southern](https://user-images.githubusercontent.com/64673015/102725320-7ef21f00-42db-11eb-9ef3-8a0f510fe9f4.PNG)

---
## Humidity versus Latitude

![humidity v latitude - northern](https://user-images.githubusercontent.com/64673015/102725333-9e894780-42db-11eb-9c62-7b504cd50f2d.PNG)

![humidity v latitude - southern](https://user-images.githubusercontent.com/64673015/102725341-a648ec00-42db-11eb-90ec-e4a9654b7503.PNG)

---
## Cloudiness versus Latitude

![cloudiness v latitude - northern](https://user-images.githubusercontent.com/64673015/102725349-b2cd4480-42db-11eb-8f1f-d9c8a98da0da.PNG)

![cloudiness v latitude - southern](https://user-images.githubusercontent.com/64673015/102725353-bbbe1600-42db-11eb-8bd6-23575b6ae9d9.PNG)

---
## Wind Speed versus Latitude

![wind speed v latitude - northern](https://user-images.githubusercontent.com/64673015/102725366-c8426e80-42db-11eb-953f-441e06908852.PNG)

![wind speed v latitude - southern](https://user-images.githubusercontent.com/64673015/102725373-cf697c80-42db-11eb-856e-5d826476acfa.PNG)

---
# Humidity Heatmap

![humidity heat map](https://user-images.githubusercontent.com/64673015/102725251-0f7c2f80-42db-11eb-8cf5-bfc6aad250aa.PNG)

----
#  Humidity Heatmap with Hotel layer

![humidity heat map with hotels](https://user-images.githubusercontent.com/64673015/102725261-2ae73a80-42db-11eb-92dd-d5c045779fc7.PNG)



