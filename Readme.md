# HR Analytics Dashboard | Power BI | Star Schema Data Warehouse

## Project Overview

This project demonstrates an end-to-end HR Analytics solution developed using Power BI and a Star Schema data model. The objective is to transform HR data into meaningful business insights that support workforce planning, compensation analysis, employee performance evaluation, and strategic decision-making.

The project highlights core Business Intelligence concepts including data modeling, dimensional modeling, DAX measure development, KPI design, and interactive dashboard creation.

---

## Business Problem

Organizations often face challenges in obtaining a consolidated view of workforce performance, payroll expenses, training effectiveness, and departmental productivity. This dashboard addresses these challenges by providing:

* Workforce visibility across departments and locations
* Compensation and payroll analysis
* Employee performance monitoring
* Training effectiveness evaluation
* Department-level workforce insights
* Executive-level KPI reporting

---

## Data Architecture

The dataset is modeled using a Star Schema design to optimize analytical performance and reporting flexibility.

### Fact Table

**FactHR**

* Salary
* Bonus
* Training Hours
* Performance Score
* Employee Key
* Department Key
* Job Key
* Location Key
* Date Key

### Dimension Tables

**DimEmployee**

* Employee ID
* Employee Name
* Gender

**DimDepartment**

* Department Name

**DimJob**

* Job Title

**DimLocation**

* Location Information

**DimDate**

* Year
* Month
* Quarter
* Calendar Attributes

---

## Dashboard Pages

### Executive Overview

Key Metrics:

* Total Employees
* Total Payroll Cost
* Average Salary
* Average Performance Score
* Total Bonus
* Total Training Hours

Visualizations:

* Department Headcount
* Payroll Trend Analysis
* Employee Distribution
* Top Paid Employees

### Workforce Analysis

Key Metrics:

* Male Employees
* Female Employees
* Total Departments
* Total Locations

Visualizations:

* Gender Distribution
* Employees by Department
* Employees by Job Role
* Employees by Location

### Compensation Analytics

Key Metrics:

* Total Compensation
* Average Compensation
* Bonus Percentage
* Payroll Cost

Visualizations:

* Salary by Department
* Salary by Location
* Compensation Breakdown
* Top Paid Employees

### Performance & Training

Key Metrics:

* Average Performance Score
* Training Hours per Employee
* Top Performers
* Total Training Hours

Visualizations:

* Performance by Department
* Training vs Performance Analysis
* Employee Performance Distribution

### Time Intelligence Analysis

Key Metrics:

* Current Year Payroll
* Previous Year Payroll
* Payroll Growth Percentage
* Running Payroll

Visualizations:

* Monthly Payroll Trends
* Payroll Growth Trends
* Department Performance Trends

---

## DAX Measures Implemented

```DAX
Headcount =
DISTINCTCOUNT(FactHR[EmployeeKey])

Payroll Cost =
SUM(FactHR[Salary])

Total Compensation =
SUM(FactHR[Salary]) +
SUM(FactHR[Bonus])

Average Performance =
AVERAGE(FactHR[PerformanceScore])

Payroll Growth % =
DIVIDE(
    [Current Year Payroll] -
    [Previous Year Payroll],
    [Previous Year Payroll]
)
```

---

## Tools and Technologies

* Power BI Desktop
* DAX
* Power Query
* Microsoft Excel
* Data Modeling
* Star Schema Design
* Data Warehousing Concepts
* Data Visualization

---

## Key Insights Generated

* Workforce distribution across departments and locations
* Salary and compensation trends
* Employee performance analysis
* Training effectiveness measurement
* Payroll growth monitoring
* Identification of top-performing employees

---

## Skills Demonstrated

### Data Analytics

* Data Cleaning
* Data Transformation
* Data Modeling

### Business Intelligence

* Dashboard Design
* KPI Development
* Executive Reporting
* Data Storytelling

### Power BI

* DAX Measures
* Data Relationships
* Star Schema Modeling
* Time Intelligence Functions

### Data Warehousing

* Fact and Dimension Modeling
* Surrogate Key Design
* Analytical Data Structures

---

## Author

### Altamash Nizamuddin

Data Analyst passionate about transforming complex datasets into actionable business insights through analytics, visualization, and storytelling.

### Connect With Me

GitHub: github.com/altamash-analyst

---

## Project Highlights

* Star Schema Data Model
* 5,000+ HR Records
* Advanced DAX Measures
* Executive-Level KPI Dashboard
* Interactive Power BI Reporting
* Business-Oriented Analytics Solution
* Portfolio-Ready Data Analytics Project
