# Global Earthquake Visualization: A Microsoft Fabric Project


<img width="723" alt="Report" src="https://github.com/user-attachments/assets/509b09a7-4c72-483a-9892-744292ef941f" />



This project leverages the power of Microsoft Fabric to create an interactive and informative visualization of global earthquake data sourced from the USGS API. It provides a clear and engaging way to explore worldwide seismic events.

## Features

* **Interactive Global Map:**
    * Visualizes earthquake locations with bubble sizes representing the maximum significance.
    * Color-coded markers indicate earthquake significance (High, Moderate, Low).
* **Date Range Filtering:**
    * Allows users to focus on specific time periods for analysis.
* **Significance Classification:**
    * Categorizes earthquakes based on their significance levels.
* **Data Enrichment:**
    * Enriches earthquake data with country codes using reverse geocoding.
* **Summary Statistics:**
    * Displays the total number of earthquakes and the maximum significance within the selected date range.

## Project Outline

<img width="926" alt="Project Flow" src="https://github.com/user-attachments/assets/22e4e549-5fa9-48b1-aa10-85f4b37ee458" />


<img width="768" alt="Earthquake lineage" src="https://github.com/user-attachments/assets/ab810669-90d3-4e09-808c-5c097516ef2f" />

## Data Source

[Link to USGS Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/#parameters)


## Technologies Used

* **Microsoft Fabric:**
    * Lakehouse: Centralized data storage.
    * Data Factory: Orchestration of data pipelines.
    * Spark Notebooks: Data processing and transformation using PySpark.
    * Power BI: Interactive data visualization and reporting.
* **Python:**
    * Data manipulation and API interaction.
* **PySpark:**
    * Distributed data processing.
* **USGS API:**
    * Source of earthquake data.
* **`reverse_geocoder`:**
    * Library for reverse geocoding.

## Data Pipeline

1.  **Data Ingestion (Bronze Layer):**
    * Data is fetched from the USGS API using Python and saved as JSON files in the Lakehouse.
2.  **Data Transformation (Silver Layer):**
    * JSON data is transformed into a structured format using Spark Notebooks.
    * Relevant attributes are extracted and renamed.
    * Timestamps are converted to readable formats.
3.  **Data Enrichment (Gold Layer):**
    * Country codes are added using reverse geocoding.
    * Earthquakes are classified based on significance.
    * The data is then stored into a gold layer table.
4.  **Visualization (Power BI):**
    * Interactive dashboards are created to visualize the enriched data.

## View the Report

[Link to Power BI Report](https://app.powerbi.com/groups/2ac10b14-3cf9-4b70-b2e2-b605206d673c/reports/6890675b-910d-433d-ba20-e342508db12d/e58b322cbc35c04557aa?experience=fabric-developer&clientSideAuth=0)


## Usage

* Use the date range filter to analyze earthquake activity during specific periods.
* Explore the map to identify regions with high seismic activity.
* Use the significance classification filter to focus on earthquakes of a specific level.
