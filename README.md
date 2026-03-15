# Exploratory-Data-Analysis-and-Visualization-of-NYC-Motor-Vehicle-Collisions-Using-Seaborn
🚦 NYC Motor Vehicle Collisions – Data Analysis & Visualization

Course: IE6600 – Computation and Visualization for Analytics
Project: Advanced Data Analysis and Visualization Using Seaborn
Dataset: NYC Motor Vehicle Collisions – Crashes
Source: NYC Open Data / Data.gov
Group: Group 4
Members:

Rutuja Dambir

Praniti Kale

Hiral Hitesh Rana

📌 Project Overview

This project presents a comprehensive Exploratory Data Analysis (EDA) and statistical investigation of the NYC Motor Vehicle Collisions – Crashes dataset using Python, Pandas, and Seaborn.

Motor vehicle collisions are a major public safety concern in New York City. By analyzing collision records, this project aims to identify:

Temporal patterns in crash occurrences

Geographic differences across boroughs

Injury and fatality distributions

Major contributing factors behind crashes

The findings provide insights that may support traffic safety policy, urban planning, and mobility management.

This project demonstrates practical skills in:

Data acquisition

Data cleaning and preprocessing

Statistical analysis

Advanced data visualization using Seaborn

According to the project report, the dataset contains hundreds of thousands of collision records spanning multiple years, with rich temporal, spatial, and safety-related attributes.

📊 Dataset Information

Dataset Name: Motor Vehicle Collisions – Crashes
Source: NYC Open Data / Data.gov
Resource ID: h9gi-nx95
Domain: Transportation / Public Safety
Update Frequency: Weekly

Key Data Attributes

The dataset includes:

Temporal features

crash_date

crash_time

Geographic features

borough

zip_code

latitude

longitude

Injury and fatality counts

number_of_persons_injured

number_of_persons_killed

pedestrian injuries

cyclist injuries

motorist injuries

Causal factors

contributing_factor_vehicle_1

contributing_factor_vehicle_2

Vehicle information

vehicle_type_code1

vehicle_type_code2

These attributes enable both distributional analysis and relational analysis using Seaborn visualizations.

⚙️ Data Processing Pipeline
1️⃣ Data Acquisition

The dataset was retrieved using the official NYC Open Data API endpoint.
If a local CSV was available, it was used for reproducibility; otherwise the API was queried.

2️⃣ Data Cleaning and Preparation

Several preprocessing steps were performed to ensure data quality:

Column Standardization

All column names were standardized to lowercase with underscores to ensure consistent referencing.

Duplicate Removal

Duplicate rows were removed using:

df.drop_duplicates()
Data Type Conversion

Several columns were converted to appropriate data types:

Date fields → datetime

Numeric variables → float or integer

Categorical variables → cleaned string values

Categorical Cleaning

Placeholder values such as:

'', 'nan', 'Unspecified'

were replaced with proper NaN values.

3️⃣ Feature Engineering

Several derived variables were created to support the analysis:

Feature	Description
crash_hour	Hour extracted from crash time
year	Year extracted from crash date
month	Month number
month_name	Full month name
day_of_week	Day name
is_weekend	Weekend indicator
total_injured	Persons injured per collision
total_killed	Persons killed per collision
total_casualties	Injured + killed
injury_flag	Indicates if injury occurred
fatality_flag	Indicates if fatality occurred
severity	Fatal / Injury / Property Damage

These derived attributes enabled temporal pattern analysis and severity analysis.

📈 Exploratory Data Analysis (EDA)

All visualizations were generated using the Seaborn library.

Collision Count by Borough

A horizontal count plot shows collision frequency across NYC boroughs.

Key observation:

Brooklyn and Queens show the highest collision volumes, likely due to population density and traffic exposure.

Collision Distribution by Hour

A histogram with KDE overlay reveals a bimodal daily pattern:

Morning commute peak → 7–9 AM

Evening commute peak → 4–6 PM

These peaks correspond to high commuter traffic periods.

Collision Count by Day of Week

Weekdays show higher collision volumes due to commuter activity.

However, weekends may show higher severity during late-night hours.

Collision Count by Month

Seasonal trends were observed:

Warmer months (May–October) show higher collision counts

Winter months have slightly fewer collisions but potentially higher severity due to weather conditions.

Injury Distribution

A boxplot was used to analyze the distribution of injuries per collision.

Findings:

Most collisions result in zero or one injury

The distribution is heavily right-skewed, with rare severe incidents.

Weekend vs Weekday Injury Distribution

A violin plot compares injury distributions across weekday and weekend collisions.

This visualization reveals differences in the density of injuries between the two groups.

Collision Severity Distribution

Collisions were categorized into three severity levels:

Property Damage Only

Injury

Fatal

Most collisions fall into property damage or injury categories, while fatal collisions represent a small minority.

Correlation Heatmap

A Pearson correlation heatmap highlights relationships among numeric variables.

Key insight:

Total casualties strongly correlate with individual injury categories, which is expected because they are additive measures.

Top Contributing Factors

The most frequent crash causes include:

Driver Inattention / Distraction

Failure to Yield Right-of-Way

Following Too Closely

These behavioral factors are consistent with national crash statistics.

📊 Statistical Analysis

Two statistical tests were applied.

Mann–Whitney U Test

Used to compare injury distributions between:

Weekday collisions

Weekend collisions

A non-parametric test was chosen because the injury distribution is highly skewed and non-normal.

Chi-Square Test

Used to evaluate the relationship between:

Borough

Collision severity

This determines whether severity distribution differs across boroughs.

🔎 Advanced Analysis

Additional analyses were conducted to gain deeper insights.

Average Casualties by Hour

Although collisions peak during commute hours, late-night collisions often have higher average severity, potentially due to:

Impaired driving

Higher speeds

Lower traffic enforcement

Fatal Collision Rate by Borough

Fatality rates were calculated as:

fatal collisions / total collisions

This normalization helps identify boroughs with higher severity risk independent of collision volume.

🔑 Key Findings
Temporal Patterns

Collisions peak during commute hours

Weekdays have higher total collisions

Late-night weekend crashes tend to be more severe

Collision counts dropped sharply in 2020 due to COVID-19 mobility reductions

Geographic Patterns

Collision counts vary significantly by borough

Fatal collision rates differ across boroughs after normalization

Injury Patterns

Most crashes cause no injuries

A small number of severe crashes account for a large share of injuries

Contributing Factors

Driver behavior is the dominant cause:

Driver inattention

Failure to yield

Unsafe following distance

🛠️ Technologies Used

Python

Pandas

NumPy

Seaborn

Matplotlib

Jupyter Notebook

📂 Repository Structure
IE6600-NYC-Collision-Analysis
│
├── data/
│   Motor_Vehicle_Collisions.csv
│
├── notebooks/
│   collision_analysis.ipynb
│
├── outputs/
│   plots/
│
├── report/
│   IE6600_Project2_Report.pdf
│
└── README.md
📚 Future Work

Future analysis could incorporate:

Weather data

Speed camera locations

Vision Zero enforcement data

Predictive models for high-risk collision events
