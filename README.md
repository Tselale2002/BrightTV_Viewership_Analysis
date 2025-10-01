## BrightTV Viewership Analysis Case Study Project
**📌 Objective**

The objective of this case study is to support BrightTV’s CEO and the Customer Value Management (CVM) team in achieving their goal of growing the company’s subscription base during the current financial year.

**🎯 Purpose**

The purpose of the analysis is to:

* Provide insights on user and usage trends of BrightTV.

* Identify factors influencing consumption.

* Recommend content strategies to increase consumption on low-usage days.

* Suggest initiatives to grow BrightTV’s user base.

**🛠️ Tools & Technologies**

* Excel – Initial dataset review and sheet separation.

* Notepad – Replaced semicolons ; with commas , for CSV compatibility.

* Snowflake – Data loading, cleaning, and transformation.

* Excel (Pivot Table) - To create visualisation

* Google Looker Studio – Dashboard creation and visualization.

* Canva – Final presentation design.

**📂 Project Mind Map**
**Step 1: Data Acquisition**

* Received readily available raw data from BrightLearn.

* Dataset contained two sheets:

  - UserProfile

  - Viewership

**Step 2: Data Preparation**

* Separated sheets into individual datasets.

* Saved as CSV files:

  - BrightTV-Dataset_UserProfile.csv

  - BrightTV-Dataset_Viewership.csv

* Cleaned UserProfile data:

  - Removed extra spaces.

  - Replaced semicolons ; with commas , for compatibility.

* Ensured datasets were ready for Snowflake loading.

**Step 3: Data Loading & Transformation (Snowflake)**

* Loaded CSV datasets into Snowflake.

* Merged Viewership and UserProfile on UserID using Left Join on.

* Converted timestamps into different levels of detail (date, time, day, month).:

  - RECORD_TS → full timestamp

  - RECORD_DATE → date only

  - RECORD_TIME → time only

  - DAY_OF_WEEK → day name

  - RECORD_MONTH → month number

* Created session metrics:

  - TOTAL_SESSIONS (count of sessions)
    
  - TOTAL_DURATION_MIN (sum of minutes)

  - AVG_DURATION_MIN (average session duration)

* Defined time of the day segmentation: Morning, Noon, Afternoon, Evening, Midnight.

* Defined duration buckets: Very Short, Short, Medium, Long, Very Long.

* Defined age buckets: Kids, Teens, Youth, Adults, Senior Citizen.

* Retained demographics: Gender, Race, Province.

* Aggregated data by: UserID, Channel, Date, Time, Duration Bucket, Demographics.

**Step 4: Processed Data Export**

* Downloaded processed dataset from Snowflake.

* Saved as CSV for visualization in Google Looker Studio.

* Saved as CSV, open it on Notedpad: replaced none with Unknown and write the content for Race, and Gender starting with capital letters (male → Male).

* Open file on Excel change the month number to month name, i.e. 1 → Jan and start to create graphs for my analysis.

* Saved all the graphs as pictures to be uploaded on CANVA for presentation.
  
**Step 5: Presentation Report (Canva)**

* Created presentation report on CANVA.

* Uploaded all the saved graphs on CANVA.

* Then compiled the report accordingly.

**Step 6: Visualisation and Dashboards Creation (Google Looker Studio)**

* User & Usage Trends – Sessions and duration over time.

* Demographics & Consumption Patterns – Age, gender, race analysis.

* Peak Hours / Low-Consumption Days – Time-based heatmaps and tables.

* Channel & Geographic Insights – Top channels and provincial engagement.

**📑 Conclusion**

This analysis converted BrightTV’s raw viewership data into practical insights for the CEO and CVM team.

Key outcomes include:

* Sports are the strongest driver of viewership, led by Supersport Live Events and the ICC Cricket World Cup.

* Music and entertainment channels (Channel O, Trace TV) show consistent engagement, highlighting diverse audience interests.

* Viewing patterns vary by time of day and week, with evenings and weekends recording the highest consumption.

* Recommendations focused on leveraging sports content, cross-promoting entertainment, and targeted marketing to grow and retain BrightTV’s subscriber base.

The repository contains: 

* Raw datasets, processed dataset, and SQL transformation scripts.
  
* Visualization exports (graphs, dashboards).
  
* Final Canva presentation report.
