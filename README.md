# NOAA Lightning Analysis

This project analyzes lightning strike data collected by the National Oceanic and Atmospheric Administration (NOAA) to explore patterns, trends, and anomalies in lightning activity across different timeframes and geographic locations. The analysis leverages Python libraries such as pandas, NumPy, Matplotlib, Seaborn, and Plotly to clean, manipulate, and visualize large datasets efficiently. The primary goal is to extract meaningful insights into lightning behavior, identify seasonal trends, and validate the reliability of the dataset for further research.

## Project Overview

The NOAA Lightning Analysis project aims to:

- Analyze lightning strike data from 1987 to 2020, with a focus on 2016, 2017, and 2018.
- Explore seasonal and geographic trends in lightning activity.
- Identify outliers and anomalies in the dataset.
- Validate data quality by checking for missing values, inconsistencies, and geographic accuracy.
- Provide actionable insights for disaster management, climate research, and public safety.

The analysis is based on multiple datasets, including:

- **Lightning Strike Data (2016–2018)**: Contains daily lightning strike counts, geographic coordinates, and location details.
- **Yearly Lightning Data (1987–2020)**: Provides aggregated yearly lightning strike counts for trend analysis.
- **Geographic Data**: Includes latitude, longitude, and location-specific details such as city, state, and zip code.

## Dataset Structure

The datasets contain the following fields:

- **date**: The date when the lightning strike was recorded.
- **year**: The year in which the lightning strike occurred.
- **number_of_strikes**: The total number of lightning strikes recorded on the given date.
- **center_point_geom**: The geometric center point of the lightning strike in the format `POINT(longitude latitude)`.
- **longitude**: The longitude coordinate of the lightning strike location.
- **latitude**: The latitude coordinate of the lightning strike location.
- **zip_code**: The postal zip code of the area where the lightning strike was recorded.
- **city**: The name of the city where the lightning strike occurred.
- **state**: The full name of the state where the lightning strike was recorded.
- **state_code**: The abbreviated state code (e.g., 'AR' for Arkansas).
- **count_lightning**: The cumulative count of lightning strikes recorded for the specified location and time period.

## Data Processing Steps

The data processing steps include:

1. **Loading and Cleaning Data**: The lightning strike data is loaded into pandas DataFrames, cleaned, and structured for analysis. Missing values and duplicates are identified and addressed.

2. **Date Manipulation**: The `date` column is converted to a datetime format, and additional time-based columns (e.g., month, week, quarter) are created for temporal analysis.

3. **Geographic Analysis**: Latitude and longitude coordinates are extracted and validated to ensure geographic accuracy. Lightning strike locations are visualized using Plotly to identify regional hotspots.

4. **Seasonal and Temporal Trends**: Lightning strike data is aggregated by month, week, and quarter to identify seasonal patterns and trends.

5. **Outlier Detection**: Outliers in yearly lightning strike counts are identified using statistical methods such as the interquartile range (IQR) and visualized using boxplots and scatterplots.

6. **Data Validation**: The dataset is validated for completeness and accuracy by checking for missing dates, implausible values, and geographic inconsistencies.

7. **Categorization and Visualization**: Lightning strike counts are categorized into severity levels (e.g., Mild, Scattered, Heavy, Severe) and visualized using heatmaps and bar charts.

## Project Insights

The project provides key insights into lightning activity patterns:

- **Seasonal Trends**: Lightning activity is highest during the summer months, with August consistently recording the most strikes.
- **Geographic Hotspots**: Regions such as the Gulf of Mexico, the Atlantic Ocean, and parts of the Midwest exhibit higher lightning activity.
- **Outliers**: Certain years, such as 1987 and 2019, show anomalous lightning strike counts due to data completeness issues or genuine variations.
- **Data Quality**: Missing data is concentrated over bodies of water and regions outside the United States, highlighting limitations in geographic coverage.

## Project Highlights

- **Data Loading & Cleaning**: Efficiently loads and cleans large datasets using pandas and NumPy.
- **Temporal Analysis**: Aggregates and analyzes lightning strike data by month, week, and quarter to identify seasonal trends.
- **Geographic Visualization**: Uses Plotly to create interactive maps for visualizing lightning strike locations and regional hotspots.
- **Outlier Detection**: Identifies and investigates outliers using statistical methods and visualizations.
- **Data Validation**: Ensures data quality by checking for missing values, inconsistencies, and geographic accuracy.

## Future Work

- **Predictive Models**: Develop predictive models to forecast lightning activity based on historical data and environmental factors.
- **Data Expansion**: Incorporate additional datasets with environmental parameters such as temperature, humidity, and atmospheric pressure to improve the analysis.
- **Interactive Dashboards**: Create interactive dashboards using tools like Dash or Tableau to visualize lightning trends and patterns dynamically.
- **Regional-Specific Studies**: Conduct in-depth analyses of lightning activity in specific regions, such as the Gulf Coast or Midwest, to identify localized trends and inform targeted mitigation strategies.
