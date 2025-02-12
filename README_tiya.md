# California Wildfire Analysis from (2013 - 2025)

This is my first SMU Group Project 1. In this project, we worked as a single team of 9 members. Each one is assigned with particular task. My task is to calculate the following:
              * Calculate and Display Acres Burned Per Year
              * Calculate and Display Counties Burned Per Year
              * Calculate and Display Personnel Involved Per Year
              * Calculate and Display Structures Damaged and Destroyed Per Year
              * Calculate and Display the Average length of the Wildfire Per Year

I have done my coding in the python language with the help of pandas library. To find my code, go to the tiya.ipynb notebook file and run it. All the output images are saved in the Output_Data_tiya folder. 

## Understanding the code
To import pandas library to our jupyter notebook we use, **import pandas as pd**. We can use 'pd' to access all the functions in the pandas library. Then I have assigned my cleaned dataset,california_wildfire_data_cleaned.csv to a new dataframe,df. We can create as many dataframes as wanted from this main df to complete our coding task.

While working with the different years dataframe,to remove the time **tz_localize()**. To use this function, we have to add the dependency **from datetime import datetime** to remove column to 
