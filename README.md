# Cyclistic-bike-share-analysis-
This is  Google Data Analysis Professional Certificate case-study project which covers data about January 2021 to December 2021. Tools use in this project are Power Query ,Power BI and power point .
## About the Dataset
This is case study about Cyclistic Bike-share company.The main Focus of the project is between January 2021 to December 2021 time perid to analysis that how Casual and Member riders use Cyclistic bike differently. 
Here is the Link of Dataset which is use in this project https://divvy-tripdata.s3.amazonaws.com/index.html
## System Use in Cyclistic-bike-share-analysis-
* Power Query for data cleaning and data analysis by using DAX language
* Power BI for data visulization
* Power Point for data presentataion
## Data Cleaning & Transforming
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
  
