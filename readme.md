# Ford GoBike System Data Exploration
## By Rahal Mehdi Abdelaziz

## Dataset


 
There are 4702822 trip on the dataset with 13 features 
( trip_duration, started_at, ended_at, start_station_id, start_station_name, 
start_lat, start_lng, start_lng, end_station_id, end_station_name, end_lat, 
end_lng, bike_ride_id, member_casual ) 
most variables are object, the trip duration is an 'int' those related to start 
and end position are 'float', the start time and the end time are 'datetime', 
and member_casual wich is a categorical variable.

The data can be found here (https://s3.amazonaws.com/baywheels-data/index.html),
there is a csv for each month, the data gathered was from 06/2019 to 05/2020  
so the the data was concatenated and cleaned by making correct column names, 
droping erronious data (some observations have a negative trip duration), 
set some feature datatypes and finally make a columns for day of time, 
day of week and month of year.



## Summary of Findings

In the exploration, the first notification is that the trip duration followed a normal 
distribution only if we make an exponential transformation, that's why every visualisation 
for trip duration was done with an exponential transformation. After that a distribution 
exploration was done for day of time, time on the week and month on the day.

In a second phase : the relationship between variables has been explored, to explore:

> Periods with the highest number of trips wich are : 

* In term of day of Time : from 08:00 to 10:00 and from 16:00 to 19:00.
* In term of dayof Week : Tuesday, Wednesday ,Thursday and Friday, Monday is slightly 
lower and the weekend have a low total number of trip.
* In term of Months : February 2020 is the with the highest total number. 

> The average trip duration : The average is about 10 minutes, some period of time the 
average is a little high.

* An interesting observation is the negatie relationship between trip duration average 
and the total number of trips for each period of time.

> The influence of the customer type : Casual customers are more susceptible to have 
a long trip, and have a low total number of trips comparing to member customer. 

* This confirms the negative relationship between the trip duration average and the relative 
total number of trips.






## Key Insights for Presentation



For the presentation, I started by showing the distribution of the distribution 
of the differente period of time types : daytime, weekdays and month.

Secondly, I've shown the behavior of the trip duration over the three differentes period 
of time types by ploting a boxplot for each one.

In the last part I've investigated the dependance of the above features to the customer type 
by ploting the count for each type of period of time, then I moved to the dependance of the average 
trip duration to the customer type by ploting the point plot for each type of period of time 
all plot in this part were regarding the customer type.






