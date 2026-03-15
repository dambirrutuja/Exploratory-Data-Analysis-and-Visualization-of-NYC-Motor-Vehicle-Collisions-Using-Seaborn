# Exploratory Data Analysis and Visualization of NYC Motor Vehicle Collisions Using Seaborn
🚦 NYC Motor Vehicle Collisions Analysis
📊 Advanced Data Visualization Using Seaborn

📚 Course: IE6600 – Computation and Visualization for Analytics
🏫 Institution: Northeastern University
📂 Dataset: NYC Motor Vehicle Collisions – Crashes (NYC Open Data / Data.gov)

👥 Team Members

Rutuja Dambir

Praniti Kale

Hiral Hitesh Rana

📌 Project Overview

Motor vehicle collisions are a major urban safety challenge in New York City.
This project analyzes the NYC Motor Vehicle Collisions dataset to uncover patterns in traffic accidents using Python-based data analysis and Seaborn visualizations.

The objective of this project is to identify:

🚗 Collision frequency patterns

🕒 Time-of-day and seasonal trends

📍 Geographic differences across boroughs

🚑 Injury and fatality distributions

⚠️ Leading contributing factors behind crashes

The analysis demonstrates practical data analytics and visualization techniques used in real-world traffic safety research.

🗂 Dataset Information

The dataset was sourced from NYC Open Data (data.gov) and contains detailed records of motor vehicle collisions reported across New York City.

Key Attributes in the Dataset

🕒 Temporal Data

Crash date

Crash time

Year, month, and day of week

📍 Geographic Data

Borough

ZIP code

Latitude and longitude

🚑 Safety Outcomes

Number of persons injured

Number of persons killed

Pedestrian, cyclist, and motorist injuries

⚠️ Contributing Factors

Driver inattention

Failure to yield

Unsafe driving behavior

These features allow both temporal and spatial analysis of collision patterns.

🧹 Data Preparation

Before performing analysis, the dataset underwent several preprocessing steps:

Standardizing column names

Handling missing or inconsistent values

Converting data types (dates, numeric fields)

Removing duplicate records

Creating additional analytical features

Engineered Features

Several derived variables were created to support the analysis:

crash hour

year and month

day of week

weekend indicator

total casualties per collision

collision severity classification

These transformations enabled more meaningful visualizations and statistical comparisons.

📊 Exploratory Data Analysis

Seaborn visualizations were used to explore multiple aspects of collision behavior across the city.

Key Analyses Performed

📍 Collision Count by Borough
Shows which NYC boroughs experience the highest number of collisions.

🕒 Collision Distribution by Hour
Reveals daily traffic accident patterns, including peak commute hours.

📅 Collisions by Day of Week and Month
Highlights weekly and seasonal variations in collision frequency.

🚑 Injury Distribution per Collision
Analyzes how severe typical collisions are.

⚠️ Top Contributing Factors
Identifies the most common causes of collisions.

📊 Correlation Heatmap
Explores relationships between numerical safety variables.

🔎 Key Insights

Several important patterns emerged from the analysis:

🕒 Temporal Patterns

Collision frequency peaks during morning (7–9 AM) and evening (4–6 PM) commute hours.

Weekdays have higher collision volumes due to commuter traffic.

Warmer months show increased collision counts due to greater road usage.

📍 Geographic Patterns

Collision counts vary significantly across boroughs.

Higher traffic density areas experience more collisions.

🚑 Injury Patterns

Most collisions result in property damage only.

A small number of severe collisions account for most injuries.

⚠️ Contributing Factors

The most frequently reported crash causes include:

Driver inattention or distraction

Failure to yield right-of-way

Following too closely

These findings align with known driver behavior trends in traffic safety studies.

🛠 Tools & Technologies

The analysis was performed using the following tools:

🐍 Python
📊 Pandas – Data manipulation
📈 Seaborn – Statistical data visualization
📉 Matplotlib – Plot rendering
📓 Jupyter Notebook – Interactive analysis environment

📌 Conclusion

The NYC Motor Vehicle Collisions dataset provides valuable insights into urban traffic safety patterns.

This analysis highlights how collision behavior is influenced by:

Traffic exposure during commute hours

Geographic characteristics of boroughs

Driver behavior and contributing factors

Understanding these patterns can support traffic safety policies, urban planning decisions, and public awareness initiatives.

⭐ This project demonstrates applied skills in data cleaning, exploratory analysis, statistical visualization, and real-world dataset interpretation.
