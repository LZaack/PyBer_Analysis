# PyBer Analysis
## PyBer Analysis Overview
I was assigned to analyze all the rideshare data from January to early May of 2019, and create a compelling visualization for the CEO, V. Isualize. To accomplish the task, we followed the next steps and deliverables:

  **1** Import the data into a Pandas DataFrame.

  **2** Merge your DataFrames.

  **3** Create a bubble chart that showcases the average fare versus the total number of rides with bubble size based on the total number of drivers for each city type, including   urban, suburban, and rural.

  **4** Determine the mean, median, and mode for the following:

    4.1 The total number of rides for each city type.

    4.2 The average fares for each city type.

    4.3 The total number of drivers for each city type.

  **5** Create box-and-whisker plots that visualize each of the following to determine if there are any outliers:
    
    5.1 The number of rides for each city type.
    
    5.2 The fares for each city type.
    
    5.3 The number of drivers for each city type.

  **6** Create a pie chart that visualizes each of the following data for each city type:
   
    6.1 The percent of total fares.
    
    6.2 The percent of total rides.
    
    6.3 The percent of total drivers.

After delivering my analysis V. Isualize asked me to create a summary DataFrame of the ride-sharing data by city type, a multiple-line graph that shows the total weekly fare for each city type.

## PyBer Analysis Results

![pyber_summary_df](/analysis/pyber_summary_df.png)

As it is shown in the previous data frame, the numbers represent that:

(a) The urban rides are 13 times bigger than the rural area and 2.6 times bigger than the suburban area;

(b) The sum of the fares in urban areas is 9.2 times bigger than the rural areas and 2.05 times than the suburban areas;

(c) The average fare per ride is 41% most expensive in rural areas and 11% more expensive in suburban areas than in urban areas.

### Coding Process
To achieve these results I have done the following steps:

`(i)` I created the next DataFrame showing the sum of the fares for each date where the indices are the city type and date.

![groupby_pivot_data_df](/analysis/groupby_pivot_data_df.png)


`(ii)` Then I reseted the index on the DataFrame.

![reset_pivot_data_df](/analysis/reset_pivot_data_df.png)


`(iii)` After, I created a pivot table with the 'date' as the index, the columns as 'type', and values as 'fare' to get the total fares for each type of city by the date.

![new_pivot_data_df](/analysis/new_pivot_data_df.png)


`(iv)` Then I created a new DataFrame from the pivot table DataFrame using the given dates, '2019-01-01':'2019-04-29'.

![dates_pivot_data_df](/analysis/dates_pivot_data_df.png)


`(v)` Following I created a new DataFrame to get the sum of the fares for each week.

![week_fares_sum](/analysis/week_fares_sum.png)


`(vi)` Finally I plot the resample DataFrame as follows.

![PyBer_fare_summary](/analysis/PyBer_fare_summary.png)


## PyBer Analysis Summary

**I.** I suggest comparing the distance of the rides between the rural areas with the suburban and the urban, to understand if it is possible to reduce the rural fare with the objective to increase the rides in that zone.

**II.** As a strategy to create competition in the rural zone, I suggest hiring more drivers.

**III.** The suburban drivers could receive grants every time they get a rural ride to develop this area.

