# Global Earthquake Visualization: A Microsoft Fabric Project


**"Global Earthquakes: Visualize the world's seismic activity."**

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

## Getting Started

1.  **View the Report:**
    * [Link to Power BI Report](YOUR_POWER_BI_REPORT_LINK_HERE)
2.  **Explore the Code:**
    * (If applicable, add a link to a GitHub repository or code location)

## Usage

* Use the date range filter to analyze earthquake activity during specific periods.
* Explore the map to identify regions with high seismic activity.
* Use the significance classification filter to focus on earthquakes of a specific level.
