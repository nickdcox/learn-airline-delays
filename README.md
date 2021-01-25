### learn-airline-delays
## Learn Python Data Analytics By Example: Airline Arrival Delays

[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)

### Introduction

While working towards my Master's in Business Analytics, I found that learning by example is the best way for me to learn Python data analytics.  Being given a dataset and a set of coding tasks is much more beneficial than reading a textbook or listening to a professor.  

I want to share this method of learning with others who will also benefit.  All you need is a Python development environment (I recommend [Jupyter Notebook](https://jupyter.org/)) and a willingness to learn and have fun.

Included in this article is a list of data analytics tasks, followed by a detailed walkthrough of how to complete the tasks.  Please try to complete the tasks yourself before reading through the walkthrough - you will get more out of it that way.  Do keep in mind that there are many many ways to solve coding problems, so your code likely will not match mine word for word and that is okay.

### Project Description

Project Description
For this project we will use a dataset of about 40,000 records, which represent flight arrival delays for 18 airlines in the United States.  Each row in the dataset represents a summary of delay data for a carrier-airport pair for the specified month.  The dataset was created in January 2021 and contains data from January 1, 2018 to December 31, 2019 sourced from the [Bureau of Transportation Statistics](https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp).

You will need to install the [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/) and [Basemap](https://matplotlib.org/basemap/index.html) libraries, if you do not already have them.


### Data Analytics Tasks

Please perform the following tasks in Python using the *delays_2018.csv*, *delays_2019.csv* and *airport_coordinates.csv* datasets available from the [GitHub repo](https://github.com/nickdcox/learn-airline-delays).
1. Read the CSV files containing the airline delay data into a single DataFrame.  Then display the total number of rows imported.
2. Change the *date* column to date format YYYY-M (e.g. 2018-1).  Then perform exploratory data analysis on the imported dataset to identify invalid data - write code to remove the impacted rows. Finally, display the number of rows remaining.
3. Display a list of all Tennessee airports that appear in the dataset.
4. Import the coordinates dataset and merge it with the existing dataset.  Plot the coordinates of all airports on a map (hint: use Matplotlib and Basemap).
5. Display the number of diverted flights for each carrier-airport pair.
6. Display how many arrivals into JFK in 2019 encountered both weather and carrier delays?
7. Display the airline with the most flight cancellations as a percentage of total arriving flights.
8. Determine the overall average number of delays per airport.
9. Display the three carriers with the lowest number of delayed flights.
10. Request that the user input an airline. Then plot the monthly number of national air system (NAS) delay minutes for that airline.  Display whether the trend is increasing or decreasing over the last 2 months.


### Data Dictionary (*delays_2018.csv, delays_2019.csv*)

Each row in the datasets represents a summary of delay data for a carrier-airport pair for the specified month.  For example, a row may represent delay data for May 2018 for American Airlines flights arriving into JFK airport in New York City.

When multiple causes are assigned to one delayed flight, each cause is prorated based on delayed minutes it is responsible for. The numbers are rounded and may not add up to the total.


| Column Name | Description |
| :--- | :----------- |
| date | Year and month, in the format YYYY-M (e.g., 2018-1) |
| carrier | The two character designator for the carrier/airline. |
| carrier_name | The full name of the carrier/airline. |
| airport | The three character designator for the arrival airport. |
| airport_name | The full name of the arrival airport. |
| arr_flights | The total number of arriving flights for the carrier-airport pair for the month specified. |
| arr_del15 | The number of arriving flights that were delayed.  Delayed is when a flight arrives more than 15 minutes later than the scheduled arrival time. |
| carrier_ct | The number of arriving flights delayed due to a carrier issue. |
| weather_ct | The number of arriving flights delayed due to a weather issue. |
| nas_ct | The number of arriving flights delayed due to a national air system issue. |
| security_ct | The number of arriving flights delayed due to a security issue. |
| late_aircraft_ct | The number of arriving flights delayed due to an earlier late arrival of an aircraft. |
| arr_cancelled | The number of cancelled flights. |
| arr_diverted | The number of diverted flights. |
| arr_delay | The total number of delayed minutes due to delays. |
| carrier_delay | The total number of delayed minutes due to carrier issues. |
| weather_delay | The total number of delayed minutes due to weather issues. |
| nas_delay | The total number of delayed minutes due to national air system issues. |
| security_delay | The total number of delayed minutes due to security issues. |
| late_aircraft_delay | The total number of delayed minutes due to earlier later arrival of aircraft. |  
