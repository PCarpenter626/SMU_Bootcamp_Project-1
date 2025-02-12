# SMU_Bootcamp_Project-1
SMU Group Project 1
 In this project, we worked as a team of 9 members. we choose to analize and work with dataset "California Wildfire"
using Python I
Calculate and Display top 10 Acres Burned 
Calculate and Display top 10 Counties Burned
Find out which county had the longest lasting fire

For my next tesk I used another dataset "California airquality"
to analyze the impact of California wildfires on air quality. It integrates wildfire data with air quality measurements to visualize the correlation between fire incidents and air pollution levels.

I merged two datasets:

Wildfire Data (df):

Contains information about wildfire incidents, including location, size, and response details.

Key columns: Incident Name, County, Acres Burned, Latitude, Longitude, Fire Started, Fire Extinguished.

Air Quality Data (airquality_es):

Provides air pollution measurements across different locations in California.

Key columns: SITE_LATITUDE, SITE_LONGITUDE, DAILY_AQI_VALUE, AQI_Color, AQI_Category.


Ensure the following Python libraries are installed:

pandas

plotly

dotenv
my tesk

1.Categorized AQI


2.Loads the Mapbox API key for visualizing data on a map.


3.Lists the column names in both datasets to confirm structure.

4. Visualizing Air Quality on a Map


Uses plotly.express to plot air quality data on a Mapbox map.

Colors represent AQI categories, and point size is based on AQI values.

Usage

Ensure your .env file contains a valid MAPBOX_API_KEY.

Run the Jupyter Notebook to analyze and visualize the data.

Modify the visualization to explore different relationships, such as overlaying wildfire locations on air quality data.

Future Improvements

Merge fire and air quality data to find correlations.

Analyze time-series trends to observe pollution spikes during fire.

Improve visualizations with interactive filters for better insights.

 

 



