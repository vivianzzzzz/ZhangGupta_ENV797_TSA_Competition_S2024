# README

Team Members: Chenjia Liu, Xiyue Zhang, Shubhangi Gupta


## Overview
This repository is part of the TSA: Forecasting Competition, aimed at predicting daily demand for January 2011 using historical data on hourly demand, temperature, and relative humidity from January 2005 to December 2010. 

## Data
The `/Competition/Data` directory contains three datasets:
- Hourly demand
- Hourly temperature
- Relative humidity

## Data Wrangling
Hourly data is transformed into daily averages using the method outlined in the R markdown file from Lesson 11, utilizing pipes for efficient data aggregation.

## Models
1. Exponential Smoothing (ETS)
Model Type: ETS(A, A, A) allowing for error, trend, and seasonal components.
Seasonal Periods: 365.25 days to reflect annual seasonality.
Model Evaluation: Accuracy is assessed using holdout samples.

2. TBATS
Model Type: TBATS, chosen for its ability to handle multiple levels of seasonality.
Seasonal Periods: Weekly (7 days) and annual (365.25 days).
Components: Includes Box-Cox transformation, ARMA error modeling, trend, and seasonal components.

3. ARIMA
Model Type: Seasonal ARIMA with external regressors.
Parameters: Differencing parameters and seasonal orders are selected based on ACF and PACF plots.
Regressors: Fourier terms for seasonality, with daily temperature and humidity data as external regressors.

4. Neural Network (NN)
Model Type: NNETAR, a type of recurrent neural network suited for time series data.
Parameters: Configured with P=1 (lagged terms considered) and seasonal periods.
Regressors: Fourier terms to capture seasonality, alongside temperature and humidity, enhancing the model's predictive capability.

## Results and Best Forecast Model

The test scores for all our models are shown below:

The best model we used to forecast the July data is the TBATS model which we obatined a MAPE score of 0.0998: 

<img width="937" alt="截屏2024-04-22 下午3 55 43" src="https://github.com/vivianzzzzz/ZhangLiuGupta_ENV797_TSA_Competition_S2024/assets/143654445/8e2fc978-ab2d-483e-9d79-0ed4d5c86d28">


## License
This project is open source and available under the GNU General Public License v3.0. See the LICENSE file for more information.

