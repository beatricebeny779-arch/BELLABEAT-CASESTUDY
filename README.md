## 🌿BELLABEAT-CASESTUDY 

**Google Data Analytics Professional Certificate: Capstone Project**

**Author:** Beatrice Benson

**Tools:** Google BigQuery, SQL, Microsoft Excel, Power Query and GitHub

---

This Analysis follows the six step analysis; **Ask**, **Prepare**, **Process**, **Analyze**, **Share**, **Act**.


❓**1. Ask**

🏢 **Business Scenario**

Bellabeat is a health-focused technology company that develops smart wellness products designed to help individuals monitor and improve aspects of their health and daily activities.

As the company seeks to expand its market presence, its leadership team wants to understand how consumers use smart fitness devices. These insights could help Bellabeat improve its marketing strategies, strengthen customer engagement and identify opportunities for product positioning.

The company has therefore tasked its marketing analytics team with examining existing smart-device usage data to identify behavioural trends and develop actionable business recommendations.


🎯 **Business Task**

Analyze smart-device usage data from Fitbit users to identify patterns in **physical activity**, **daily routinesG** and **sleep behaviour** and provide data-driven marketing recommendations for Bellabeat.




❔ **Key Business Questions**

1. What are some trends in smart device usage?
   
2. How could these trends apply to Bellabeat customers?
 
3. How could these trends help influence Bellabeat marketing strategy?  



👥 **Stakeholders**


**Primary Stakeholders:** Bellabeat Executive team, Product Development team.

**Secondary Stakeholder:** Bellabeat market analytics team, Customer Engagement and digital wellness teams.


**2. Prepare**

### About the Dataset


This project uses publicly available data collected from 30 Fitbit users via an Amazon Mechanical Turk survey between March 12 and May 12, 2016. The dataset was made available by Mobius On Kaggle for educational and non-commercial analysis.

- Source: [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) on Kaggle.

- License: [CCO: Public Domain](https://www.kaggle.com/arashnic) through Mobius.

- **Limitations:** The dataset is small (30 users), lacks demographic data (age, gender), and represents a short timeframe.

**ROCCC Assessment**
To ensure data quality and integrity, the raw Fitbit data was evaluated using the ROCCC checklist:
*   **Reliable:** Moderate. Data was self-reported via survey.
*   **Original:** Yes. It was collected directly from the devices.
*   **Comprehensive:** No. Missing key data like stress data (which Bellabeat tracks).
*   **Current:** No. The data is from 2016.
*   **Cited:** Yes. Publicly available on Kaggle.

**How is this data useful?**
While the data does not come from Bellabeat devices, it offers valuable insight into real-world behavior among smart-tech users.

**Decision to Proceed:**
Although the dataset did not fully meet all the ROCCC criteria, it was deemed suitable for exploratory analysis after thorough cleaning and validation, with the understanding that supplementary data should be considered for additional analysis.

















  
To ensure data quality and integrity, the raw Fitbit data was evaluated using the ROCCC checklist:

 **Reliable:** Moderate. Data was self-reported via survey.
 
 **Original:** Yes because it was collected directly from the devices.
 
 **Comprehensive:** No. Missing key data like stress data (which Bellabeat tracks).
 
 **Current:** No. The data is from 2016.
 
**Cited:** Yes. Publicly available on Kaggle.


To ensure data quality and integrity, the raw Fitbit data was evaluated using the ROCCC checklist. Although the dataset did not fully meet all the criteria, it was deemed suitable for exploratory analysis after thorough cleaning and validation, with the understanding that supplementary data should be considered for additional analysis.





How is this data useful?

While the data does not come from Bellabeat devices, it offers valuable insight into real-world behavior among smart-tech users.


## Data Processing

To ensure data quality and integrity, the raw Fitbit data was evaluated using the ROCCC checklist; Reliable, Original, Comprehensive, Current, and Cited. Although the dataset did not fully meet all the criteria, it was deemed suitable for exploratory analysis after thorough cleaning and validation, with understanding that supplementary data should be considered for additional analysis.

**Key cleaning steps**

- Standardized column names for consistency and clarity.

- Merged relevant .csv files by user ID and date.

- Removed duplicate observations.

- Converted data types for usability (e.g. datetime, factor, character, interger)

- Filtered out records with insufficient data (e.g IDs with very few observations)


**Key Validation Checks**

- Reviewed distributions of activity and sleep variables at minute and daily levels.

- Identified inconsistencies and gaps in user participation.

- Verified logical ranges for durations, timestamps, and categorical labels.



  **Business Task**

  Bellabeat wants to explore how smart device data from non-Bellabeat users can reveal trends in **physical activity**, **calories burn**, and **sleep** that may provide data-driven recommendations to better support the unique health and wellness journeys of our customers.

  



  


  

Step 2: Merge Activity and Sleep Data (JOIN)
Description: I used a LEFT JOIN to keep all the activity data intact, even on days when the user didn't record sleep.

sql
CREATE OR REPLACE TABLE `bellabeat_analysis.combined_activity_sleep` AS
SELECT ... (your code here)
Result: Successfully created a combined table with 457 rows.

Where do the actual numbers (Results) go?
They go in the Analyze phase.

Here is exactly how your Analyze section should look. Copy and paste this whole block (I have filled in the numbers from your earlier screenshot so you don't have to guess):



## 📊 4. Analyze

I used Google BigQuery to run summary statistics on the combined activity and sleep dataset.

### Overall Summary Statistics
*Description: I calculated the average steps, calories, sleep, and sedentary time across all users to understand general behavior.*

```sql
SELECT 
  COUNT(DISTINCT Id) AS unique_users,
  ROUND(AVG(TotalSteps), 0) AS avg_daily_steps,
  MAX(TotalSteps) AS max_daily_steps,
  ROUND(AVG(Calories), 0) AS avg_daily_calories,
  ROUND(AVG(TotalMinutesAsleep), 0) AS avg_sleep_minutes,
  ROUND(AVG(SedentaryMinutes), 0) AS avg_sedentary_minutes
FROM `bellabeat_analysis.combined_activity_sleep`;
Results:

unique_users	avg_daily_steps	max_daily_steps	avg_daily_calories	avg_sleep_minutes	avg_sedentary_minutes
35	6547	28497	2189	444	995
Insights:

High Sedentary Time: Users spend an average of 995 minutes (16.5 hours) per day sedentary, compared to only a small fraction of time being highly active.

Below Recommended Activity: The average daily steps (6,547) falls below the widely accepted 10,000-step goal, indicating room for fitness improvement.

Adequate Sleep: Users average 7.4 hours of sleep per night (444 minutes), which is within the recommended 7-9 hour range.

















### Overall Summary Statistics
*Description: I calculated the average steps, calories, sleep, and sedentary time across all users to understand general behavior.*

```sql
SELECT 
  COUNT(DISTINCT Id) AS unique_users,
  ROUND(AVG(TotalSteps), 0) AS avg_daily_steps,
  MAX(TotalSteps) AS max_daily_steps,
  ROUND(AVG(Calories), 0) AS avg_daily_calories,
  ROUND(AVG(TotalMinutesAsleep), 0) AS avg_sleep_minutes,
  ROUND(AVG(SedentaryMinutes), 0) AS avg_sedentary_minutes
FROM `bellabeat_analysis.combined_activity_sleep`;






