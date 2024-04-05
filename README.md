# Stock_Price_Forecasting

## Objective
A company’s stock price is a potent indicator of the company's health, reflecting investor confidence in its ability to weather economic storms, innovate, and deliver shareholder value. Accurately predicting its movements empowers investors to make good decisions, hedge against risks, and capitalize on potential opportunities. Thus, this project aims to predict the daily stock price of Boeing company in Nasdaq stock market with a small datset, wich is useful when dealing with companies that have been listed on the stock market for less than 3 years.

## Data Description

### Overview
The Dataset contains daily records for the stock price of Boeing company in Nasdaq stock market.
This dataset contains 943 rows and 6 columns.

### Data Source
The data for this project comes from Yahoo Finance platform which aggregates data from different stock markets.
Link to dataset : https://finance.yahoo.com/quote/BA/history/

## Data Dictionary
- Open: the opening price of the stock on the given date
- High: the highest price at which the stock traded during the course of the day
- Low: the lowest price at which the stock traded during the course of the day
- Close: the closing price of the stock on the given date
- Volume: the number of shares that changed hands during the given day
- Adj_Close: the closing price of the stock that has been adjusted to include any corporate actions

## Methodologie
We will explore and clean the dataset, then, we will use two univariate models to predict the daily stock prices. Performance will be evaluated based on sevral metric like r2 and mse scores.

## Exploratory Data Analysis

The exploratory visuals include the following plots:

    - a line plot for the boeing daily adj close stock price
    - an autocorrelation plot for the boeing daily adj close stock price
    - a partial autocorrelation plot for the boeing daily adj close stock price
    
<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/Stock_Price_Forecasting/blob/main/Images/boeing_stock_price_lineplot.png">
</p>

This lineplot shows the variation of the boeing daily stock price over the time
## Modeling & Evaluation

###  Models
The models used in this project are the following :

    - ARIMA
    - Prophet
    
### Models Evaluation & Results

<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/Stock_Price_Forecasting/blob/main/Images/arima_test.png">
</p>

This plot shows the performnce of the ARIMA model on the testing data


<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/Stock_Price_Forecasting/blob/main/Images/prophet_test.png">
</p>

This plot shows the performnce of the Prophet model on the testing data


Models were evaluated depending on the R2, MSE, RMSE and MAE. The following are the MAE scores for each model on the testing set and for an horizon of one month:

    - ARIMA: 8.57 
    - Prophet: 14.32

Deponding on all the scores, the ARIMA model had the better performance.

## Recommandations
- The use of the ARIMA model to forecast the daily stock price is reliable for an horizon of one month and an error tolerance of $9.
- Regardless the prformance of this model, It is important to take in consideration any events that can affect the stock price such a pandemic or economic crisis, befor taking any decision.

## Limitations & Next Steps
For an horizon of more than one month the model could not be very reliable so to improve its performance for a higher horizons we can add other features like economic indicators and try to combine different models.
 
