# Analysis of Taxi Mobility Traces and Time Series in Rome

This repository contains a Python notebook that analyzes a mobility dataset of taxis in Rome, Italy, and applies time series forecasting to model future mobility trends. The notebook is divided into two main parts: Mobility Analysis and Time Series Analysis.

## Notebook Content

### 1. Dataset Introduction
The dataset used in this project contains GPS traces from approximately 320 taxis operating in Rome, collected over a 30-day period. These traces provide a detailed view of the mobility patterns within the city. The data is sourced from:
- [Taxi GPS Traces](https://ieee-dataport.org/open-access/crawdad-romataxi)
- [Rome Zones Tessellation](https://www.info.roma.it/mappa_confini_storici_roma.asp)

### 2. Importing Libraries
The notebook utilizes several Python libraries essential for mobility analysis and time series forecasting, including:
- `skmob`: for managing and analyzing mobility data
- `geopandas`: for geographic data handling and manipulation
- `matplotlib` and `folium`: for creating static and interactive visualizations
- `statsmodels` and `sklearn`: for implementing time series models and forecasting

### 3. Visualization Configuration
Custom configurations are applied to Matplotlib to enhance the quality and clarity of the visualizations throughout the notebook.

### 4. Mobility Analysis

#### 4.1 Loading and Visualizing Tessellation
- **Objective**: The tessellation of Rome's zones is loaded from a GeoJSON file, providing a geographic framework for analyzing taxi mobility. Each zone is assigned a unique `tile_ID` to facilitate mobility analysis.
- **Visualization**: An interactive map is created using `folium` and `skmob`, where the tessellated zones of Rome are plotted. This map serves as the base for visualizing taxi movements across different parts of the city.

#### 4.2 Mobility Data Processing
- **Objective**: The taxi GPS data is processed to filter and compress the trajectories, making it more suitable for analysis. This includes noise reduction and trajectory compression using `skmob` preprocessing functions.
- **Techniques Used**: 
  - **Filtering**: Removes GPS points that are considered outliers or errors.
  - **Compression**: Simplifies trajectories by reducing the number of points while preserving essential movement patterns.

#### 4.3 Mobility Pattern Analysis
- **Objective**: The processed mobility data is analyzed to identify key patterns, such as frequent routes, high-traffic zones, and temporal variations in mobility (e.g., rush hours vs. off-peak times).
- **Visualization**: Heatmaps and trajectory maps are generated to visualize these patterns, providing insights into how taxis navigate through different areas and times in Rome.

### 5. Time Series Analysis

#### 5.1 Preparing Data for Time Series Analysis
- **Objective**: The mobility data is aggregated over time to create time series data. This includes aggregating the number of trips, average speeds, or other relevant metrics by hour, day, or week.
- **Techniques Used**: 
  - Time series data is created by resampling and aggregating the original GPS traces based on temporal intervals.

#### 5.2 Time Series Forecasting Models
- **Objective**: Various statistical and machine learning models are applied to the time series data to forecast future mobility trends.
- **Models Implemented**:
  - **Simple Exponential Smoothing (SES)**: Models the time series by exponentially weighting past observations.
  - **Holt's Linear Trend Model**: Extends SES by adding a linear trend component.
  - **Exponential Smoothing with Seasonality (Holt-Winters)**: Incorporates both trend and seasonality into the model.
  - **ARIMA/SARIMA**: Models the time series using autoregressive integrated moving averages, with or without seasonality.

#### 5.3 Model Evaluation and Comparison
- **Objective**: The performance of the forecasting models is evaluated using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Log Error (RMSLE).
- **Results**: The models are compared to identify the best-performing approach for predicting future mobility trends in Rome.
