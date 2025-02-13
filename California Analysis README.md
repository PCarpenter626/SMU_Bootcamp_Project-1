f# SMU_Bootcamp_Project-1: California Wildfire Analysis

# California Wildfire Analysis (2013 - 2024)

## Project Overview
This project analyzes the impact of wildfires in California from 2013 to 2024 using data-driven techniques, statistical analysis, and visualizations. It examines wildfire behavior, key environmental factors, and correlations with various variables to provide a comprehensive understanding of wildfire trends and their consequences.

The analysis explores patterns in wildfire occurrences, identifies factors influencing fire severity, and assesses their impact on air quality, vegetation recovery, and emergency response efforts. By leveraging time-series analysis and statistical testing, this study offers insights into wildfire trends and possible mitigation strategies.

## Project Goals
The primary objectives of this project are:

1. **Analyze Annual Wildfire Impact**: Identify trends in acres burned, affected counties, personnel involvement, structures damaged, and fire duration.
2. **Assess Climate and Seasonal Influences**: Examine correlations between temperature, humidity, seasonality, and wildfire extent.
3. **Investigate Vegetation Recovery Constraints**: Identify factors that hinder regrowth in fire-affected regions.
4. **Perform Time-Series Analysis**: Visualize wildfire trends over time to detect patterns and fluctuations.
5. **Conduct Correlation Studies**: Explore relationships between variables such as:
   - Injuries vs. Acres Burned
   - Helicopters vs. Acres Burned
   - Water Tenders vs. Acres Burned
   - First Responders vs. Acres Burned
6. **Analyze Air Quality Impact**: Assess how wildfires influence air pollution levels.
7. **Classify Wildfire Sizes**: Categorize wildfires based on severity and affected areas.
8. **Perform County-Level Analysis**: Evaluate regional differences in wildfire severity and investigate the high wildfire impact in Siskiyou County.
9. **Conduct Statistical Testing**: Use hypothesis testing to identify significant trends and relationships.

## How These Goals Are Achieved
To achieve these objectives, the project employs the following methodologies:

- **Data Collection & Preprocessing**: Compiles wildfire data from government sources and cleans it for analysis.
- **Exploratory Data Analysis (EDA)**: Uses descriptive statistics and visualizations to identify key trends.
- **Time-Series Analysis**: Applies visualization techniques to observe long-term wildfire trends.
- **Statistical Analysis & Hypothesis Testing**: Determines significant relationships between wildfire characteristics.
- **Correlation Studies**: Uses statistical measures to evaluate the strength of relationships between variables.
- **Data Visualization**: Uses graphs, heatmaps, and geospatial mapping for better insight presentation.

By integrating these techniques, this project provides valuable insights into California's wildfire patterns, their driving factors, and potential mitigation strategies.


## Installation & Usage Instructions
This project utilizes the following Python libraries. Install them using pip if not already installed:

```bash
pip install pandas numpy matplotlib seaborn scipy pingouin hvplot geopandas
```

## Libraries Used
- `pandas`: Data manipulation and analysis
- `numpy`: Numerical computations
- `matplotlib.pyplot`: Data visualization
- `seaborn`: Statistical data visualization
- `scipy.stats`: Statistical analysis
- `pingouin`: Statistical hypothesis testing
- `hvplot.pandas`: Interactive plotting
- `geopandas`: Geospatial analysis
- `datetime`: Date and time manipulation
- `plotly.express`: Interactive visualizations
- `plotly.graph_objects`: Advanced plotting
- `time`: Time-related functions
- `scipy.stats.linregress`: Linear regression analysis
- `scipy.stats.spearmanr`: Spearman correlation analysis
- `pathlib.Path`: File system path handling
- `pyproj`: Coordinate reference system transformations
- `cartopy`: Geospatial mapping
- `geoviews`: Geographic data visualization
- `os`: Operating system interface
- `dotenv.load_dotenv`: Environment variable handling 

 ## Data Preprocessing & Cleaning
