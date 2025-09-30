## BrightTV Viewership Case Study Project
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

* Merged Viewership and UserProfile on UserID.

* Parsed timestamps into multiple granularities:

- RECORD_TS → full timestamp

- RECORD_DATE → date only

- RECORD_TIME → time only

- DAY_OF_WEEK → day name

* Created session metrics:

- TOTAL_SESSIONS (count of sessions)

- TOTAL_DURATION_MIN (sum of minutes)

- AVG_DURATION_MIN (average session duration)

* Defined duration buckets: Very Short, Short, Medium, Long, Very Long.

* Defined age buckets: Kids, Teens, Youth, Adults, Senior Citizen.

* Retained demographics: Gender, Race, Province.

* Aggregated data by: UserID, Channel, Date, Time, Duration Bucket, Demographics.

**Step 4: Processed Data Export**

* Downloaded processed dataset from Snowflake.

* Saved as CSV for visualization in Google Looker Studio.

**Step 5: Dashboards Creation (Google Looker Studio)**

* User & Usage Trends – Sessions and duration over time.

* Demographics & Consumption Patterns – Age, gender, race analysis.

* Peak Hours / Low-Consumption Days – Time-based heatmaps and tables.

* Channel & Geographic Insights – Top channels and provincial engagement.

* Filters included: Date, Channel, Province, Age, Gender, Race, Duration Bucket.
Visuals used: Line charts, bar charts, stacked bars, heatmaps, tables, maps, scatter plots.

**Step 6: Presentation Report (Canva)**

Slides summarized:

Data preparation and cleaning steps.

Transformation process in Snowflake (SQL query overview).

Key insights from dashboards.

Recommendations for content and growth strategies.

Visual aids:

Charts from Looker dashboards.

Infographics for metrics and demographics.

Maps for geographic insights.

Color-coded duration and age buckets.

Step 7: Optional Enhancements

Annotated slides with key findings.

Highlighted low-consumption days and peak usage times.

Added summary KPIs:

Total users

Average session duration

Most popular channels

📑 Repository Note

The raw data, processed data, SQL codes, and the final presentation report will be uploaded in this repository’s files for reference.
