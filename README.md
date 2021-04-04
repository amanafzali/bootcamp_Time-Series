# Time Series and Regression Analysis

![demo](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/Time%20series%20demo.png?raw=true)

## Introductions

In this project I will analyze time series tolls to predict future movement in the value of the Japanese yen vs U.S dollar. In order to predict forecasting two time series analysis notebooks used. Time Series forecasting and Linear Regression Forecasting

## Time-Series Forecasting

In this notebook, I have loaded historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

In order to complete Time-Series Forecasting I have performed following steps.

1. Decomposition using a Hodrick-Prescott Filter

![Settle](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/Settle%20vs%20Trend.PNG?raw=true)


2. Forecasting Returns using an ARMA Model.

![ARMA](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/ARMA%20model%20results.PNG?raw=true)

![ARMA](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/5%20days%20return%20forecast.PNG?raw=true)

3. Forecasting the Settle Price using an ARIMA Model.

![ARIMA](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/ARMA%20model%20results.PNG?raw=true)

![ARIMA](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/5%20days%20future%20forecase.PNG?raw=true)

4. Forecasting Volatility with GARCH.

![GARCH](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/GARCH%20results.PNG?raw=true)

![GARCH](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/5%20Days%20forecast%20of%20volatility.PNG?raw=true)


## Linear Regression Forecasting

In this notebook, I have built a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with lagged Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

To analyze Linear Regression Forecasting the following steps are completed.

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.

![prediction](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/Predictions.PNG?raw=true)


4. Out-of-sample performance.
5. In-sample performance.

![prediction](https://github.com/amanafzali/bootcamp_Time-Series/blob/main/Pictures/Performance.PNG?raw=true)


## Conclusions

 Based on times series analysis using ARMA and ARIMA models and forecasting of volotility with GARCH it looks good and trending upward so I will by the yen for now.

Using GARCH model for volatility forecasting it looks like volatility of yen is increasing over time so the expected risk will also increase.

Based on evaluation I would not feel confident using these models for longer term investment because The ARMA model (p > 0.05) also the ARIMA model (p > 0.05) and looking to volatility forecasting GARCH 5 days is significantly volatile.

With Linear Regression Forecasting model when comparing out of sample and in sample performances it looks like Out-of-Sample Root Mean Squared Error (RMSE): 0.41545437184712763 and In-sample Root Mean Squared Error (RMSE): 0.5962037920929946 since in sample RMSE is higher than out of sample RMSE so we can say that out of sample data performed better.