The project uses two datasets:

### **Dataset 1: mapdataall.csv**
- **Source:** California Department of Forestry and Fire Protection
- **Data:** Wildfire incidents in California from 2013 to present
- **Shape:** (2835, 23)
- **Columns Retained:** 9 columns selected for analysis

### **Dataset 2: California_Fire_Incidents.csv**
- **Source:** Kaggle - California Wildfire Incidents
- **Data:** Wildfire incidents in California from 2013 to 2020
- **Shape:** (1636, 40)
- **Columns Retained:** 14 columns selected for analysis

### **API Dataset 3:
- **Source** Openmateo http://openmeteo.com/
- **Data:**Climate and weather
- **Shape:** 2922 row x 4 coluns

### Cleaning Process
1. **Data Import & Filtering**
   - Imported both datasets.
   - Retained relevant columns for analysis (9 from Dataset 1, 14 from Dataset 2).
2. **Handling Duplicates & Missing Data**
   - Removed duplicate rows based on unique incident IDs in Dataset 2.
   - Missing values in key columns were filled with 0.
3. **Merging Datasets**
   - Merged datasets on unique incident ID.
   - Filled missing values for rows from 2020 to present with 0.
   - Renamed columns for clarity and consistency.
4. **Checking & Handling Null Values**
   - **Fire Extinguished:** 625 missing values.
   - **Administrative Unit:** 56 missing values filled with 'Unknown'.
   - **Acres Burned:** 53 missing values dropped.
   - **County:** 10 missing values manually filled using latitude and longitude.
   - **Fire Duration:** 65 missing or incorrect values removed making accuarte readings.
5. **Estimating Missing Fire Extinguished Dates**
   - Categorized acres burned into bins.
   - Calculated median extinguishing time for each bin.
   - Estimated missing Fire Extinguished dates using the median values.

