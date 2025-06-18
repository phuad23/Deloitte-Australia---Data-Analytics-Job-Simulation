# Deloitte-Australia---Data-Analytics-Job-Simulation
Deloitte Australia Data Analytics Job Simulation on Forage - June 2025

1. 	I completed a Deloitte job simulation involving data analysis and forensic technology 
2. 	I created a data dashboard using Tableau 
3. 	I used Excel to classify data and draw business conclusions

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


2. To determine the machines that broke most often in that location, plot another bar chart of device type on column against sum(unhealthy) on row on another sheet. 
  
