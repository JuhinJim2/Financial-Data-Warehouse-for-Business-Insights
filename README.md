# Maritime Traffic and Vessel Tracking System | End to End Data Engineering

## Introduction

An end-to-end data pipeline for tracking maritime vessel movements and analyzing traffic patterns in a specific region.  This system will use Automatic Identification System (AIS) data, weather data, and historical traffic data to create insights about shipping lanes, potential congestion points, and environmental impacts.

## Architecture 
<img src="Sequence diagram.png">

## Technology Used

- **Python** (Pandas, NumPy, GeoPandas, Requests)
- **Time-series Database:** InfluxDB, TimescaleDB
- **Data Pipeline Orchestration:** Apache Airflow or Prefect
- **Weather APIs:** OpenWeatherMap, NOAA API
- **GIS Mapping & Visualization:** Folium (for maps), Plotly/Dash for interactive visualizations, Grafana for real-time dashboards
- **Machine Learning:** Scikit-learn, TensorFlow, or PyTorch for congestion prediction
- **Cloud Platforms:** AWS (S3, Lambda, EC2), Google Cloud Storage, or Azure

## Data Sources

- **AIS Data:** Collect real-time maritime vessel position data from public AIS feeds or APIs (e.g., MarineTraffic, VesselFinder).
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

5. **Traffic Congestion Prediction:**
    - Develop a model to predict congestion points in major shipping lanes, considering factors like port activity, historical traffic, and weather conditions.
    - Use machine learning models like time series forecasting (e.g., ARIMA, LSTM) or regression models to predict delays and high-traffic zones.

6. **Real-Time Dashboard and Visualization:**
    - Build a real-time dashboard using tools like **Grafana**, **Power BI**, or **Plotly Dash** to visualize the current positions of vessels on a map, weather conditions, and potential congestion points.
    - Display key performance metrics (e.g., number of vessels per region, average speed, weather impact) for maritime operators to make informed decisions.
    - Integrate interactive map features to track vessel movements, ports, and regions with heavy traffic.

7. **Alerting System:**
    - Set up an alert system that triggers notifications when:
        - A vessel deviates from its planned route.
        - Vessel congestion exceeds a threshold in critical shipping lanes.
        - Weather conditions are expected to worsen, potentially affecting traffic.

## Data Model
<img src="uber_data_model.png">


## Sample Looker Visualization
<img src="Uber_Data_Analytics_-_Payment_Type_Distribution.png">

This is a sample dashboard. Data analysts can create their own dashboards tailored to their specific use cases since the data is at an atomic level.

See Sample Dashboard: https://lookerstudio.google.com/reporting/e9764425-6638-4eba-ac09-e9e3977c28fc

## Credits
All of the credits belong to Darshil Parmar for inspiration and resource.
# Financial-Data-Warehouse-for-Business-Insights
