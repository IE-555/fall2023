# Homework 3 - Pandas
- Due date and submission details to be determined. 
- If you have questions, [post them to the Issue Tracker](https://github.com/IE-555/fall2023/issues/6).  Emailed questions will not be answered.

--- 

In this assignment you are asked to submit a single file, named `homework6.py`, which will contain all of the functions described below.

This homework assignment requires you to write functions to analyze data from the New York City CitiBike system.

- Please visit https://www.citibikenyc.com/system-data for a description of the system and the data that are available.
- This homework assignment will only use the "Citi Bike Trip Histories" data.

Please read the instructions **carefully**.

---


1.  Write a function named `countTrips`.  It will take a pandas bike trips history dataframe as its input.  The function should return an integer indicating the number of trips that are contained in the dataframe.

    - NOTE:  Each row corresponds to a "trip" (i.e., it has a single origin and a single destination.

2.  Write a function named `avgTripDuration` that will return the average trip duration (in seconds) for a given pandas bike trips history dataframe.

3.  Write a function named `maxTripDuration` that will return the maximum trip duration (in seconds) for annual members who were born on or after a given (input) year. 
    - This function will take two inputs, in this order:
        - A 4-digit integer year (e.g., `1999`), and 
        - A pandas bike trips history dataframe.


4.  Write a function named `countBikes` that will return the number of distinct bikes in a given pandas bike trips history dataframe. 

    - NOTE: Each bike has a unique ID.

5.  Write a function named `countStartStations` that will return the number of unique **starting** stations in a given pandas bike trips history dataframe. 

6.  Write a function named `countAllStations` that will return the number of unique stations (across both start and end stations) in a given pandas bike trips history dataframe. 

7.  Write a function named `avgTripsPerBike` that will return a single scalar numeric value representing the average number of trips each bike has taken in a given pandas bike trips history dataframe. 
    - NOTE 1:  **Do NOT use "for" loops.**
    - HINT: See the pandas `groupby()` operation.
    
8.  Write a function named `avgRiderAge` that will return a single scalar numeric value describing the average age of bike riders
as of Jan. 1 of an input year (the first input described below).  Assume riders were born on Jan. 1 of their birth year, as per the given pandas bike trips history dataframe.
    - This function will take two inputs, in this order:
        - A 4-digit integer year (e.g., `2023`), and 
        - A pandas bike trips history dataframe.
        
9.  Write a function named `avgTripsByDayOfWeek` that will return a 7-element **list** containing the average number of trips taken on each day of the week.  The first element of the list should represent the average number of trips taken on Sundays; the last (7th) element of the list should represent the average number of trips taken on Saturdays.  The function will have one input: 
a given pandas bike trips history dataframe. 

    - NOTE 1:  **Do NOT use "for" loops**.
    - HINT 1:  Add a column to the dataframe that contains the day of the week corresponding to the start date of each row.
    - HINT 2:  The `groupby()` operation may be helpful.
        
10.  Write a function named `topXdepartures` that will find the `x` stations that have the most departures, sorted in descending order.  If there are ties, include those as well.  For example, your function may be asked to find the 10 stations with the most departure; if there is a 3-way tie for 10th place, then your function should return 12 stations.  Your function should return a pandas **dataframe** containing three columns:
- `rank` (where rank `1` has the highest number of departures.  If two or more stations have the same number of departures, then those stations should have the same rank);
- `start station id`; and 
- `number of departures`.

    This function will take two inputs, in this order:
    - An integer indicating the top `x` number of departures; and
    - A pandas bike trips history dataframe.
    

    
11.  Write a function named `numEarlyTrips` that returns the integer number of trips that were started between 8:00am and 10:00am.  The function will have one input: a given pandas bike trips history dataframe. 
