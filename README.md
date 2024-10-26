# Smart City Traffic Prediction Project

## Introduction
This project focuses on building a traffic prediction system for four key junctions in a city as part of a smart city initiative. The objective is to forecast vehicle counts, helping the city reduce congestion, plan infrastructure, and enhance the quality of urban life. This project is inspired by the JanataHack Machine Learning for IoT competition hosted by Analytics Vidhya ([details here](https://datahack.analyticsvidhya.com/contest/janatahack-machine-learning-for-iot/#ProblemStatement)).

## Business Understanding
Efficient traffic flow is essential for urban living. With 20 months of traffic data collected at varying intervals, we developed a robust forecasting model to predict vehicle counts over the next four months, aiding city planners in managing traffic effectively.

## Data Preparation & Exploration
- **Data Import & Cleaning**: Imported the traffic dataset, explored vehicle counts, and visualized distributions across junctions.
- **Time Series Processing**: Time series data was prepared with the `xts` package, split by junction, and adjusted for stationarity through differencing.

## Modeling Strategy
- **Stationarity Analysis**: Conducted stationarity tests using the Augmented Dickey-Fuller test and differencing to stabilize trends.
- **Autocorrelation Analysis**: Used ACF and PACF plots to understand time-based dependencies and select suitable ARIMA model parameters.
- **Model Fitting**: Fitted ARIMA and SARIMA models tailored to each junction, with further refinements where necessary.
- **Evaluation**: Different models were tested and evaluated for each junction:
  - **Junction 1**: ARIMA model to capture trend and seasonality.
  - **Junction 2**: SARIMA with seasonal adjustments.
  - **Junction 3**: SARIMA (1,1,1) as an effective model.
  - **Junction 4**: Linear regression with seasonal dummies.

## Sustainable Development Goals (SDGs)
This project supports:
- **SDG 9 (Industry, Innovation, and Infrastructure)**: Through improved traffic forecasting, the project facilitates better urban infrastructure.
- **SDG 11 (Sustainable Cities and Communities)**: By reducing traffic congestion, it helps to create sustainable urban environments.

## Conclusion
Using advanced time series modeling, this project demonstrates the use of data science to support real-world urban planning. The results provide valuable insights for sustainable city development.

## Acknowledgements
Special thanks to Analytics Vidhya for hosting the JanataHack Machine Learning for IoT competition, which inspired this project.
