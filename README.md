# Financial Data Warehouse for Business Insights

## Project Overview:

This project focuses on developing and maintaining an enterprise-level data warehouse, integrating API to pull business financial data, and creating an ETL pipeline for efficient data management. The final goal is to provide actionable business insights through reports and dashboards in Power BI/Looker.

## Architecture 
<img src="Sequence diagram.png">

## Technologies Used:

- **Programming Languages** Python, SQL
- **ETL Tools:** Apache Airflow
- **APIs** API (for financial data)
- **Data Warehouse:** Google Cloud Storage, SQL Server / Azure SQL Database
- **Data Visualization:** Power BI

## Data Sources

- **Payroll Data:** Collect real-time maritime vessel position data from public AIS feeds or APIs (e.g., MarineTraffic, VesselFinder).
- **Weather Data:** Integrate weather data (wind speed, temperature, etc.) to analyze the effect of weather conditions on maritime traffic.
- **Port Data:** Collect data on port arrivals and departures, shipping schedules, and cargo traffic.
- **Historical Vessel Traffic:** Use historical AIS data or simulated data to study patterns and predict traffic congestion.

## Data Sources

1. **Data Collection and Ingestion:**
    - Ingest real-time vessel location data from AIS APIs.
    - Collect weather data from public APIs (e.g., OpenWeatherMap, NOAA).
    - Gather historical maritime traffic data (e.g., vessel movements, port data).

2. **Data Preprocessing:**
    - Clean and preprocess the raw AIS data (e.g., timestamp corrections, coordinate normalization).
    - Handle missing or erroneous data (e.g., when a vessel's GPS signal is lost).
    - Merge and join AIS data with weather data based on timestamps to analyze vessel performance under different weather conditions.

3. **Data Storage:**
    - Store real-time AIS data in a time-series database (e.g., InfluxDB, TimescaleDB) for easy querying of vessel positions and movements.
    - Store aggregated vessel traffic and weather data in a relational database (e.g., PostgreSQL, MySQL) for historical analysis.
    - Consider cloud storage solutions like AWS S3 or Google Cloud Storage for large datasets.   

4. **Data Transformation and Analysis:**
    - Implement data pipelines to aggregate vessel movement data by region, time, and type of vessel (e.g., cargo, passenger, tanker).
    - Perform analysis on the speed, trajectory, and route of vessels to identify trends in maritime traffic.
    - Analyze weather data in correlation with vessel movement to understand how weather impacts shipping schedules and traffic.


6. **Real-Time Dashboard and Visualization:**
    - Build a real-time dashboard using tools like **Grafana**, **Power BI**, or **Plotly Dash** to visualize the current positions of vessels on a map, weather conditions, and potential congestion points.
    - Display key performance metrics (e.g., number of vessels per region, average speed, weather impact) for maritime operators to make informed decisions.
    - Integrate interactive map features to track vessel movements, ports, and regions with heavy traffic.

## Data Model
<img src="uber_data_model.png">


## Sample Looker Visualization
<img src="Uber_Data_Analytics_-_Payment_Type_Distribution.png">

This is a sample dashboard. Data analysts can create their own dashboards tailored to their specific use cases since the data is at an atomic level.

See Sample Dashboard: https://lookerstudio.google.com/reporting/e9764425-6638-4eba-ac09-e9e3977c28fc

## Credits
All of the credits belong to Darshil Parmar for inspiration and resource.
