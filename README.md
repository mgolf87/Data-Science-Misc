# Data-Science-Misc
Collection of various Data Science topics and techniques.
<br />

## Quantile Regression
### QuantileRegression.ipynb
#### How can DoorDash give us an estimated delivery range?
Quantile Regression is used to generate bounds (i.e. DoorDash: "Your order will arive in 25 to 35 minutes")
<br />
<br />
**Regression Loss Function:** <br />
L = (y - Xθ)^2
<br />
<br />
**Quantile Loss Function:** <br />
L = τ(y - Xθ) if y - Xθ >= 0 : predicted value low, used for low quantiles, penalizes high
<br />
L = (τ - 1)(y - Xθ) if y - Xθ < 0  : predicted value high, used for high quantiles, penalizes low
<br />
<br />
**Penalize the Loss when:** 
<br />
The percentile τ is low, but the prediction is Xθ is high  
The percentile τ is high, but the prediction is Xθ is low
<br />
<br />
For this example we will be using τ = [0.2, 0.5, 0.9] however we will only consider the 20th and 90th quantile as we want our time prediction to have a minimum at 20% and a maximum at 90%. Thus, ensuring that we don't get the hopes up of the customers too much like a 10% minimum time might. As well, we don't want our maximum to be higher than 90% as this may skew our range to appear greater than what is likely.
<br />
<br />

## Centered Moving Average (CMA)
### Forecasting, Seasonality
### CMA Forecast MGolf.xlsx
Moving Averages are used to analyze data through generating series of the averaged data where each series is constrained by a given period. For biological and some financial data these time periods may tend towards seconds or milliseconds, however larger time periods like quarters or years are frequently used for analyzing and forecasting financial data. When the period analyzed is even the moving average falls on a fractional number, this doesn't make sense when analyzing months as we want to know the values for the 7th month not the 7.5th month. Therefore, we must center the data by averaging two consecutive periods, thus producing an integer value.
<br />
<br />
**Net Revenue Forecasting using CMA:**
<br />
**(1)** Using CMA we find the deseasonalized net revenue for each month
<br />
**(2)** Generate a trend line for the deseasonalized data
<br />
**(3)** Find the seasonal index for each month and estimate future net revenue
<br />
**(4)** Modify the estimate by incorporating seasonality into the forecast
<br />
*Any metric which can be evaluated over periods can be analyzed using CMA*
<br />
<br />
Graphs are generated which compare the net revenue, cost of goods and services (COGS), and the year over year (YOY) growth of the net revenue for the 2019, 2020, and 2021 time periods. As well, the whole 2021 year was forecasted using CMA for both the net revenue and YOY growth metrics. The forecasted seasonal trend of the net revenue is also represented in a graph and clearly displays a seasonality in the data. Actual net revenue is compared to the CMA forecast, where accuracy is evaluated by measuring the percent error. A high accuracy is indicated by a percent error lower than 5%, a moderate accuracy is between 5 and 10%, and a low accuracy is anything greater than 10%. Net revenue is compared for all years (2019, 2020, 2021) using the forecasted (2021) data, and the YOY Growth of the net revenue in 2020 is compared to the forecasted values for 2021.
<br />
<br />

## Topic 3
### Files
Description

<br />
<br />

## Topic 4
### Files
Description

<br />
<br />

## Topic 5
### Files
Description

<br />
<br />

## Topic 6
### Files
Description
