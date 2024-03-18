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

I downloaded the 12 months of trip data. I uploaded the files to GoogleCloud and created a bucket.

[Processing the data](https://github.com/drreid1/DReid/blob/8fa50b904e745338b0c50a7855f42629b6ce429e/Process%20the%20data.ipynb)  
1. Combine the data in a table called combined_trips.
2. Count the rows
3. Check for distinct rows
4. Check for missing information or nulls
5. Count the number of member types

## Clean
After combining the data into a table called combined_trips, I [cleaned the data](https://github.com/drreid1/DReid/blob/8fa50b904e745338b0c50a7855f42629b6ce429e/Process%20the%20data.ipynb) for analysis.
1. Select and delete rows containing nulls. Removed 1,388,170 rows.
2. Add column for ride_length.
3. Delete rows where ride_length is less than 1 minute or greater than 1440 minutes (day).
4. Add columns for month and day_of_week.
5. Count the number of remaining rows after cleaning.
   Result: 4331540

## Analyze
I used Tableau to create data vizualizations. I uploaded my combined and cleaned dataset into Tableau Desktop. 

I wanted to compare how the casual riders and member riders differ throughout the year.   
During 2023, there was a total of 4,331,540 riders.   
Memeber riders: 2,799,909   
Casual riders: 1,531,631

![Rider Percentages](https://github.com/drreid1/DReid/blob/e330a240a68b70617b54c8f661136c4e821bb139/Sheet%206.png)

August was the most popular month for Member riders (351,056) and July was the most popular for Casual riders (245,279). Summer months could be a peak time for riders of both types. 

![Riders by Month](https://github.com/drreid1/DReid/blob/565c550c4ec1235a253769e8952c956f2ba4ffc4/Sheet%201.png)

Member riders tended to use Cyclisitc during the week, while Casual riders tended to use them on the weekends.

![Riders by Day of the Week](https://github.com/drreid1/DReid/blob/71af82182424627fa765b30d135f41618def6fac/Sheet%202.png)

Members' average ride length was around half of the Casual riders' average ride length.
Casual riders rode for longer on the weekends. Member riders had more consistent ride length throughout the whole week.

![Average ride length](https://github.com/drreid1/DReid/blob/cd1ce9d154d9a68a6b81781da457af4a6f883dc6/Sheet%203.png)

The following graphic shows the most popular start stations for Member and Casual riders.

![Most Popular start stations](https://github.com/drreid1/DReid/blob/61bbae38309a88a2d3d7a6f9988138c312b4337e/Dashboard%203.png)
