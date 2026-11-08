## 🌿BELLABEAT-CASESTUDY 

**Google Data Analytics Professional Certificate: Capstone Project**

**Author:** Beatrice Benson

**Tools:** Google BigQuery, SQL, Microsoft Excel, Power Query and GitHub

---

This Analysis follows the six step analysis; **Ask**, **Prepare**, **Process**, **Analyze**, **Share**, **Act**.



❓ **1. Ask**

🏢 **Business Scenario**

Bellabeat is a health-focused technology company that develops smart wellness products designed to help individuals monitor and improve aspects of their health and daily activities.

As the company seeks to expand its market presence, its leadership team wants to understand how consumers use smart fitness devices. These insights could help Bellabeat improve its marketing strategies, strengthen customer engagement and identify opportunities for product positioning.

The company has therefore tasked its marketing analytics team with examining existing smart-device usage data to identify behavioural trends and develop actionable business recommendations.


🎯 **Business Task**

Analyze smart-device usage data from Fitbit users to identify patterns in **physical activity**, **daily routines** and **sleep behaviour** and provide data-driven marketing recommendations for Bellabeat.




❔ Key Business Questions

1. What are some trends in smart device usage?
   
2. How could these trends apply to Bellabeat customers?
 
3. How could these trends help influence Bellabeat marketing strategy?  






👥 Stakeholders

Bellabeat executive leadership.

Bellabeat marketing team.

Product development team.

Customer engagement and digital wellness teams.











Analyzing Fitbit smart device usage data (activity, sleep, and calories) to uncover consumer trends and provide data-driven marketing recommendations for Bellabeat.



## About the Dataset

This project uses publicly available data collected from 30 Fitbit users via an Amazon Mechanical Turk survey between March 12 and May 12, 2016. The dataset was made available by Mobius On Kaggle for educational and non-commercial analysis.

- Source: [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit) on Kaggle.

- Participants: 30 Fitbit users (as reported by source; up to 35 IDs were found during processing).

- Date Range: March 12 - May 12, 2016

- Data collected: Personal tracker data including physical activity, heartrate and sleep monitoring.

- Granularity: Second, minute, hourly, and daily-level data across 29 CSV files.

- License: [CCO: Public Domain](https://www.kaggle.com/arashnic) through Mobius.
  


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

  



  


  


