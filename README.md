# Energy Forecasting Time Series

## Motivation
Regression and time series techniques are used to forecast and visualize energy usage for millions of customers for resource allocation. With the growing focus on dynamic energy usage, getting accurate forecasts for the use and demand is vitally important. These energy forecasts allow energy companies to better adjust and plan for future energy demand by consumers, which guides policy and resource management. Forecasting too low leads to buy energy from other locations or rolling blackouts while forecasting too high leads to overuse of resources. Finding the optimal balance where supply meets demand is essential for an efficient system.


## Brief description of the three datasets
One way to gain accuracy in the forecasts is to understand what factors impact the energy usage of people, which is why the following datasets where chosen:

* hr_temp_20170201-20200131_subset.csv - this dataset contains hourly (variable DATE) temperature data (variable
HourlyDryBulbTemperature at a weather station near the area of interest.

* hrl_load_metered - 20170201-20200131.csv - This is a dataset contains hourly (variable datetime_beginning_ept) megawatt usage data (variable mw) for the area in Pennsylvania centered around Duquesne. We are using only three years of data because we want to make sure that we look at recent energy patterns that are still applicable to our current customers.
* hr_temp_20200201-20200229_subset.csv - This is the holdout dataset containing just the weather information used as input into the final model to forecast Feb 2020 energy consumption.

We are assuming that temperature and energy data are probably related. The hotter or colder it is outside, the more energy could be consumed by residential and commercial buildings to manage indoor temperature. By combining and cleaning the datasets, we will attempt to explore relationships and eventually build a model to predict future consumption.

A time series model was developed to forecast demand for energy utility using ordinary least squares (OLS) method , then added time series components by adding dynamic effects of autoregressive integrated moving average (ARIMA) models and exponential smoothing (ESM) that further improved the accuracy from 94% (OLS) to 97% (OLS + dynamic effects).

<a href="https://github.com/jonpresto/Energy-Forecasting-Time-Series/blob/main/Notebook%20for%20energy%20forecast.ipynb">CLICK HERE</a> to display final notebook.
