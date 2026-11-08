## 🌿BELLABEAT-CASESTUDY 
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

  



  


  


