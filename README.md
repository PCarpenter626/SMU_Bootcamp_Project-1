# California Wildfire Data Cleaning & Analysis (2013 - Present)

## Overview
This project aims to analyze California wildfire incidents from 2013 to the present. Specifically, my responsibility was to clean the dataset and answer the question: Is there a significant difference in acres burned between counties? The analysis was conducted using statistical testing, particularly Welch's ANOVA.

## Business Question & Motivation
- **Question:** Is there a significant difference in acres burned between counties?
- **Motivation:** Understanding county-level variations in wildfire impact can help allocate resources efficiently and develop better mitigation strategies.

## Project Goals & Methods
- **Goal:** Clean and preprocess the data to enable statistical analysis and Determine if there is a statistically  significant difference in acres burned across different counties.
- **Method:** Perform statistical testing:
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
5. **Estimating Missing Fire Extinguished Dates**
   - Categorized acres burned into bins.
   - Calculated median extinguishing time for each bin.
   - Estimated missing Fire Extinguished dates using the median values.

## Export
After cleaning, the final dataset was successfully exported to the output folder for analysis.


