# Evaluating-different-time-series-models-to-predict-COSTCO-sales
This project trains different time series models, including VAR, Random Walk, ARIMA, OLS, and Exponential Moving Average, to predict COSTCO sales

## Introduction to Time series analysis to forecast

In this analysis, we train different time series models to predict COSTCO sales. The method basically consists of applying a rolling window to the target variable (sales), which is first made stationary using seasonal adjustment, in order to move the sample and train the models. We use the MSE to select the best model adjustment, comparing it with a NAIVE method, which consists of an Exponential Moving Average


## Data
Source and Accessibility

The financial metrics used in this analysis are sourced from Stockrow.com, a reliable provider of comprehensive financial data for publicly traded companies. This platform offers a wide array of financial metrics crucial for conducting detailed financial analyses. Personal income data was acquired from the Bureau of Economic Analysis, U.S. Department of Commerce.

![image](https://github.com/user-attachments/assets/fc9b45b1-e84f-411d-9be8-0c560749c51d)


## Estimation Method

We estimate different time series models to forecast COSTCO sales, using an Exponential Moving Average as the baseline. The ARIMA model is considered using the auto.arima function. The RW model is a Random Walk, which basically consists of predicting a new value by replicating the last value in the training set. The VAR model was estimated with 2 lags, incorporating Walmart sales and Personal Income data according to official sources. The OLS model includes Personal Income and Walmart sales, along with their squared values, as exogenous variables. 

![image](https://github.com/user-attachments/assets/ebcfbd4b-9775-4190-975a-abd9ce31be87)

## Forecast Analysis Results
As a first approach, it is possible to observe that the Mean Squared Error suggests that the best adjustment corresponds to the Exponential Moving Average model, followed by the ARIMA and VAR models. In all these cases, the forecast variance is smaller than the target variable variance, which supports the idea that these models are useful. The OLS and PCA (Principal Component Analysis) adjustments perform poorly, as their variance exceeds the variance of the target variable 

https://en.wikipedia.org/wiki/Mean_squared_error

![image](https://github.com/user-attachments/assets/e99d341b-2356-417a-9a11-cdfc2dfe6d8d)

This result is consistent with the following graph, where we show the cumulative Mean Squared Error throughout the sample. It is easy to observe how the Naive (EMA) model, followed by the ARIMA and VAR models, achieve the best performance

![image](https://github.com/user-attachments/assets/f4be92ad-0539-419d-950e-2596b611d7ef)


ARIMA Projections
Using Fundamental stock price data, an ARIMA model will be configured to forecast the price movements for the next two years. This section will detail the selection process for the ARIMA model parameters (p, d, q) and discuss the model’s fit and forecast accuracy. The model's predictions will be compared against the estimated intrinsic values to identify potential periods where the stock might be under- or over-valued.

To select the appropriate ARIMA model, we utilize the auto.arima function in RStudio, which determines the optimal ARIMA order by minimizing the AIC criterion

image

Results and conclusions
The analysis results show that, over the last year, Nike's stock price has been significantly lower than its fundamental values. According to value investing theory, this presents a good opportunity to buy Nike stock at the current price due to the substantial safety margin it offers. Furthermore, if the sales and EBITDA remain relatively stable, the continued decline in current prices could present an even more compelling buying opportunity.

image
