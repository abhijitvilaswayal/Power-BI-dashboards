**Weather Monitoring & Air Quality Dashboard**

An interactive real-time dashboard that combines weather and air quality data (AQI) for major Indian cities.
This project helps citizens, planners, and policymakers monitor environmental conditions, assess health risks, and make data-driven decisions for urban planning and public advisories.

**Problem Statement**

Access to consolidated, accurate weather and AQI data is often fragmented and lacks actionable health context.
Goal: Build a unified, live Power BI dashboard that integrates diverse weather & AQI variables for rapid decision-making and public awareness.

**Data Source**

* Primary: WeatherAPI.com – JSON data (current, daily, hourly) with AQI.
* Metrics: Temperature, humidity, UV index, pressure, visibility, wind, rain probability, sunrise/sunset, and pollutants (PM2.5, PM10, CO, SO₂, O₃, NO₂).

**Data Preprocessing & ETL**

* Master Table: Combined all cities’ data and expanded nested JSON (location, forecast, air\_quality).
* Daily & Hourly Forecasts: Separate tables for day-level and hour-level trends with clean timestamps.
* Current Weather: Snapshot table for live conditions.
* Dynamic Background Mapping: Linked weather types to background images for a real-time visual effect.

**Data Modelling**

* Fact Tables: Current, Forecast\_Day, Forecast\_Hour, Master
* Dimension Tables: Weather\_Bg, City, Date
* Helper Table: Measures to organize DAX calculations
* Relationships: One-to-many links between facts and dimensions; bi-directional relationship for dynamic visuals.
* Time Intelligence: Supports YOY/monthly/day-level analysis and historical vs forecast comparison.

**Dashboard Highlights**

* Real-time and forecasted weather and AQI for major Indian cities
* Dynamic tiles and color-coded AQI (green = safe, red = hazardous)
* Drill-down from city-level overview → daily trends → hourly insights
* Displays sunrise/sunset times, daylight duration, and rain probability
* Automatic data refresh ensures up-to-date information

**Key Findings**

* Single-point interface for weather and air quality across cities
* Rapid risk assessment through AQI color codes and pollutant metrics
* Supports event planning and health advisories with accurate forecasts
* Dynamic backgrounds create a visually rich, real-time experience
