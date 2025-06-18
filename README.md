# Deloitte-Australia---Data-Analytics-Job-Simulation
Deloitte Australia Data Analytics Job Simulation on Forage - June 2025

1. 	I completed a Deloitte job simulation involving data analysis and forensic technology 
2. 	I created a data dashboard using Tableau 
3. 	I used Excel to classify data and draw business conclusions

i earned the certification after completing the internship program with Deloitte Australia

![Deloitte Certificate](https://github.com/user-attachments/assets/361cf8d7-e081-4d1a-9d7d-1abbc0e947b2)

## Introduction
Using a data modification algorithm, the tech team at Daikibo has converted all telemetry data collected from its 4 factories
1. Daikibo Factory Meiyo (Tokyo, Japan)
2. Daikibo Factory Seiko (Osaka, Japan)
3. Daikibo Berlin (Berlin, Germany)
4.  Daikibo Shenzhen (Shenzhen, China)
   
Each location has 9 types of machines, sending a message every 10 mins. Daikibo has been collecting this data for one month (May 2021)
and they've shared this data in the form of a single json file.

## Objectives/Problems
1. In which location did machines break the most?
2. What are the machines that broke most often in that location?

## Task One
1.	Create a Dashboard using Tableau and set the first chart to be used as a filter.
2.	Select the factory with the most down time.

## Processes
a. Data Understanding

b. Data Analysis

c. Uncover Insight

## Data Understanding
A datasets was given that was stored in JSON file and the Dataset is 3 in 1 dataset. 3 different datasets that have been merged to become 1 dataset.

 ## Data Analysis
 After loading the data into Tableau by choosing JSON file, i selected the schema levels that are necessary for the analysis in the worksheet.
 Then the Analysis begin properly.
 1. To determine which location did machine breaks the most, create a calculated measure field called "Unhealthy" with a value of 10 for every unhealthy status (representing 10 mins of potential down time since the previous message). The code to type in order to create the calculated measure field is an "IF statement that goes thus (IF [Status] = "Unhealthy" THEN 10 ELSE 0 END)".

Then a bar chart was plotted called “Down Time per Factory” where a column  name "Factory" was plotted against the Sum(Unhealthy) which is the new column created. The bar chart can be seen below
![Downtime per factory](https://github.com/user-attachments/assets/1ffe33f2-cf40-4ab7-ac90-e128b9030350)


2. To determine the machines that broke most often in that location, plot another bar chart of device type on column against sum(unhealthy) on row on another sheet. Here is the chart below.


![Downtime per machine](https://github.com/user-attachments/assets/9d00f56c-b8f0-4510-bc19-ae2a4012a362)

## Uncover Insight
The 2 bar chart is merged together to make a dashboard and by building the dashboard we can answer our questions. when the dashboard is built, The first chart which is Downtime per factory was used as filter to  be able to answer the question. below is the dashboard

![Dashboard](https://github.com/user-attachments/assets/0ade7057-dd53-4546-b29c-caab92aca327)

From the dashboard we can deduce the following:
1. The location where the machine breaks most is Daikibo Factory Seiko (Osaka, Japan)
2. The Machine that broke most often in that location is Laser Welder

## Task Two

Forensic Technology
The company wants to know how they are doing about their employee compensation particularly about gender equality.
They gave a data on employee compensation and generated an Excel file (Equality Table.xlsx, available in the Resources) containing 3 columns:
1.	Factory
2.	Job Role
3.	Equality Score (integer; ranging between -100 and +100; 0 is ideal)

Here is your task:
•	Create a 4th column (Equality class), classifying the equality score into 3 types:

o	Fair (+-10)

o	Unfair (<-10 AND >10)

o	Highly Discriminative (<-20 AND >20)

Examples:

•	10 → Fair

•	-9 → Unfair

•	-30 → Highly Discriminative

## Solution
I created another column named Equality Class where i used the IF statement to classify the equality score based on the instructions given.

The equation goes thus: =IF(ABS(C2)<=10, "Fair", IF(ABS(C2)<=20, "Unfair", "Highly Discriminative")).

Below is the excel file that contains the solution to the question.

[Task 5 Equality Table.xlsx](https://github.com/user-attachments/files/20798503/Task.5.Equality.Table.xlsx)

