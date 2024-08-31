# Analysis of Taxi Mobility Traces in Rome

This repository contains a Python notebook used to analyze a mobility dataset based on GPS traces of taxis in Rome, Italy. The project employs spatial and temporal analysis techniques to visualize and predict mobility patterns.

## Notebook Content

### 1. Dataset Introduction
The dataset used in this project contains GPS traces of approximately 320 taxis in Rome, collected over a period of 30 days. The data was sourced from the following:
- [Taxi GPS Traces](https://ieee-dataport.org/open-access/crawdad-romataxi)
- [Rome Zones Tessellation](https://www.info.roma.it/mappa_confini_storici_roma.asp)

### 2. Importing Libraries
The notebook uses several Python libraries, including:
- `skmob`: for mobility analysis
- `geopandas`: for handling geographic data
- `matplotlib` and `folium`: for data visualization
- `statsmodels` and `sklearn`: for temporal trend forecasting

### 3. Visualization Settings
Custom settings to enhance the quality of graphical visualizations produced during the analysis.

### 4. Loading and Visualizing Tessellation
The tessellation of Rome's zones is loaded from a GeoJSON file and visualized on an interactive map using `geopandas` and `skmob`.

### 5. Loading the Taxi Dataset
The taxi mobility dataset is read and prepared for analysis in the subsequent sections of the notebook.