## Additional Information and Images
![This graph shows total and avg days of a wildfire per year](https://github.com/user-attachments/assets/2e7363ac-5747-40fd-9427-a1266ab010b3)
- This graph shows the total and average days of a wildfire per year

![Total Counties Burned Per year](https://github.com/user-attachments/assets/4df1c53d-c0ca-4bb7-b0fe-d676dcbd200d)
- Here shows the total counties burned per year.
- 2018 was one of the most descructive years per the graph

![Acres burned per year](https://github.com/user-attachments/assets/dac81eaa-fe8e-4453-a95f-c6e5a554a71b)
- Showing the acerage burned per year, this graph shows how the majority happened in the 2018 season 

![Personnel Involved Per year](https://github.com/user-attachments/assets/2e70c053-3bf8-4877-b06a-9bd2fde09bf7)
- With the decreasing number of Personnel involved to respond to the fires its taking longer for them to be contained

![Humidity v Acres ](https://github.com/user-attachments/assets/ae5b1d83-fae1-47f1-8d4b-2508365c56d6)
- The correlation between humidity and severity of the fires is shown here
- Higher humidity correlates with the how many acres burned

![image](https://github.com/user-attachments/assets/411ac995-f5c8-4395-afa5-46b49c6e848c)
- Siskiyou county has the largest wildfire area
- After statistical testing and doing a hypothesis test we found that due to the conditions and climate of the northern-most county, it is a prone to larger longer wildfires
- Siskiyou counties is made up of mostly wildlife and forest and lies predominantly on volcanic land/soil.


### Major Findings
- What we have found from our research is that 2018 Saw the most affected counties and had the most destroyed during the fires with 2020 and 2021 having the highest acres burned. If the number of personnel increased the containment time for the wildfires could lessen.

### Limitations of Current Approaches to California Wildfires
1. **Resource Constraints**: Firefighting resources, including personnel, equipment, and funding, are often limited, especially during peak wildfire seasons. This can hinder effective response and containment efforts.
2. **Climate Change Impact**: Increasing temperatures and prolonged drought conditions due to climate change exacerbate wildfire risks, making it difficult to predict and manage fire behavior.
3. **Land Management Practices**: Historical land management practices, such as fire suppression and lack of controlled burns, have led to an accumulation of fuel (dead trees, brush, etc) that can intensify wildfires.
4. **Urban-Wildland Interface**: The expansion of urban areas into wildland regions increases the risk of property damage and loss of life during wildfires, complicating evacuation and response strategies.
5. **Data Limitations**: While technology has improved, there are still gaps in real-time data collection and analysis regarding fire behavior, weather conditions, and vegetation health, which can hinder effective decision-making.
6. **Public Awareness and Preparedness**: Many residents in fire-prone areas may lack awareness of wildfire risks and preparedness measures, leading to inadequate responses during emergencies.

### Future Development 
1. **Enhanced Predictive Modeling**: Investing in advanced modeling techniques that incorporate climate data, vegetation health, and historical fire behavior can improve predictions of wildfire risks and behavior.
2. **Improved Land Management**: Implementing more proactive land management strategies, including controlled burns and forest thinning, can reduce fuel loads and mitigate the severity of wildfires.
3. **Community Engagement and Education**: Increasing public awareness and preparedness through community programs can help residents understand risks and develop effective evacuation plans.
4. **Technological Innovations**: Utilizing drones, satellite imagery, and AI for real-time monitoring and assessment of wildfire conditions can enhance response efforts and resource allocation.
5. **Policy and Funding**: Advocating for policies that prioritize wildfire prevention and response funding can ensure that resources are available for effective management and recovery efforts.
6. **Collaboration and Partnerships**: Strengthening collaboration between government agencies, non-profits, and local communities can lead to more coordinated and effective wildfire management strategies.


### Conclusion
 The analysis of California wildfires from 2013 to 2024 highlights significant trends in wildfire behavior, impact, and response efforts. The most widespread wildfires occurred in 2020 and 2021, burning over 2 million acres each year, while 2018 saw the highest number of affected counties. Structural damage was most severe in 2017 and 2018, reinforcing the growing threat of wildfires. Seasonal patterns reveal that July and August are the peak months, with wildfires more likely to occur when temperatures exceed 20°C. Additionally, data shows a strong correlation between temperature and acres burned, emphasizing the role of climate conditions in wildfire severity. The deployment of more personnel is linked to reduced wildfire spread, indicating the effectiveness of response efforts. While most wildfires remain relatively small, no statistical evidence suggests significant differences in acres burned across counties. Understanding these patterns is crucial for improving fire management strategies and mitigating future wildfire risks.

#### References
- [Kaggle](Kaggel.com)
- [Cali.gov](www.fire.ca.gov/our-impact)
- [Wiki California wildfire](https://en.wikipedia.org/wiki/List_of_California_wildfires) 
- [enviroliteracy](https://enviroliteracy.org/how-long-can-a-wildfire-last)
- [frontline fire](https://www.frontlinewildfire.com/california-wildfire-map)
- [mateo](http://openmeteo.com/)


#Team Members:</p>
_Arangassery, Tiya_</p>
_Brewer, Vanessa_</p>
_Carpenter,Patrick_</p>
_Daniels,Ricia_</p>
_Girma,Dagim_</p>
_Gonzalez,Fransicso_</p>
_Guerrero,Sergio_</p>
_Shchepotkina,Elena_</p>
_Westlman,Matt_</p>



### Acknowledgement

For this project we used California Wildfire dataset from the site kaggel.com. Our teammate Dagim Girma has done cleaning and filtering of the dataset.

Our Instructor, Tuncay E. Dogan, provided great assistance in completing this project. He shared many helpful website links to explore new ideas in data visualization and improve our coding skills.

Weather data was taken hourly from points in the North, Center and South of California– Sacramento, Fresno and Los Angeles, points and times were averaged together to get “Daily Average” weather data for California

Various internet sites such as, Stack Overflow, GeeksForGeeks, and others were also helpful in times of error encounters and code generation.



