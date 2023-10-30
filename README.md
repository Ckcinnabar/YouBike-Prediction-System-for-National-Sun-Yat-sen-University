#YouBike Prediction System for National Sun Yat-sen University

This project is dedicated to providing predictive insights for YouBike shared bicycles specifically around the National Sun Yat-sen University in Kaohsiung City, Taiwan. Utilizing the TDX (Transport Data Exchange) API, the script fetches real-time station data for YouBike stations within a 1km radius of the university. The ARIMA forecasting model is then employed to predict which of these stations are likely to run out of bikes or slots within the next 10 minutes.


##Key Features
1. Data Collection: Fetches real-time statuses of YouBike stations situated within 1km of National Sun Yat-sen University using the TDX API.
2. Time Series Forecasting: Implements the ARIMA time series forecasting model to predict the number of available bikes and slots at each station in the near future.
3. Automated Predictions: The system is designed to automatically conduct predictions every 10 minutes, ensuring up-to-date insights.

##Notes
1. It's crucial to have the client_id and client_secret for the TDX API to fetch data.
2. Although this script focuses on the vicinity of National Sun Yat-sen University, the methodology can be adapted to other locations by adjusting the coordinates and parameters.
3. Ensure you have a stable internet connection, as the script communicates with external APIs for data collection.

##Potential Improvements
1. Integrate with a visualization tool or dashboard to provide graphical representations of predictions.
2. Implement notifications or alerts when stations are predicted to run out of bikes or slots.
