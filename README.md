# NSYSU-YouBike-Forecasting-System

Absolutely! Here's a more detailed README:

NSYSU YouBike Forecasting System
This project is designed to forecast the availability of YouBike shared bicycles specifically around National Sun Yat-sen University (NSYSU) in Kaohsiung City, Taiwan. Leveraging the TDX (Transport Data Exchange) API, the system gathers real-time data for YouBike stations within a 1-kilometer radius of NSYSU. It then uses the ARIMA time series forecasting model to predict which stations are likely to run out of bikes or slots in the next 10 minutes.

Key Features
Real-time Data Collection: Gathers real-time status updates of YouBike stations using the TDX API.
Time Series Forecasting: Employs the ARIMA model to predict the future availability of bikes and slots for each station.
Automated Predictions: The system automates the forecasting process, running predictions every 10 minutes.
Installation
Prerequisites
Python 3.x
Access credentials (client_id and client_secret) for the TDX API.
Steps
Clone the repository or download the script.
Install the required Python packages:
bash
Copy code
pip install pandas requests statsmodels
Ensure that the TDX client_id and client_secret are correctly set in the script.
Usage
Navigate to the directory containing the script.
Run the script:
bash
Copy code
python [script_name].py
The script will start collecting data and making predictions. Every 10 minutes, it will print out the stations predicted to have shortages of bikes or slots.

Notes
This script specifically targets YouBike stations within a 1-kilometer radius of NSYSU.
Make sure you have a stable internet connection to ensure uninterrupted data collection from the TDX API.
The system's accuracy may vary based on the amount of historical data collected. The more data points available, the better the forecasting potential.
