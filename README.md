# PyBer Analysis

## Overview of Project:

Going through the PyBer rideshare data from [city_data](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Resources/city_data.csv) and [ride_data](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Resources/ride_data.csv) csv files and creating datafiles to help analyze various factors. This analysis will be helpful for PyBer in their future approach towards creating a more successful outcome each year.

There are three deliverables:  

  1. Summary DataFrames for PyBer  
  2. Multiple Line Plot indicating the total weekly of the fares for each type of city
  3. The Written Report  

## DELIVERABLE 1: Summary DataFrame for PyBer:  

Once we merge the city_data and ride_data with their common column *city*, we can start creating the following series:  

  1. Total Rides for each City Type  
  ![ride_per_type](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/total_rides_by_city_type.png)

  Notice that there are _13 times_ as many trips in *Urban cities* than in *Rural cities* and more than _2.5 times_ as many trips as in *Suburban cities.*
  
  2. Total Driver for each City Type  
  ![driver_per_type](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/total_drivers_by_city_type.png)
  
  Notice that there are more _30 times_ as many drivers in *Urban cities* than in *Rural cities* and almost _5 times_ as many drivers as in *Suburban cities.*
  
  3. Total Fares per City Type  
  ![fares_per_type](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/total_fares_by_city_type.png)
  
  Notice that total fares in *Urban cities* are more than _9 times_ that of *Rural cities* and more than _twice_ that of *Suburban cities*
  
  4. Average Fare per Ride per City Type  
  ![fare_per_ride_city](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/avg_fares_per_ride_by_city_type.png)
  
  Notice the fares per ride is highest in *Rural cities* and the lowest in *Urban cities*
  
  5. Average Fare per Driver per City Type  
  ![fare_per_ride_driver](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/av_fare_per_driver_by_city_type.png)
  
  Notice PyBer drivers in *Rural cities* can make more than _three times_ as much money per ride (on average) than in *Urban cities*.  
  
 
 This data is very helpful when looking into the statistics of PyBer's rideshare information. 
 
### The PyBer Summary DataFrame would look like this:  

![pyber_summary_df](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/pyber_summary_df.png)  

## DELIVERABLE 2: Multiple Line Plot  

1. Create a new dataframe showing the sum of the fares for each date. Indices: City type and Date
![total_fare_percitytype_perdate](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/fare_by_city_sum_by_date.png)

Using the *.to_frame()*, we create a dataframe from the series.

2. Reset the index 
3. Create a Pivot table with index: date, columns: types and values: fare
![pivot_table](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/fare_by_city_pivot.png)  

4. Create a new DataFrame using loc on dates between 2019-01-01 and 2019-04-29
![dates_by_loc](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/dates_by_loc.png)

5. Set 'date' as index.    
6. Check index datatype using df.info()    

7. Resample using _weekly_ bins  
![weekly_resample](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Screenshots/resample-weekly.png)  


### Graph for the resampled dataframe:  

![line_graph](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/Analysis/Pyber_fare_summary.png)

From the graph, we can infer some of the following:  

  * The end of February looks like the most profitable busiest for PyBer in all city types.
  * _Urban cities_ make the most money, nearly always making more than *$2000.00* a day.
  * _Rural cities_ make the least money, never making more than *$500.00* on any given day.
  * _Suburban cities_ see a range of fares as low as *$700* and sometimes making *$1700*. 

-------
-------

The complete code can be found [PyBer_Challenge](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/PyBer_Challenge.ipynb)
Some other analyses on the PyBer city and ride data can be found:  
[PyBer_Analysis](https://github.com/SoumyaAbraham/PyBer_Analysis/blob/main/PyBer_Analysis.ipynb)
[PyBer


