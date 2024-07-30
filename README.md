# Evaluating-different-time-series-models-to-predict-COSTCO-sales
This project trains different time series models, including VAR, Random Walk, ARIMA, OLS, and Exponential Moving Average, to predict COSTCO sales

Introduction to Time series analysis to forecast
In this analysis, we train different time series models to predict COSTCO sales. The method basically consists of applying a rolling window to the target variable (sales), which is first made stationary using seasonal adjustment, in order to move the sample and train the models. We use the MSE to select the best model adjustment, comparing it with a NAIVE method, which consists of an Exponential Moving Average

The gravitational metaphor, illustrated by the interaction between two spheres in the accompanying image, vividly demonstrates how the intrinsic value influences and ultimately guides market prices, asserting that despite temporary deviations, prices will converge on their true economic worth in the long run.

This visualization and explanation underscore the core tenet of value investing: market rationality will prevail as prices gravitate towards their fundamental intrinsic values over the long term.

image

Objective
The aim of this analysis is to determine the fundamental price of Nike stocks, which acts as a gravitational point drawing the current market price towards it. The primary objective is to estimate this fundamental value and project the time series for the next 24 months, assuming that the fundamental values remain relatively stable.

Data
Source and Accessibility

The financial metrics used in this analysis are sourced from stockrow.com, a reliable provider of comprehensive financial data for publicly traded companies. This platform offers a wide array of financial metrics crucial for conducting detailed financial analyses.

image

Estimation Method
Objective and Approach To estimate the fundamental price of Nike's stock, we initially identify the most predictive financial metrics. An Ordinary Least Squares (OLS) regression model is then employed, selecting Sales and EBITDA as primary predictors. These metrics were chosen for their significant roles in representing revenues and profitability, respectively.

Statistical Significance and Model Efficacy The chosen variables are both statistically and economically significant, with the regression model explaining approximately 90% of the variance in Nike's stock price. This high degree of explanation underscores the robustness of the model in capturing key price drivers.

Visual Analysis The following images display the regression analysis results and the correlation matrix, visually substantiating the strong relationship between the chosen variables and the stock price:

Regression Analysis Results

image

image

Finally, we apply the Hodrick-Prescott filter to isolate the trend components within the Sales and EBITDA series. These components are then utilized to estimate a linear projection in our OLS model. This method facilitates an effective evaluation of these trends, enabling us to accurately predict the fundamental price of Nike stocks

image

ARIMA Projections
Using Fundamental stock price data, an ARIMA model will be configured to forecast the price movements for the next two years. This section will detail the selection process for the ARIMA model parameters (p, d, q) and discuss the model’s fit and forecast accuracy. The model's predictions will be compared against the estimated intrinsic values to identify potential periods where the stock might be under- or over-valued.

To select the appropriate ARIMA model, we utilize the auto.arima function in RStudio, which determines the optimal ARIMA order by minimizing the AIC criterion

image

Results and conclusions
The analysis results show that, over the last year, Nike's stock price has been significantly lower than its fundamental values. According to value investing theory, this presents a good opportunity to buy Nike stock at the current price due to the substantial safety margin it offers. Furthermore, if the sales and EBITDA remain relatively stable, the continued decline in current prices could present an even more compelling buying opportunity.

image
