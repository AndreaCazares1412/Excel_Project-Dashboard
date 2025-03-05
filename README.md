# Excel Salary Dashboard


## Introduction

This project was developed as part of the **[Excel for Data Analytics - Full Course by Luke Barousse](https://www.youtube.com/watch?v=pCJ15nGFgVg&t=5352s)**. The goal of this dashboard is to provide job seekers with the tools to explore salaries for various positions, helping them to make informed decisions and ensure they are being fairly compensated.

The data used in this project was sourced from the course materials, offering a comprehensive look at job titles, salaries, locations, and the skills required for each role. This dashboard serves as a practical example of how to analyze and visualize salary trends using **Excel**, a powerful tool for data analysis.

### Dashboard File
My final dashboard is in 

### Excel Skills Used
The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation

### Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

## Dashboard Build

### 📉 Charts

### 📊 Data Science Job Salaries - Bar Chart

image

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🗺️ Country Median Salaries - Map Chart

- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type - specified.

🍽️ Background Table

image

📉 Dashboard Implementation

image


### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

image

📉 Dashboard Implementation:

image

### ❎ Data Validation

### 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced
 
  image

  ## Conclusion
This dashboard was created to provide an overview of salary trends across various data-related job titles. Using data from the **[Excel for Data Analytics - Full Course by Luke Barousse](https://www.youtube.com/watch?v=pCJ15nGFgVg&t=5352s)**, this dashboard offers valuable insights that help users make informed decisions about their career paths. Through this project, I explored Excel's functionalities to understand how location and job type impact salaries, while reinforcing my knowledge and applying the skills I learned to create a useful and practical tool.


**Acknowledgments**
- This project was created as part of the "Excel for Data Analytics - Full Course" by Luke Barousse.
