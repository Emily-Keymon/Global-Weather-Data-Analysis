# Global Weather Data Analysis


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
1.  Built scatter plot for latitude vs. temperature.  
2.  Added analysis date for reference.  Saved the plot as Fig1.png.
3.  Built scatter plots for latitude vs. humidity.
4.  Added analysis date for reference.  Saved the plot as Fig2.png.
5.  Built scatter plots for latitude vs. cloudiness.
6.  Added analysis date for reference.  Saved the plot as Fi31.png.
7.  Built scatter plots for latitude vs. wind speed.
8.  Added analysis date for reference.  Saved the plot as Fig4.png.


---
## Analysis
As suspected, the weather becomes warmer the closer you get to the equator (0 degrees latitude). There are some spikes in temperature between 20 degrees and 40 degrees latitude.

Neither humiditiy, cloudiness nor wind speed have direct relationships with the latitude. This applies to both the Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).

There is a negative correlation between temperature and latitude. The further away from the equator (0 degrees latitude), the lower the temperature.

There is a positive correlation between latitude and max temperature. The closer you get to the equator (0 degrees latitude), the higher the temperature.

---
## Results

![Fig1](https://user-images.githubusercontent.com/64673015/102723606-ba3a2100-42ce-11eb-8e89-72d0666ed3cc.png)

![Fig2](https://user-images.githubusercontent.com/64673015/102723613-c4f4b600-42ce-11eb-970f-dcba9b182597.png)

![Fig3](https://user-images.githubusercontent.com/64673015/102723619-cde58780-42ce-11eb-8549-316dafe6cd53.png)

![Fig4](https://user-images.githubusercontent.com/64673015/102723624-d5a52c00-42ce-11eb-931c-38d0c0743aff.png)




* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

Run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

### Part II - VacationPy

* Create a heat map that displays the humidity for every city from the part I.

* Narrow down the DataFrame to find your ideal weather condition. 

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

