# Olympics-Data-Analysis-Project

## Table of Outline
## [Project Overview](#project-overview)
## [Data Import Process](#data-import-process)
## [Tool Used](#tool-used)
## [Data Transformations](#data-transformations)
## [Key Insights Include](#key-insights-include)
## [Crafting DAX Measures for Deeper Insights](#crafting-dax-measures-for-deeper-insights)
## [Data Visualization](#data-visualization)
## [Conclusion](#conclusion)

### Project Overview
---
For this project, we are doing exploratory data analysis on Olympics Games data. Our objective was to develop a comprehensive and interactive Power BI report that showcases insights into key aspects of the Olympics. This project serves as a demonstration of our data analysis skills, from data import and transformation to data modeling and visualization.

### Data Import Process
---
To begin the analysis, we imported two(2) CSV files format that captured different aspects of the Olympics. Each dataset provided a unique view of the event, such as athlete names, countries, gender, disciplines, sports, events and the number of medals won. The primary datasets we used included:

**Summer & Winter csv**: Contains information about athletes, including their country and discipline, the total count of gold, silver, and bronze medals won by countries. And also, shows the gender distribution of participants in each discipline. It is an open source data that was freely downloaded from Kaggle.com.

Power BI’s 'Get Data' feature made the import process seamless, supporting various file formats. We used CSV files, which were easily integrated into Power BI. During this step, we ensured that all datasets were formatted consistently, and we took note of any potential issues like missing values or incorrect data types.

**Challenges faced**: 

One of the datasets had inconsistent data formats, such as commas in the name field or text fields where numeric values were expected. These issues were resolved during the data transformation phase and ......(Mazi Ben to supply how he was able to clean the data)

### Tool Used
---
- Microsoft Excel [Download Here](https://www.microsoft.com)
- Microsoft Power Bi
  
### Data Transformations 
---
Data cleaning and transformation are critical steps in preparing raw data for analysis. In Power BI, we used Power Query to apply various transformations, ensuring that the data was consistent, accurate, and ready for analysis.
**Key transformations we applied included**:

**Replacing Values**:  we replaced missing or inconsistent values using Power Query’s Replace Values feature, especially in cases where country names or abbreviations were inconsistent across datasets.

**Data Type Corrections**: Ensured that numeric fields (e.g., number of medals or athletes) were set to the correct data types, avoiding text or mixed data formats.

**Calculated Columns**: We added calculated columns for total medal to ensure these values could be easily referenced during the data modeling phase.

This transformation phase ensured that the data was clean and cohesive, making the modeling and visualization processes more efficient.

### Key insights include: 
---
We analyze the performance of men versus women in the Olympic Games. By categorizing medal count and gender, we can discern how some countries may have higher performing athletes from men or women.

1. Count of Medal By Gender 

2. Total number of medals won by countries.

3. Distribution of athletes by gender and sports.

4. Country-wise Medal Count

5. Top 10 Countries by Medals

### Crafting DAX Measures for Deeper Insights
---
Once the model was established, we used DAX (Data Analysis Expressions) to create dynamic measures for key insights. These measures allowed us to perform complex calculations on the fly, enabling the dashboard to display dynamic and context-sensitive metrics based on the user’s interactions.
Key measures created:

i. **Total Sports**:

``` CALCULATED MEASURE
SELECT * FROM THE OLYMPIC DATA TABLE
WHERE Total Sports = SUM(Sports[Total])
```

This measure calculated the total number of medals won by each 
country across all disciplines.

ii. **Total Athletes**:

``` CALCULATED MEASURE
SELECT * FROM THE OLYMPIC DATA TABLE
WHERE Total Athletes = COUNTROWS(Athletes)
```

This measure counted the total number of athletes across all countries 
and disciplines.

### Data Visualization
---
**Title**: Creating Interactive Dashboards with Power BI

We focused on creating highly interactive and visually engaging dashboards using a variety of Power BI features, including buttons, slicers, and custom visuals. The goal was to provide users with an intuitive experience where they could explore the data and uncover insights on their own.
Visuals used:

**Card Visuals**: Displayed key metrics such as Total Medals, Total Athletes, and Total Countries.

**Bar and Column Charts**: Used to show the distribution of medals by country, athlete participation by sports, and the number of countries participating in each event.

**Slicers**: Added for filtering by Country, Events, and Gender to allow users to focus on specific aspects of the data.

**Buttons for Page Navigation**: We created custom buttons for smooth navigation between different report pages, including Summary, Medals Overview, Athletes Performance, and Countries.

**Pie Charts and Maps**: Used to display the Medal Distribution across countries and global participation in the Olympics.

**Example screenshot**:

![Olympics Dashboard 1](https://github.com/user-attachments/assets/c30b8dbb-247f-40e6-a10e-1206bb3fb3e3)

![Olympics Dashboard 2](https://github.com/user-attachments/assets/f7965d33-f966-4dae-b34b-e10b0750b5d4)

![Olympics Dashboard 3](https://github.com/user-attachments/assets/b4f15ecf-72a2-4133-8e7e-c0f7be24a925)

### Conclusion
---
This project showcases the end-to-end process of working with Power BI, from data import and transformation to building advanced data models and creating interactive dashboards. The result is a comprehensive report that provides valuable insights into the Olympics, making it easy to explore medal distributions, athlete participation, and country rankings.
Working on this project allowed us to deepen our expertise in Power BI, particularly in crafting efficient data models, writing dynamic DAX measures, and creating user-friendly visualizations. We look forward to applying these skills in real-world business environments to deliver actionable insights.
“Explore the full interactive report here: Power BI Olympic Report”.
