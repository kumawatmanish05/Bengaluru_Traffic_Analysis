# Bengaluru Traffic Analysis Dashboard

## Project Overview

An interactive data analysis & visualization project exploring traffic, average speed and congestion patterns in Bengaluru. 

This project identifies high-congestion hotspots, best-performing routes, and analyzes daily, weather-based, and monthly traffic trends using an interactive Streamlit dashboard provides a comprehensive look at traffic volume, average speeds, and congestion levels, with insights derived from a detailed analysis of traffic data from 2022 to 2024.

The primary goal is to help users understand key factors influencing traffic, such as monthly, yearly and daily seasonal patterns, weather conditions, and the impact of public transport availability.

## Dataset
- **Source:** Kaggle Dataset
- **Dataset Size:** 8000+ Rows x 16 Cols
- **Period Covered:** 2022 - 2024
- **Key Columns:**
  - `Area Name`
  - `Road/Intersection Name`
  - `Traffic Volume`
  - `Average Speed`
  - `Congestion Level`
  - `Weather Conditions`
  - `Day of Week`

## Exploratory Data Analysis (EDA)

- **Data Cleaning:** Handled missing values, duplicates, added new derived columns.
- **Traffic Trends:** Explored by month, weekday/weekend, and area.
- **Congestion Patterns:** Identified bottleneck intersections.
- **Comparative Insights:** Found top 3 most problematic and best performing traffic locations.

Complete EDA is found here: [02_eda_analysis.ipynb](Notebooks/02_eda_analysis.ipynb)

## Visualize Data
```python
most_problematic_locations = avg_speed_congestion_lvl.sort_values(
  by = ["Congestion Level", "Average Speed"], 
  ascending = [False, True]).head(3)

print("Top 3 locations with High Traffic Volume, Low Average Speed and High Congestion Level:\n", most_problematic_locations)
```

```python
best_performing_locations = avg_speed_congestion_lvl.sort_values(
  by = ["Average Speed", "Congestion Level"], 
  ascending = [False, True]).head(3)

print("Top 3 locations with Low Traffic Volume, High Average Speed and Low Congestion Level:\n", best_performing_locations)
```

## Technical Stack

* **Python:** The core programming language for the project (Pandas, NumPy, Matplotlib, Seaborn).
* **Streamlit:** Used to build the interactive web dashboard and create the user interface.
* **Pandas:** Essential for data loading, cleaning, manipulation, and aggregation.
* **Plotly Express:** Used for creating professional, interactive, and aesthetically pleasing data visualizations.

