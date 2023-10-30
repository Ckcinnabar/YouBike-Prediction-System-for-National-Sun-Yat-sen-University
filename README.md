# YouBike Prediction System for National Sun Yat-sen University

This project is dedicated to providing predictive insights for YouBike shared bicycles specifically around the National Sun Yat-sen University in Kaohsiung City, Taiwan. Utilizing the TDX (Transport Data Exchange) API, the script fetches real-time station data for YouBike stations within a 1km radius of the university. The ARIMA forecasting model is then employed to predict which of these stations are likely to run out of bikes or slots within the next 10 minutes.

## Overview
Target Area: 1-kilometer radius around NSYSU, Kaohsiung City, Taiwan.
Data Source: TDX (Transport Data Exchange) API.
Prediction Model: ARIMA time series forecasting model.

## Key Features
### Real-time Data Collection:
1. Fetches current status of YouBike stations within the specified area.
2. Data includes station ID, station name, bike capacity, available bikes for rent, type of available bikes (electric or general), and available slots for bike returns.
### Automated Predictions:
1. Continuously runs every 10 minutes to gather fresh data.
2. Uses the ARIMA model to predict which stations will likely have no bikes available for rent or no open slots for returns in the next 10 minutes.
### Data Storage:
Saves the collected data to a CSV file named 國立中山大學幾何中心周圍1公里Youbike站點即時狀態.csv.

## Notes
1. It's crucial to have the client_id and client_secret for the TDX API to fetch data.
2. Although this script focuses on the vicinity of National Sun Yat-sen University, the methodology can be adapted to other locations by adjusting the coordinates and parameters.
3. Ensure you have a stable internet connection, as the script communicates with external APIs for data collection.

## Potential Improvements
1. Integrate with a visualization tool or dashboard to provide graphical representations of predictions.
2. Implement notifications or alerts when stations are predicted to run out of bikes or slots.

## Acknowledgments
This project utilizes data from the TDX platform, provided by the Taiwanese government to promote the use of shared transportation data.
