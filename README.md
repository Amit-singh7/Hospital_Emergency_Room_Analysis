🏥 Hospital Emergency Room Dashboard – Data Analyst Project
📌 Project Overview

This project analyzes Hospital Emergency Room (ER) patient data to identify key performance indicators such as patient wait times, admission rates, patient demographics, and department referrals.

The project demonstrates an end-to-end Data Analyst workflow including:
Data Cleaning using Python (Pandas)
Exploratory Data Analysis using SQL
Data Preparation using Excel
Dashboard Development using Power BI
The goal of this project is to help hospitals improve operational efficiency, patient satisfaction, and emergency room performance.

📊 Dashboard Preview
🏠 Main Dashboard
Includes ER performance KPIs and patient demographics.

Key Metrics:
Total Patients: 9,216
Average Wait Time: 35.3 Minutes
Patient Satisfaction Score: 4.99
Patients Referred: 3,816

Visuals Included:
Patient Admission Status
Patients by Gender
Patients by Age Group
Department Referrals
Patient Race Distribution

📈 Consolidated View
Provides time-based analysis and operational insights.
Visuals Included:
% Patients Seen Within 30 Minutes
Patients by Day
Patients by Hour Heatmap

📋 Patient Details View
Detailed patient-level dataset used for analysis.
Columns Include:
Patient ID
Patient Name
Gender
Age
Admission Date
Race
Wait Time
Department Referral
Admission Status

🧰 Tools & Technologies
Tool	Purpose
Python (Pandas)	Data Cleaning
SQL	Exploratory Data Analysis
Excel	Data Preparation
Power BI	Dashboard Creation

📂 Project Workflow
Step 1 — Data Collection
The dataset contains emergency room patient information including:
Patient demographics
Admission status
Wait time
Department referrals
Patient satisfaction
Visit date and time

Step 2 — Data Cleaning (Python – Pandas)
Data cleaning was performed using Python Pandas.
Tasks Performed:
Removed duplicate records
Handled missing values
Standardized column names
Converted date columns to datetime format
Cleaned inconsistent text values
Corrected data types

Example Code:
import pandas as pd
df = pd.read_csv("hospital_er_data.csv")

# Remove duplicates
df.drop_duplicates(inplace=True)

# Handle missing values
df.fillna("Unknown", inplace=True)

# Convert date column
df['Patient Admit Date'] = pd.to_datetime(df['Patient Admit Date'])

# Standardize text
df['Patient Gender'] = df['Patient Gender'].str.title()

Step 3 — Exploratory Data Analysis (SQL)
SQL was used to analyze patterns and generate KPIs.
Example Queries

Total Patients
SELECT COUNT(*) AS Total_Patients
FROM ER_Data;

Average Wait Time
SELECT AVG(Patient_Waittime) AS Avg_Wait_Time
FROM ER_Data;

Admission Rate
SELECT Admission_Status,
COUNT(*) AS Patients
FROM ER_Data
GROUP BY Admission_Status;

Patients by Department
SELECT Department_Referral,
COUNT(*) AS Total
FROM ER_Data
GROUP BY Department_Referral
ORDER BY Total DESC;

Step 4 — Data Preparation (Excel)
Excel was used for final dataset preparation before Power BI.
Tasks Performed:
Verified data accuracy
Created calculated columns
Formatted date fields
Checked outliers
Created age groups

Example Age Group Formula:
=IF(Age<=10,"0-10",
IF(Age<=20,"11-20",
IF(Age<=30,"21-30",
IF(Age<=40,"31-40",
IF(Age<=50,"41-50",
IF(Age<=60,"51-60",
IF(Age<=70,"61-70","71-80")))))))

Step 5 — Dashboard Development (Power BI)
Power BI was used to create an interactive dashboard.

Features:
✔ Interactive Filters
Year Filter
Month Filter

✔ Navigation Buttons
Home Page
Consolidated View
Patient Details

✔ KPIs
Number of Patients
Average Wait Time
Patient Satisfaction
Referred Patients

✔ Charts
Bar Charts
Donut Charts
Heatmaps
Tables
KPI Cards

📊 Key Insights
Patient Flow
Total Patients: 9K+

Patient visits peak on weekends
Highest traffic between 00–02 hours

Wait Time
Average Wait Time: 35 Minutes
Around 59% patients seen within 30 minutes

Admissions
50% Admitted
50% Not Admitted

Demographics
Male: 51%
Female: 49%

Most common age group:
21–40 years

Department Referrals
Top departments:
None (No referral)
General Practice
Orthopedics

📁 Project Structure
Hospital-ER-Dashboard
│
├── Dataset
│   └── hospital_er_data.csv
│
├── Python
│   └── data_cleaning.ipynb
│
├── SQL
│   └── er_queries.sql
│
├── Excel
│   └── cleaned_dataset.xlsx
│
├── PowerBI
│   └── hospital_er_dashboard.pbix
│
└── README.md
🚀 How to Run This Project
1️⃣ Python Cleaning
pip install pandas
Run:
data_cleaning.ipynb

2️⃣ SQL Analysis
Import dataset into:
SQL Server / MySQL / PostgreSQL
Run:
er_queries.sql

3️⃣ Power BI Dashboard
Open:
hospital_er_dashboard.pbix

🎯 Project Skills Demonstrated
✔ Data Cleaning
✔ Data Transformation
✔ Exploratory Data Analysis
✔ SQL Queries
✔ Data Visualization
✔ Dashboard Design
✔ Business Insights

📌 Business Value
This dashboard helps hospitals:
Reduce patient waiting time
Improve ER efficiency
Monitor patient satisfaction
Optimize staffing
Track patient trends

👨‍💻 Author
Amit
Data Analyst

Skills:
Python
SQL

Excel

Power BI
