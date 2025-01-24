# Jobs Salary Dashboard

![Slaray GIF](https://github.com/user-attachments/assets/3014ce30-9fa1-47fd-b3e8-aea0b754197b)

## Introduction

This Excel-based salary dashboard is designed to help job seekers and professionals analyze salaries for various roles, countries, and industries. The dashboard provides insights into salary trends, allowing users to make informed decisions about career growth and compensation expectations.

The project uses a dataset from 2023 with comprehensive information about job titles, salaries, geographic locations, and educational levels.

### Dashboard File
My final dashboard is in [Jobs_Salary.xlsx](https://github.com/user-attachments/files/18530210/Jobs_Salary.xlsx)


### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts** For visualizing salary distributions, top-paying roles, and regional disparities.
- **🧮 Formulas and Functions** To calculate median salaries, filter data dynamically, and perform multi-criteria analysis.
- **❎ Data Validation** For ensuring accurate and consistent user inputs.

### Dataset Overview

The dataset contains real world data related to data science jobs, including:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Education**
  The data includes over 6,700 entries and covers critical metrics such as salary distribution, years of experience, and gender demographics.
## Dashboard Features and Insights

### 📉 Charts

#### 📊 Salary Distribution

![Excel Salary](https://github.com/user-attachments/assets/7cbc40f1-33c1-4636-85b8-087e4eb3e475)


- 🛠️ **Excel Features:** Histogram showcasing the salary spread, with markers for median and percentile ranges.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** Most salaries fall between $70,000 and $160,000, with senior roles earning significantly higher.

#### 🗺️ Country Median Salaries - Map Chart

![Excel Map](https://github.com/user-attachments/assets/73202bb0-0ec0-4d0a-a139-092600009847)


- 🛠️ **Excel Features:**  Map chart showing median salaries by country.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Canada, China, and the UK have the highest median salaries, exceeding $115,000.

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

- 🔍 **Multi-Criteria Filtering:**  Nested IF statements with MEDIAN() and error handling using IFERROR().
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and Edacation.
- **🔢 Formula Purpose:** Dynamically calculates the median salary based on job title, country, and education level.

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


- **🔢 Formula Purpose:** TFilters and counts unique entries in the dataset based on criteria like job title, country, and education level.

🍽️ Background Table

![1_Salary_Dashboard_Type.png](/0_Resources/Images/1_Salary_Dashboard_Screenshot2.png)

📉 Dashboard Implementation:

![Excel_Education](https://github.com/user-attachments/assets/dab031d4-cfaf-43e2-bf89-d0842ee4b311)


### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced User Experience:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Education` option in the Data tab ensures:
    - 🎯 Predefined lists for job titles, countries, and education levels using Excel’s data validation feature.
    - 🚫Prevents incorrect entries and ensures consistency.
    - 👥 Overall usability of the dashboard is enhanced.

<img src="/0_Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

## Conclusion

This dashboard offers valuable insights into salary trends across job roles, countries, and educational backgrounds. The project demonstrates the powerful capabilities of Excel in analyzing and visualizing real-world data, enabling professionals to make data-driven career decisions.
