# Cyclistic Case Study
## Google Data Analytics Course
## By: Dottie Reid

Note: Much of the background information is directly from the case study document provided. 

## Introduction
This is a capstone project for completion of the Google Data Analytics Course. In order to answer the business questions, I will follow the steps of the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

### Scenario
> You are a junior data analyst working on the marketing analyst team at Cyclistic, a fictional bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations. 

### Key Stakeholders 
* **Cyclistic:** Bike-sharing company   
* **Me:** Junior Data Analyst in the marketing analyst team   
* **Lily Moreno:** Director of Marketing   
* **Cyclistic marketing analytics team:** A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy   
* **Cyclistic executive team:** executive team will decide whether to approve the recommended marketing program   

## Ask
Three questions will guide the future marketing program: 
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships? 
3. How can Cyclistic use digital media to influence casual riders to become members?

Moreno has assigned you the first question to answer: **How do annual members and casual riders use Cyclistic bikes differently?**

**Business Task:**   
Use Cyclistic’s historical trip data to analyze and identify trends of members and casual riders

## Prepare
**Data Source**   
> Use Cyclistic’s historical trip data to analyze and identify trends. Download the previous 12 months of Cyclistic trip data [here](https://divvy-tripdata.s3.amazonaws.com/index.html).
> 
> (Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are appropriate and will enable you to answer the business questions. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement).
> 
> This is public data that you can use to explore how different customer types are using Cyclistic bikes. But note that data-privacy issues prohibit you from using riders’ personally identifiable information. This means that you won’t be able to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes. 

The data is organized by month. I used 12 CSV files from January 2023 to December 2023. The data is organized and stored in 12 comma-separated values (csv) files. The naming convention of the csv files is YYYYMM-divvy-tripdata.csv.   
Each file had 13 columns: ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng, member_casual.

## Process
I used BigQuery SQL for processing and cleaning the data, becuase Excel can only process 1,048,576 rows. The 12 data sets, once combined, contained a total of 5,719,877 rows.   
After, I used Tableau to create data vizualizations. 


My first three steps were to:
1. Download the previous 12 months of trip data.
2. Upload to GoogleCloud and create a bucket.
3. Combine the data in one table.







