# A case study on cyclic bike sharing analysis

## Introduction

In this case study, I will demonstrate the entire process of data analysis using Google Data Analytics principles, which include the following: 
**Ask, Prepare, Process,Analyze, Share,** and **Act**

## Scenario

The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, the team wants to understand how casual riders and annual members use Cyclistic bikes differently. 
From these insights, my insight will help design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve my recommendations, so it must be backed up with compelling data insights and professional data visualizations.

## Setting

Region: Chicago, USA  
Period: May 2023 - May 2024  
Seasons Covered: Fall, Winter, Spring & Summer

## Tools

- Microsoft Excel
- R

## Characters and teams
● **Cyclistic:** A bike-share program that features more than 5,800 bicycles and 600
docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand
tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities
and riders who can’t use a standard two-wheeled bike. The majority of riders opt for
traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more
likely to ride for leisure, but about 30% use the bikes to commute to work each day.

● **Lily Moreno:** The director of marketing and the manager. Moreno is responsible for
the development of campaigns and initiatives to promote the bike-share program.
These may include email, social media, and other channels.

● **Cyclistic marketing analytics team:** A team of data analysts who are responsible for
collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy.

● **Cyclistic executive team:** Whether to approve the suggested marketing program will be up to the executive team, 
who are known for their meticulous attention to detail.

## About the company

Cyclistic is a fictional company that launched a successful bike-sharing in 2016. Since then, the program has grown into a fleet of 5,824 bicycles that are geo-tracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. 

Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Although the pricing flexibility helps Cyclistic attract more customers, Moreno believes that maximizing the number of annual members will be key to future growth. Rather than creating a marketing campaign that targets all-new customers, Moreno believes there is a solid opportunity to convert casual riders into members. She notes that casual riders
are already aware of the Cyclistic program and have chosen Cyclistic for their mobility needs.

Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

# Ask

The data analysis cycle begins with the ask phase, which entails establishing the project's scope, the problem to be solved, and the expectations of stakeholders by posing **SMART** (Specific, Measurable, Action-oriented, Relevant, Time-bound) questions.

The challenge to be addressed for this project is creating marketing plans that would turn casual riders into yearly members. My analysis will provide the marketing team with insights to help them develop a fresh and effective plan to turn casual riders into yearly members. It will also help persuade the Cyclistic management team to embrace this new approach.  

Determining the differences in Cyclistic usage between annual members and casual riders will be the key business task. Lily Moreno, the marketing director, and the Cyclistic executive team are the project's stakeholders, and I will be presenting the findings to them.

# Prepare

This includes locating the data source that will be used for the analysis, making sure that the data source is trustworthy, unique, thorough, up-to-date, and referenced, modeling the data, making sure that the data is free from bias in any way during collection, and adhering to all data ethics guidelines when working with the data.

This project will leverage historical cyclic data from the past 12 months that is kept in an [online repository](https://divvy-tripdata.s3.amazonaws.com/index.html) (provided by Motivate International Inc. under this license). Twelve CSV files, each with ride details for each month from May 2023 to May 2024, contain the data.

Since Cyclistic gathered and kept the data, its first-party status guarantees its authenticity and dependability. A cursory examination of the data reveals that it contains comprehensive information that provides key metrics to compare rides by annual members and casual riders and will be sufficient to complete the key business task. Only historical data from the previous 12 months is used to ensure that the data reflects the current trend in cyclic rides.

# Process

This includes all the procedures used to clean the data, ensure that it is correct, complete, consistent, and reliable before analysis, align the data with the business goal, and perform data verification.

Each CSV file was imported into a separate Excel worksheet in order to process the data for this project. Data processing was divided into four main tasks:

**Normalization of dataset**: this involved checking the data completeness, making sure the datasets included accurate information, and making sure that the information was consistent across the datasets used.

**Cleaning the dataset**: this involved checking for any error, typos, duplicate entries, blank cells, and ensuring consistent data formats across each column.

**Aligning the dataset with the business objective**: Aligning the dataset with the business task involves manipulating the data to provide the best answers for the task at hand. To achieve this, four new variables were created:

1. **ride_length**: This variable is calculated by subtracting the start time of each ride from its end time.
2. **day_of_week**: This variable indicates the day of the week on which each ride started.
3. **day_of_week_desc**: This variable maps each day of the week to a corresponding number, where 1 represents Sunday and 7 represents Saturday.
4. **route**: This variable is formed by concatenating the start station name with the end station name, allowing us to identify the most frequent route taken by users.
5. **time_of_day**: This variable helps identify which time of day experiences the highest number of rides by users.

These new variables will enhance my analysis and provide insights into user behavior.

# Analyze

I started my analysis by exploring each dataset, utilizing Excel functions and pivot tables to identify trends for each month. I documented the average and maximum ride lengths, and I compared the frequency and duration of rides between casual riders and annual members. Additionally, I examined their preferred starting and ending locations, as well as their preferred bike types.

# May 2023

1. Out of a total of 604,827 rides, 602 rides lasted more than 24 hours.  
2. The average ride length for this month is 19 minutes.  
3. The longest ride lasted for 23 hours and 58 minutes, excluding rides that lasted more than 24 hours.  
4. Tuesday has the highest number of rides for all riders, with a total of 101,062 (including both casual and member riders).  
5. Among casual riders, Sunday has the most rides, followed by Saturday and Tuesday, with 42,124 rides on Sunday, 40,758 on Saturday, and 33,382 on Tuesday. For member riders, Tuesday has the most rides, followed by Wednesday and Thursday, with 67,680 rides on Wednesday, 67,517 on Tuesday, and 55,686 on Thursday.  
6. Out of the 604,827 rides, casual riders accounted for 234,181 rides, while member riders accounted for 370,646 rides.  
7. The most frequently taken route by riders is from Streeter Dr & Grand Ave to Streeter Dr & Grand Ave, with 1,159 rides taken by casual riders and 179 by member riders.  
8. Afternoon is the time with the most rides taken by casual riders, totaling 89,445 rides, while member riders took 120,472 rides in the afternoon.  
9. Both casual and member riders used electric bikes, with casual riders accounting for 46,785 rides and member riders for 62,891 rides.





