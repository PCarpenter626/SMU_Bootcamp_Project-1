# California Wildfire Analysis from (2013 - 2025)

This is my first SMU Group Project 1. In this project, we worked as a single team of 9 members. Each one is assigned with particular task. My task is to calculate the following:

> Calculate and Display Acres Burned Per Year
> Calculate and Display Counties Burned Per Year
> Calculate and Display Personnel Involved Per Year
> Calculate and Display Structures Damaged and Destroyed Per Year
> Calculate and Display the Average length of the Wildfire Per Year

I have done my coding in the python language with the help of pandas library. To find my code, go to the tiya.ipynb notebook file and run it. All the output images are saved in the Output_Data_tiya folder. 

## Understanding the code

To import pandas library to our jupyter notebook we use, **import pandas as pd**. We can use 'pd' to access all the functions in the pandas library. Then I have assigned my cleaned dataset,california_wildfire_data_cleaned.csv to a new dataframe,df. We can create as many dataframes as wanted from this main df to complete our coding task.

While working with the different years dataframe,to remove the timezone information from my python's builtin datetime object directly, i used, **tz_localize()**. To include this function in our code, we have to add the dependency **from datetime import datetime**

### Acres Burned Per Year

This calculation finds that the most acres burned are in the years 2020 and 2021. Almost 2.4 and 2.3 million acres burned these years.

![Acres Burned Per Year_tiya](https://github.com/user-attachments/assets/7e43eed9-d5d6-4e90-9d5f-e87a8c1f5d4f)

I have created an *Area plot* to show the total acres burned per year. I have imported **import matplotlib.pyplot as plt** to do the plotting with Pandas and Matplotlib. 

### Counties burned Per Year

This calculation shows that in the year 2018, the number of counties burned are 113 and in the year 2019, almost 110 counties we under the wildfire. 2018 and 2019 are the years that has the highest number of counties burned.

[Uploading Total Counties Burned Per Year_tiya.html…]()




