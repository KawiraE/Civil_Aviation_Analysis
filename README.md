# Civil_Aviation_Analysis


DATA CLEANING

Data cleaning is a fundamental process in preparing the dataset for analysis. 
This step involves identifying and correcting any issues within our dataset to ensure its reliability and validity. The aviation accident dataset, spanning incidents from 1962 to 2023, will undergo various cleaning techniques to address missing values, inconsistencies, and other data quality issues.

Here’s a detailed breakdown of the steps involved in this process:

1. Identifying and Handling Missing Values

Assessment: Each column was analyzed to determine the extent of missing values. Columns with excessive missing data, such as those with over 30-40% missing values, were reviewed to evaluate their importance to the analysis.
Strategies Used:
- numerical columns (e.g., fatalities or injuries), missing values were replaced using the mean or median, depending on the distribution of the data. This ensures that outliers do not distort the imputation process.
- categorical columns (e.g., cause of accident, aircraft type), missing values were replaced with "Unknown" to maintain the context of the dataset without introducing bias.

2. Identifyng and Removing Duplicate Records if any.

Duplicate rows can occur due to data entry errors or redundant records in the source dataset. 

3. Standardizing Data Types

Ensuring correct data types for each column is essential for seamless processing and analysis:
Dates: The "Date" column was converted to a datetime format, enabling accurate time-based analysis, such as accident trends over decades.
Numerical Fields: Columns such as "Fatalities" and "Injuries" were confirmed as float or int types to allow calculations and aggregations.
Text Columns: Categorical fields (e.g., "Aircraft Type" or "Cause of Accident") were standardized by normalizing case (e.g., converting all text to lowercase) and stripping unnecessary whitespace or punctuation.

4. Addressing Inconsistencies

Inconsistencies in the data, such as variations in formatting or naming conventions, will be identified and corrected:
Geographical Data: The supplementary USState_Codes.csv file was utilized to map state abbreviations (e.g., "CA") to their full names (e.g., "California"), ensuring consistency in the "Location" column.
Categorical Data: Variants of the same category (e.g., "Boeing 737" vs. "Boeing-737") were consolidated into a single, standardized format.

5. Detecting and Handling Outliers

Outliers—values that deviate significantly from the norm—can distort the analysis if not addressed:
Numerical Columns: Columns like "Fatalities" and "Injuries" were assessed for extreme values. Outliers were either retained if they were deemed relevant (e.g., rare but valid incidents) or flagged for exclusion if they were likely errors.
Approach: Boxplots and histograms were used to visualize distributions and identify potential outliers.

6. Final Validation

Once the data cleaning steps were completed, the dataset underwent thorough validation to ensure its readiness for analysis:
Summary Statistics: The .describe() function was used to generate statistical summaries, confirming the accuracy and consistency of numerical data.
Spot Checks: Random samples of the dataset were inspected to verify that missing values were appropriately handled, duplicates were removed, and data types were consistent.
Shape Check: The .shape attribute was used to confirm the final number of rows and columns in the cleaned dataset, ensuring alignment with expectations.

7. Preparing for Visualization

To streamline the visualization process, the cleaned dataset will be aggregated where necessary.
Key groupings include:
- Grouping by aircraft model to analyze accident rates.
- Summarizing by cause of accident to identify the leading factors.
- Aggregating by year to observe trends over time.

##### OBJECTIVES OF DATA CLEANING 

- Identify missing values in a dataframe using built-in methods
- Explain why missing values are a problem in data science
- Determine and implement the optimal technique for dealing with missing, duplicate, and erroneous values in a given dataset.

### **Data Visualization Introduction 

The data visualization phase transforms raw aviation accident data into meaningful insights through a range of compelling plots. By analyzing trends over time, geographical patterns, weather impacts, and flight phases, this section sheds light on key safety challenges. These visualizations aim to support stakeholders in identifying high-risk factors and formulating strategies to enhance aviation safety.

### **OVERVIEW**

The visualization phase of this project was designed to uncover insights and trends within the aviation accident dataset, using a range of compelling plots to analyze various aspects of the data. Below is an overview of the visualizations created and their corresponding insights:

1. **Number of Accidents Over Time**:
   - A line plot revealed temporal trends, showing fluctuations in accidents over decades and indicating potential improvements in aviation safety.

2. **Distribution of Accident Severity**:
   - A bar plot highlighted the frequency of accidents categorized as minor, serious, or fatal, offering insights into the severity of aviation incidents.

3. **Accidents by Day of the Week**:
   - A bar plot explored weekday patterns, identifying the days with the highest accident occurrences.

4. **Most Common Aircraft Types**:
   - A horizontal bar plot showcased the top aircraft models involved in accidents, helping pinpoint frequently involved designs.

5. **Geographical Distribution of Accidents**:
   - An interactive heatmap visually emphasized high-risk regions, providing a geographical perspective on accident density.

6. **Types of Injuries vs. Phase of Flight**:
    - A stacked bar plot illustrated the distribution of injury severity (fatal, serious, minor) across flight phases, highlighting high-risk stages like takeoff and landing.

7. **Accidents by Number of Engines**:
   - A bar plot analyzed accident proportions by engine type, shedding light on risks associated with single-engine, twin-engine, and multi-engine aircraft.

8. **Impact of Weather Conditions**:
   - A scatter plot revealed the relationship between weather conditions and accident fatalities, identifying the weather scenarios with the highest risks.

9. **Manufacturer vs. Number of Engines**:
   - A stacked bar plot uncovered trends across manufacturers and engine types, helping stakeholders assess which combinations are more prone to accidents.


### **Insights from the Visualization Phase**
- Identified high-risk conditions and phases (e.g., landing and takeoff).
- Revealed geographical regions with frequent accidents and their possible contributing factors.
- Pinpointed aircraft types, manufacturers, and weather conditions associated with higher risk.
- Provided actionable insights to guide improvements in aviation safety protocols, training, and operations.

These visualizations played a key role in transforming raw data into meaningful insights, equipping stakeholders with a deeper understanding of aviation safety dynamics and areas for improvement.

