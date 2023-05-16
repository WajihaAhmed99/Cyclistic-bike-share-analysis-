# Cyclistic-bike-share-analysis-
This is  Google Data Analysis Professional Certificate case-study project which covers data about January 2021 to December 2021. Tools use in this project are Power Query ,Power BI and power point .
## About the Project
The bike sharing company wants to analyze their user data to find the main differences in behaviour between their two types of users, the “casual” who pays for each ride and the annual member who pays a yearly subscription to the service.
#### According to Google ,their are six phases for analysis
* Ask
* Prepare
* Process
* Analyze
* Share
*  Act
so we are doing our analysis according to these six phases.

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
#### 1.Who use bikes mostly member or casual riders
* Member riders are 9.6% more than casual riders

![number of riders by member or casual](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/bfc18738-1ffd-4384-abff-28d77711b104)

#### 2.Which month is Busiest
* July and August is most busiest month
* Casual riders use mostly bikes in July and August
* Member riders use mostly bikes on August and September

![number of riders by month](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/76f5ee9d-0669-4581-9b12-bdbeb4d78c68)

#### 3.Busiest Day of week
* Saturday and Sunday are most busiest days of week
* Casual riders use bikes mostly on Saturday and Sunday
* Member riders use bikes mostly on Tuesday and Wednesday

![number of riders by weekdays](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/eedff863-ea66-4d9e-8593-87be7a937d97)

#### 4.Which Hour is busiest in a day for riders
* 6 PM and 7 PM are the most rush hours of day for both casual and member riders
* In morning 9 AM is  2nd most rush hour for member riders

![hours](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/24fdab23-7eb9-4b91-8d43-7a27829c27a7)

#### 5.Average time duration of riders
* Casual riders have more average time duration than member riders
* Average time duration of casual riders are 18 minutes
* Average time duration of member riders are 12 minutes

![time duration](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/1854b48d-d144-4ee8-8835-d38f22c89613)



#### 6.Widely use Ride-Type
* Classic-Bikes are more famous in member and casual riders

![ridable type](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/e347d3e7-25d1-4297-9e27-2254acf4e054)


#### 7.Widely use stations
* Wood St & Milwaukee Ave, Woodlawn Ave & 55th St, Wood St & Chicago Ave and Wood St Taylor St(Tamp) are among widely use stations for riders

![stations](https://github.com/WajihaAhmed99/Cyclistic-bike-share-analysis-/assets/132120179/46a97220-2bcf-43c9-a559-a9ff1d4581a4)


## Conclusion
* Member riders are more in population then casual riders but Average time per minute for bike use by casual riders is greater then member riders.
* Casual Riders use  mostly bikes then member riders in July, August and September while in all other months of year member riders use mostly bikes. Member riders use rides between  0.4M to 0.5M in all days of week ,casual riders use its mostly bike on weekend between 0.38M to 0.55M rides. Member riders use mostly bikes on 6PM and 9AM  casual riders use mostly bikes between12PM to 8PM.
* Besides all these facts we conclude that Member riders use bikes for daily routine or they might use it for 9 to 5 job while casual riders use it for enjoinment specially in  evenings ,weekends and in summer peak days. 

## Recommendations
**As we see in our analysis that casual riders use bikes on envenings,weekdays and summer month holidays for enjonynment it is diffcult to convert casual riders into member riders because they are using bikes for enjoynment but  we should introduce a yearly subscription of evening( 12PM to 8PM ), weekdays(friday,saturday,sunday) and summer holiday months(july,august,september) which will gives us a huge revenue and  casual rider average time of using bikes is also greater than member riders so this also great factor for revenue increase.**

## Thanks for Reading




