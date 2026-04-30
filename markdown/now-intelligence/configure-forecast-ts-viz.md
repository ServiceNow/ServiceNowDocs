---
title: Configure a forecast in a time series visualization
description: If a time series visualization is configured to show forecasts, you can configure the forecasts for that visualization.Forecasting uses standard statistical methods. You can select a method or let the system choose one automatically.If you are a statistics expert, you can select a forecast method manually. By default, the instance chooses the best method for you automatically, based on the fit of the method.Forecast periods have a default length that depends on the frequency of the data sources. Not all data sources have the same frequencies.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Create time series visualizations, Data visualizations in Platform Analytics, Platform Analytics]
---

# Configure a forecast in a time series visualization

If a time series visualization is configured to show forecasts, you can configure the forecasts for that visualization.

## Before you begin

This procedure assumes you have created a [time series visualization](create-dv-time-series-ac.md) for a non-table data source and you want to configure forecasting for that visualization.

**Note:** Support is not provided for the Hour of day or Day of week aggregations on table data.

Role required: Any role that can create a time series visualization. For non-indicator data sources, a subscription to Performance Analytics is also required.

## About this task

When you configure forecasting on a data visualization, you override any forecast configuration set on the data source, such as an indicator. The override applies only to the specific data visualization.

## Procedure

1.  Open the configuration panel of the time series visualization.

2.  In **Additional settings**, activate **Show forecast**.

    Table data sources do not support forecasting.

3.  Select **Configure forecast**.

    The **Configure forecast** pane opens.

4.  Complete the following fields:

<table id="table_vjr_2vs_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Forecast method

</td><td>

The statistical method the system uses to forecast values for this indicator. The default value is Auto, meaning that the system chooses a method that best fits the data. For more information, see [Forecast methods](configure-forecast-ts-viz.md#) and [Automatic selection of forecast methods](configure-forecast-ts-viz.md#).

</td></tr><tr><td>

Period length

</td><td>

The number of data points needed to establish a pattern in the time series. If you select **Use default**, the period length depends on the frequency of the data source. For example, the period length for a time series with a daily frequency is 7 data points by default. For more information, see [Default forecast period lengths](configure-forecast-ts-viz.md#).

</td></tr><tr><td>

Number of periods to look ahead

</td><td>

Number of data periods in the future to forecast scores for.

</td></tr><tr><td>

Forecast range lower limit

</td><td>

The lowest meaningful value of a forecast score. If a score lower than this value is forecast, this value is displayed instead.

</td></tr><tr><td>

Forecast range upper limit

</td><td>

The highest meaningful value of a forecast score. If a score higher than this value is forecast, this value is displayed instead.

</td></tr></tbody>
</table>5.  Select which data to base the forecast on.

<table id="choicetable_jhq_bkr_5xb"><tbody><tr><td id="d46157e217">

**Visualization date range**

</td><td>

All data within the date range of the visualization

</td></tr><tr><td id="d46157e226">

**Previous periods**

</td><td>

The number of data periods before the present to base forecasts on. These data periods are the same length as the ones in **Period length**.If you select Previous periods, also specify the number of periods in the **Number of periods to consider** field.

</td></tr><tr><td id="d46157e243">

**Specific starting date**

</td><td>

All scores collected after a start date. If you select Specific starting date, also specify the **Start date**.

</td></tr></tbody>
</table>    **Warning:** If there are insufficient data points to generate a forecast, nothing is shown, neither the forecast nor a message.


**Related topics**  


[Performance Analytics scores forecasts](../../performance-analytics/concept/c_ForecastingData.md#)

## Forecast methods

Forecasting uses standard statistical methods. You can select a method or let the system choose one automatically.

<table id="table_vhn_pmr_5xb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Linear

</td><td>

Generates a linear regression forecast based on the historical scores, using constant and trend as explanatory variables.

</td></tr><tr><td>

Seasonal

</td><td>

Generates a linear regression forecast based on the historical scores, using seasonal dummies as explanatory variables. A 'season' for this analysis is one period.

</td></tr><tr><td>

Seasonal Trend

</td><td>

As Seasonal, but includes a trend as an explanatory variable.

</td></tr><tr><td>

Seasonal Trend Loess \(STL\)

</td><td>

Generates a seasonal forecast based on a best-fit function. This method fits a trend, a season, and a random noise process to the data using an exponentially weighted moving average approach. The forecast is based on the full data set, with more weight given to more recent observationsA 'season' for this analysis is one period.

</td></tr><tr><td>

Random Forest \(RF\)

</td><td>

Creates a combination of decision trees where the predictions produced by these trees are averaged to get a single prediction. The randomness comes from each tree being built from a random subset of the available data and inputs. For more information about the random forest method, see this [Medium article](https://williamkoehrsen.medium.com/random-forest-simple-explanation-377895a60d2d).

</td></tr><tr><td>

Autoregressive \(AR\)

</td><td>

The autoregressive \(AR\) model forecasts future values of an indicator by using a linear combination of a trend, seasonal dummies, and past values. Like the Random Forest \(RF\) model, the AR model checks for the best number of lags. However, the AR model relates current to past values linearly, whereas the RF model is non-linear.

</td></tr></tbody>
</table>## Automatic selection of forecast methods

If you are a statistics expert, you can select a forecast method manually. By default, the instance chooses the best method for you automatically, based on the fit of the method.

To determine the best fitting forecast method, the instance generates forecasts using each forecast method with your historical data. The instance then compares those forecasts with the latest data based on how far ahead you want to forecast. The instance performs this evaluation each time it displays the forecast. Therefore, collecting additional scores or changing the forecast period can alter which forecast method is used.

Consider a time series visualization of a Performance Analytics indicator with a daily frequency. You configure forecasting on the visualization to use a period length of 7 days and to base forecasts on the previous two periods. The instance applies each forecasting method to your historical data that is older than two weeks. Then the instance compares those forecasts against the latest two weeks of data. The forecast that most closely fits the latest two weeks of data is then recalculated using the entire data set. The visualization shows the results of this final calculation.

## Default forecast period lengths

Forecast periods have a default length that depends on the frequency of the data sources. Not all data sources have the same frequencies.

### Default period lengths common to all data sources

|Score frequency|Number of data points per period|Total period length|
|---------------|--------------------------------|-------------------|
|Daily|7|1 Week|
|Weekly|13|1 Quarter|
|Bi-weekly|6|1 Quarter|
|Four Weekly|13|1 Year|
|Monthly|12|1 Year|
|Bi-monthly|6|1 Year|
|Quarterly|4|1 Year|
|Fiscal Quarterly|4|1 Year|
|Half Yearly|2|1 Year|
|Yearly|4|4 Years|
|Fiscal Yearly|4|4 Years|

### Default period lengths unique to MetricBase

|Score frequency|Number of data points per period|Total period length|
|---------------|--------------------------------|-------------------|
|Minutely|100|Dynamic, controlled by data source depending on query|

