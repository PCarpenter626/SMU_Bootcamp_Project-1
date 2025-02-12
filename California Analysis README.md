# SMU_Bootcamp_Project-1: California Wildfire Analysis

## _Overview_
This is our first group project where we showcase the information we've learned thus far for Mining, cleaning and visualizing a data set. For our project we chose to analyze the California wildfires from 2013 - present times specifically focusing on the following 10 counties.
1. RiverSide,
2. Los Anfeles,
3. San Diego,
4. San Luis Obispo,
5. Butte,
6. Fresno,
7. San Bernadino,
8. Siskiyou,
9. Kern
10. Tulare</p>
We used various Python libraries and created indivdual branches to save and share our findings. We pulled data from APIs and other data sets, created graphs and heat maps and all collectively wrote code to assist with our overall findings.

## _Questions_
We started by creating the following reserach questions:
- How have wildfire occurrenceds changed in California from 2013 - current?
- What is the total acres burned per year?
- How long do wildfires typicallay last, and has this changed over the years?
-  How do firefighting resources impact containment time?
  
#### From our reserach questions, We came up with different Hypothesis and a statistical summary that we teamed up to breakdown.
- Yearly Summary Statistics such as acres and counties burned, The Personanel involved, the structures damaged/ destroyed and the average length of Wildfires per year.</p>  _Specifically Tiya calculated the following_:<br>
              - Calculate and Display Acres Burned Per Year <br>
              - Calculate and Display Counties Burned Per Year <br>
              - Calculate and Display Personnel Involved Per Year <br>
              - Calculate and Display Structures Damaged and Destroyed Per Year <br>
              - Calculate and Display the Average length of the Wildfire Per Year <br>

-  Does the temperature, humidity and time of year have a correlation with the number of acres burned? - _Matt_
- What is the environmental impact of wildfires; Specifically the severity of the fires and the time it took for containment as well as how it effected the vegetation of the land and soil. - _Ricia_
- 
- Is there a correlation between Personnel Involved and First Responders. </p> **Hypothesis:** I believe there is a Correlation. I believe the more personnel involved, the less acres burned -_Patrick_
- Which California counties have Experienced the highest numebr of wildfires? - _Elena_
- Is there a correlation between acres burned and fatalities? - _Sergio and Francisco_
-  Is there a significant differnece in the average acres burned between counties? - _Dagim and Vanessa_
  
## Project Goals & Methods
- **Goals:** Clean and preprocess the data to enable statistical analysis and Determine if there is a statistically  significant difference in acres burned across different counties.


- **Method:** Perform statistical testing and dissect and slice the cleaned DataFrame to calculate the total Acres Burned and the total Personnel Involved from the 10 counties. From there, we display the data in graphical form and draw a conclusion from the displayed Data. 

  - **Data Cleaning:** Handling missing values, duplicates, and merging datasets
  - **Statistical Testing:** Performing Welch's ANOVA test to compare mean acres burned across counties.
 

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

## Export
After cleaning, the final dataset was successfully exported to the output folder for analysis.

