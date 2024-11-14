# Olympics-Data-Analysis-Project

### Introduction/Overview
For this project, we are doing exploratory data analysis on Olympics Games data. Our objective was to develop a comprehensive and interactive Power BI report that showcases insights into key aspects of the Olympics. This project serves as a demonstration of our data analysis skills, from data import and transformation to data modeling and visualization.

### Data Import Process
To begin the analysis, we imported two(2) CSV files format that captured different aspects of the Olympics. Each dataset provided a unique view of the event, such as athlete names, countries, gender, disciplines, sports, events and the number of medals won. The primary datasets we used included:

Summer & Winter csv: Contains information about athletes, including their country and discipline, the total count of gold, silver, and bronze medals won by countries. And also, shows the gender distribution of participants in each discipline. It is an open source data that was freely downloaded from Kaggle.com.

Power BI’s 'Get Data' feature made the import process seamless, supporting various file formats. We used CSV files, which were easily integrated into Power BI. During this step, we ensured that all datasets were formatted consistently, and we took note of any potential issues like missing values or incorrect data types.

Challenges faced: 

One of the datasets had inconsistent data formats, such as commas in the name field or text fields where numeric values were expected. These issues were resolved during the data transformation phase and ......(Mazi Ben to supply how he was able to clean the data)

### Tool Used
- Microsoft Excel [Download Here](https://www.microsoft.com)
- Microsoft Power Bi
  
### Data Transformations 
Data cleaning and transformation are critical steps in preparing raw data for analysis. In Power BI, we used Power Query to apply various transformations, ensuring that the data was consistent, accurate, and ready for analysis.
Key transformations we applied included:

Replacing Values:  we replaced missing or inconsistent values using Power Query’s Replace Values feature, especially in cases where country names or abbreviations were inconsistent across datasets.

Data Type Corrections: Ensured that numeric fields (e.g., number of medals or athletes) were set to the correct data types, avoiding text or mixed data formats.

Calculated Columns: We added calculated columns for total medal to ensure these values could be easily referenced during the data modeling phase.

This transformation phase ensured that the data was clean and cohesive, making the modeling and visualization processes more efficient.

### Key insights include: 
 
We analyze the performance of men versus women in the Olympic Games. By categorizing medal count and gender, we can discern how some countries may have higher performing athletes from men or women.

1. Count of Medal By Gender 

2. Total number of medals won by countries.

3. Distribution of athletes by gender and sports.

4. Country-wise Medal Count

5. Top 10 Countries by Medals

### Crafting DAX Measures for Deeper Insights

Once the model was established, we used DAX (Data Analysis Expressions) to create dynamic measures for key insights. These measures allowed us to perform complex calculations on the fly, enabling the dashboard to display dynamic and context-sensitive metrics based on the user’s interactions.
Key measures created:

i. Total Sports:

``` CALCULATED MEASURE
SELECT * FROM THE OLYMPIC DATA TABLE
WHERE Total Sports = SUM(Sports[Total])
```

This measure calculated the total number of medals won by each 
country across all disciplines.

ii. Total Athletes:

``` CALCULATED MEASURE
SELECT * FROM THE OLYMPIC DATA TABLE
WHERE Total Athletes = COUNTROWS(Athletes)
```

This measure counted the total number of athletes across all countries 
and disciplines.



