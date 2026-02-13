# Hospital-Pharmacy-Performance-PowerBI-Dashboard
This project showcases a comprehensive PowerBI dashboard analyzing Hospital-Pharmacy operations, overall performance and drug consumption patterns. The objective of this analysis is to transform raw data into meaningful insights that support data driven decision making from the Hospital-Pharmacy Performance data.

The analysis involved data cleaning in Power Query in PowerBI, Data Modelling in the Model View, then analyzing the data and incorporating DAX, visualizing the data using charts and cards and eventually buiding an interactive dashboard with KPIs, Slicers and Charts. 

# Tools and Techniques used
PowerBI Desktop

Power Query

DAX operations

Charts

Slicers

# Data Cleaning
The dataset was first imported into PowerBI and cleaned using Power Query. The cleaning process included;

Removing Duplicates

Correcting the Data Types as required into Dates, Numeric Values, Decimals, Texts

Ensuring no Null values affected Key metrics

This data cleaning ensured data accuracy and reliability before analysis.

# Data Analysis
Key measures and new columns were created in support of the Data analysis using DAX.

A new measure was created for Total_Pharmacy_Revenue, Total_Hospital_visits, Average_Length_of_Stay(days), Average_Drug_UnitPrice using the formulas;


_Total_Pharmacy_Revenue = SUM(Pharmacy_Transactions[Total_Cost])_

_Total_Hospital_Visits = COUNT(Visits[Patient_ID])_

_Average_Length_of_stay (Days) = AVERAGE(Visits[Length_of_Stay_Days])_

_Average_Drug_Unit_Price = AVERAGE(Pharmacy_Transactions[Unit_Price])_

A new Column 'Age_groups' was also created inorder to group the ages for better analysis. It was created as shown below;

_Age_groups = IF(Patients[Age]<=20, "0 - 20", IF(Patients[Age]<=40, "21 - 40", IF(Patients[Age]<=60, "41 - 60",">60")))_


# Dashboard Highlights
KPI Cards displaying: Total Pharmacy Revenue, Total Hospital Visits, Average Length of Stay(Days), Average Drug UnitPrice

Slicers: For County, Diagnosis, Month

Disease trends over time (Line Chart)

Pharmacy cost breakdown by Drug Category(Column Chart)

Comparison between each County's Departments by Revenue(Clustered Bar Chart)


# Dashboard Preview
<img width="1189" height="680" alt="Dahboard_preview image" src="https://github.com/user-attachments/assets/aa1d963d-501b-4f88-bd57-720f87ba76b0" />

# Key Insights
The Pharmacy generated a Total Revenue of **275.41K** indicating high Drug purchase by Patients. Uasin Gishu County had Highest Pharmacy revenue per county contributing to slightly above 25% of the Total Revenue. 

There is an evident seasonal fluctuation in the Number of Diagnosis frequency, with a peak observed in March followed by a decline in the subsequent months suggesting possible seasonal disease patterns.

The inpatient and Emergency Departments contribute significantly more to Pharmacy Revenue compared to the Outpatient department. This shows that higher drug consumption is associated with inpatient and emergency services.

The number of Total Visits to the hospital was **300** during the period with Uasin Gishu County and Kiambu  County contributing to the highest number of visits.

The Average length of Stay was **1.41 days** indicating that most cases are treated quickly, potentially reflecting effective treatment protocols or high outpatient patients.

Patients aged above 60 years old purchased the highest number of drugs, contributing to 37.43% of the total number of drugs sold. Followed by patients aged between 21- 40 years at 23.43%

Diabetes was the most common Diagnosis in Kiambu and Mombasa County. The Flu was most common in Uasin Gishu and Nakuru County. Hypertension was most common in Kisumu County. Pneumonia was the most common in Nairobi county. Typhoid was most common in Kiambu as well as Uasin Gishu County.








          
