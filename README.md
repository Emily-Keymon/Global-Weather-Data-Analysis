# Global Weather Data Analysis


---
## Data Sources
* https://openweathermap.org/api
* https://github.com/Emily-Keymon/Global-Weather-Data-Analysis/blob/master/output_data/cities.csv

---
## Tools Used
* 


---
## Tasks
###
1.
2.



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



## Part I - WeatherPy

Create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. 

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

