# Cyclistic-bike-share-analysis-
This is  Google Data Analysis Professional Certificate case-study project which covers data about January 2021 to December 2021. Tools use in this project are Power Query ,Power BI and power point .
## About the Project
The bike sharing company wants to analyze their user data to find the main differences in behaviour between their two types of users, the “casual” who pays for each ride and the annual member who pays a yearly subscription to the service.

## Phase 1:ASK
#### Key Objectives
#### Business Task
How casual riders and annual members use Cyclistic bikes differently and using these insights how we  design a new marketing strategy to convert casual riders into annual members.
#### Key Stakeholders
The main stakeholders here are the director of marketing and my manager Lily Moreno, the rest of the marketing analytics team, and the Cyclistic executive team.

## Phase 2:Prepare
#### Determine the credibility of the data:
This is case study about Cyclistic Bike-share company.This datset include data between 2020-04 to 2023-04 (three years).
* Here is the Link of Dataset which is use in this project https://divvy-tripdata.s3.amazonaws.com/index.html
#### Datsets Use in this Project
The main Focus of the project is between January 2021 to December 2021 time perid to analysis that how Casual and Member riders use Cyclistic bike differently. Data seems to be in good condition and its first hand data collected by the company itself with lots of entries and with lots of useful data.

## Phase 3:Process
We use Power Query for Data Cleaning and transformation process 
* Firstly upload the 12 month data from **folder** into Power BI then **combine and transform** to clean the data.
* In the  **Query Editor** window
  * Remove unwanted columns that are not needed: Source Name, start_station-id, end_station_id,start_lat, start_lng, end_lat, end_lng
  * Create Custom columns:
    * time_duration = ([ended_at]-[started_at])
    * time_duration 1 = Number.Abs([time_duration])  (to get absolute numbers)
    * month_number = Date.Month([started_at])
    * day_number = Date.DayOfWeek([started_at],1)    (1 to start week by monday)
    * number_of_riders = transform tab - count - from 1
  month_number and day_number columns  are helpful for sort of months and day of weeks in arragnment.
  * Transform columns: 
    * Duplicate **started_at** to get
      * started_date = change type into Date
      * started_hour = transform into hour
    * Duplicate **started_date** to get
      * started_month = transform to month to Name of Month
      * started_day =  transform to Day to Name of Day
 * Remove Null 
   * Generally when we find null we can ask back to company form complete data but in this case we don't have direct connect to company so we remove null in by filtering it **member_casual** column so we 

## Phase 4 & 5: Analyse & Share

  
