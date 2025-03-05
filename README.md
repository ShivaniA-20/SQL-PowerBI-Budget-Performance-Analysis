# SQL-PowerBI-Budget-Performance-Analysis

## 📌 Project Overview

This project aims to analyze department and project performance in relation to budget constraints. The goal is to identify underperforming or over-budget departments and projects, ensuring that departmental budgets set for two-year intervals can sufficiently cover expenses.

## 📊 Key Objectives

1. **Identify departments and projects at risk** of exceeding budgets or underperforming.
2. **Organize and structure data** from multiple sources, including employee info, salary data, department budgets, and project details.
3. **Develop an interactive Power BI dashboard** to provide insights into employee performance, salary distribution, and departmental project management.

## 🛠️ Tech Stack

 - **SQL (MySQL Workbench)** – Data cleaning, transformation, and modeling.
 - **Power BI** – Data visualization and dashboard creation.

## 📂 Data Sources

The following datasets were used to create the database:
 - **completed_projects.csv** – Details of completed projects.
 - **departments.csv** – Department information.
 - **employees.csv** – Employee data.
 - **project_assignments.csv** – Employee-project mapping.
 - **projects.csv** – General project details.
 - **upcoming_projects.csv** – Upcoming projects information.
 - **headshot.xlsx** – Employee profile pictures for Power BI.

## 🏗️ Data Processing & SQL Operations

1️⃣ **Database Creation & Data Loading**

- Created a new **MySQL database** and loaded the required files.
- Used **INNER JOIN** to combine *employees* and *departments* on *department_id*.
- Joined *project_assignments* and *employees* using *employee_id*.

2️⃣ **Project Status Classification**
- Used **UNION ALL** to merge *upcoming_projects* and *completed_projects*.
- Added a **status column** to differentiate between completed and upcoming projects.

3️⃣ **Combining Employee & Project Data**
- Created a **Common Table Expression (CTE)** to unify employee and project data for further analysis.

## 📊 Power BI Dashboard Development

1️⃣ **Data Import & Preparation**
- Connected **MySQL database** to Power BI.
- Imported *headshot.xlsx* and linked it to employee data using *employee_id*.
- Used **Power Query’s Group By feature** to calculate budget per department.
- Created a **custom column ‘Revenue’** to analyze department profitability.
- Created another column to calculate **budget for 2 years**.

2️⃣ **Data Visualizations**
1. 📊 **Donut Chart** – Displays Department Name and Project Cost.

2. 📈 **Clustered Bar Chart** – Shows Project Name and Budget.

3. 🎚️ **Slicer** – Dropdown filter for selecting **Employee ID**.

4. 📋 **Table** – Highlights **low-performing departments**.
    - Displays: Department Goals, Department Name, Project Cost, Salary Cost, 2-Year Budget, and Revenue.
  

## 📢 **Key Insights**

✔️ Identified departments at risk of exceeding budgets and projects with high costs.  
✔️ Revealed underperforming departments, e.g., **Human Resources** with low revenue generation.  
✔️ Enabled dynamic filtering for employee-specific insights using Power BI slicers.  
✔️ Highlighted budget shortfalls across multiple departments using custom measures.  
