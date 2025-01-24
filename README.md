# Excel Salary Dashboard

![Slaray GIF](https://github.com/user-attachments/assets/3014ce30-9fa1-47fd-b3e8-aea0b754197b)

## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Jobs_Salary.xlsx](https://github.com/user-attachments/files/18530210/Jobs_Salary.xlsx)


### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Edacation**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

![Excel Salary](https://github.com/user-attachments/assets/7cbc40f1-33c1-4636-85b8-087e4eb3e475)


- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![Excel Map](https://github.com/user-attachments/assets/73202bb0-0ec0-4d0a-a139-092600009847)


- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=IFERROR(
  MEDIAN(
    IF(
      (Table1[Job Title]=B1)*
      (Table1[Salary]<>0)*
      (Table1[Country]=country)*
      (Table1[Education Level]=education_level),
      Table1[Salary]
    )
  ),
  "No Data"
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and Edacation.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and Edaction.

🍽️ Background Table

![Background_Table]
(https://github.com/user-attachments/assets/d72c1c31-b422-44c1-8999-c3b01e15fd9e)


📉 Dashboard Implementation

![Excel_table](https://github.com/user-attachments/assets/f9b8b483-2d36-4d4d-99b5-ec3241d0d033)


#### ⏰ Count of Edacation

```
=COUNTIFS(
    Salary_Data_Based_country_and_r!E2:E3134, IF(job_title="All", "*", job_title),
    Salary_Data_Based_country_and_r!H2:H3134, IF(country="All", "*", country),
    Salary_Data_Based_country_and_r!D2:D3134, IF(education_level="All", "*", education_level)
)
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

![1_Salary_Dashboard_Type.png](/0_Resources/Images/1_Salary_Dashboard_Screenshot2.png)

📉 Dashboard Implementation:

![Excel_Education](https://github.com/user-attachments/assets/dab031d4-cfaf-43e2-bf89-d0842ee4b311)


### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

<img src="/0_Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 
