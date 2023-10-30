# YouBike Prediction System for National Sun Yat-sen University

This project is dedicated to providing predictive insights for YouBike shared bicycles specifically around the National Sun Yat-sen University in Kaohsiung City, Taiwan. Utilizing the TDX (Transport Data Exchange) API, the script fetches real-time station data for YouBike stations within a 1km radius of the university. The ARIMA forecasting model is then employed to predict which of these stations are likely to run out of bikes or slots within the next 10 minutes.

![image](https://github.com/chiu0915/NSYSU_nearby_1km_Youbike_station/blob/main/Youbike%E7%AB%99%E9%BB%9E%E3%80%81%E6%A0%A1%E5%9C%B0%E7%AF%84%E5%9C%8D%E3%80%81%E5%B9%BE%E4%BD%95%E4%B8%AD%E5%BF%83(300px).png)

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

## API Call Limitations:
With API Key: 50 calls/second per source IP (no daily limit).
Without API Key: Can only call API through a browser, with a limit of 50 calls per day for each source IP.
Given that this script makes a call every 10 minutes, users are required to register and obtain an API key.

## Potential Improvements
1. Integrate with a visualization tool or dashboard to provide graphical representations of predictions.
2. Implement notifications or alerts when stations are predicted to run out of bikes or slots.




## Exported Table Format:
|Column1|	StationID|	StationName|	StationAddress|	BikesCapacity|	AvailableRentBikes|	ElectricBikes|	GeneralBikes|	AvailableReturnBikes|	UpdateTime|
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----: |
|0|	501209024|	YouBike2.0_濱海臨海路口(西南側)|	濱海二路/臨海二路口(西南側人行道)|	22|	3|	0|	3|	19|	2023/4/18 19:39|
|1|	501209036|	YouBike2.0_一號船渠景觀橋|	濱海二路12號旁人行道|	16|	12|	0|	12|	4|	2023/4/18 19:39|
|2|	501209039|	YouBike2.0_中山大學社科院|	中山大學社會科學院與管理學院間人行道|	30|	0|	0|	0|	29|	2023/4/18 19:39|
|3|	501209040|	YouBike2.0_中山大學海工館|	中山大學海工館旁|	31|	2|	0|	2|	29|	2023/4/18 19:39|
|4|	501209042|	YouBike2.0_鼓山國小(臨海二路)|	臨海二路50號(東南側人行道)|	15|	12|	0|	12|	3|	2023/4/18 19:39|
|5|	501209051|	YouBike2.0_中山大學工學院|	中山大學工學院東側|	24|	3|	0|	3|	21|	2023/4/18 19:39|
|6|	501209052|	YouBike2.0_中山大學圖資大樓|	中山大學圖書館東側|	22|	3|	0|	3|	19|	2023/4/18 19:39|
|7|	501209054|	YouBike2.0_中山大學材料大樓|	中山大學材料大樓西北側|	10|	1|	0|	1|	9|	2023/4/18 19:39|
|8|	501209062|	YouBike2.0_鼓山國小(登山街)|	登山街36號(對側人行道)|	15|	12|	2|	10|	3|	2023/4/18 19:39|
|9|	501209069|	YouBike2.0_中山大學體育館|	中山大學體育館(北側人行道)|	18|	14|	0|	14|	4|	2023/4/18 19:39|
|10|	501209070|	YouBike2.0_中山大學西灣藝廊|	中山大學西灣藝廊(對側人行道)|	17|	4|	0|	4|	12|	2023/4/18 19:39|
|11|	501209071|	YouBike2.0_中山大學海資館|	中山大學海資館(北側)|	17|	0|	0|	0|	17|	2023/4/18 19:39|

![image](https://user-images.githubusercontent.com/86599394/232777628-ab9a8826-49a7-467f-8f7e-905bf7a42d23.png)


## Acknowledgments
This project utilizes data from the TDX platform, provided by the Taiwanese government to promote the use of shared transportation data.
