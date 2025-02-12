# SMU_Bootcamp_Project-1: California Wildfire Analysis

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

### Libraries Used
- `pandas`: Data manipulation and analysis
- `numpy`: Numerical computations
- `matplotlib.pyplot`: Data visualization
- `seaborn`: Statistical data visualization
- `scipy.stats`: Statistical analysis
- `pingouin`: Statistical hypothesis testing
- `hvplot.pandas`: Interactive plotting
- `geopandas`: Geospatial analysis


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

## Additional 
After cleaning, the final dataset was successfully exported to the output folder for analysis.

### Conclusion
 The analysis of California wildfires from 2013 to 2024 highlights significant trends in wildfire behavior, impact, and response efforts. The most widespread wildfires occurred in 2020 and 2021, burning over 2 million acres each year, while 2018 saw the highest number of affected counties. Structural damage was most severe in 2017 and 2018, reinforcing the growing threat of wildfires. Seasonal patterns reveal that July and August are the peak months, with wildfires more likely to occur when temperatures exceed 20°C. Additionally, data shows a strong correlation between temperature and acres burned, emphasizing the role of climate conditions in wildfire severity. The deployment of more personnel is linked to reduced wildfire spread, indicating the effectiveness of response efforts. While most wildfires remain relatively small, no statistical evidence suggests significant differences in acres burned across counties. Understanding these patterns is crucial for improving fire management strategies and mitigating future wildfire risks.






