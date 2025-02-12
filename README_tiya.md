# California Wildfire Analysis from (2013 - 2025)

This is my first SMU Group Project 1. In this project, we worked as a single team of 9 members. Each one is assigned with particular task. My task is to calculate the following:

- Calculate and Display Acres Burned Per Year
- Calculate and Display Counties Burned Per Year
- Calculate and Display Personnel Involved Per Year
- Calculate and Display Structures Damaged and Destroyed Per Year
- Calculate and Display the Average length of the Wildfire Per Year

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

![Screenshot 2025-02-11 at 10 21 55 PM](https://github.com/user-attachments/assets/828c9aab-8080-40a7-bae8-3017550c9eb3)


I have created an *interactive 2D Scatter plot*. To run it in your python code, we have to first install 
**pip install plotly** then import **import plotly.express as px** and to use the write_image command for exporting image to my output folder, i need to install **pip install kaleido** package.

### Personnel Involved Per Year

This calculations finds that 2013 has the highest number of personnel involved to manage the fire.

![Screenshot 2025-02-11 at 10 29 30 PM](https://github.com/user-attachments/assets/4c22676c-7912-4508-9977-cfec4dd953b3)


Here, i have used Bar plotting method to achieve above diagram. I have to import **import seaborn as sns** for enhanced statistical visualizations.

### Structures Damaged and Destroyed Per Year

Comparison of Structures damaged and destroyed per year resulted in finding that the year, 2017 has most structures damaged and 2018 has most structures destroyed.

![Screenshot 2025-02-11 at 10 33 31 PM](https://github.com/user-attachments/assets/7e77abc3-e5f1-4128-9a9d-616e6b5bd1d8)

In the above diagram, i have used twin axis plotting. first axis is to plotting structures damaged using a bar chart. The second axis is used for plotting structures destroyed using a line plot with markers. These are all done using the Pandas library and Matplotlib plotting techniques.

### Average length of the Wildfire Per Year

This calculations finds number of days wildfire lasted in a year and averge of those days per year. Year, 2018 has total of 732 days of wildfire and is the highest number so far in between the years 2013 and 2025. Year, 2017 with 152 is the highest average number of wildfire days in a year.

![Screenshot 2025-02-11 at 10 40 50 PM](https://github.com/user-attachments/assets/df7f7169-2f69-459a-9f39-66d1abf78c91)


To create this interactive visualizations, i have to add **import plotly.graph_objects as go** as my dependencies. go.Bar() and go.Scatter() are part of this module. Since we already installed plotly, no need to install again. 

# Acknowledgement

For this project we used California Wildfire dataset from the site kaggel.com. Our teammate Dagim Girma has done cleaning and filtering of the dataset.

Our Instructor, Tuncay E. Dogan, provided great assistance in completing this project. He shared many helpful website links to explore new ideas in data visualization and improve our coding skills.

Various internet sites such as, Stack Overflow, GeeksForGeeks, and others were also helpful in times of error encounters and code generation.



