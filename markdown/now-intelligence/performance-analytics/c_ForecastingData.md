---
title: Performance Analytics scores forecasts
description: Performance Analytics enables you to forecast future scores based on past behavior. You can forecast scores on time series widgets, time series data visualizations, KPI Details, and the Analytics Hub. Forecast scores appear as a dotted line.In the record of an automated indicator, configure forecasts as they will appear on the Analytics Hub, Performance Analytics widgets, and time series data visualizations.If you are a statistics expert, you can select a forecast method manually. By default, the instance chooses the best method for you automatically, based on the fit of the method.Depending on the frequency of the score, a different period length is selected. Consult the table to find out the length of the period that is used for your series.When forecasting is enabled for an indicator and there is a global target defined, the forecast shows when the target will be reached.If you apply a time series aggregation to an indicator, the forecast period length changes. The change depends on the type of the time series.In the classic environment, show the forecasts on a time series widget or the Analytics Hub. On a configurable workspace, show the forecasts on a time series data visualization or KPI Details.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Forecast method used, Forecasting method used, Selecting the forecast method, Forecasting and targets, Forecasting with time series]
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics scores forecasts

Performance Analytics enables you to forecast future scores based on past behavior. You can forecast scores on time series widgets, time series data visualizations, KPI Details, and the Analytics Hub. Forecast scores appear as a dotted line.

Forecasting is set up in the **Forecasting** tab of the indicator record. The number of data points included in the forecast depends on the indicator frequency and the number of **Periods to forecast** configured on the indicator. A period is a set number of scores based on the indicator frequency. Regardless of the settings and the forecast method, no more than 2688 forecast data points are generated.

**Note:** In time series data visualizations on a configurable workspace, you can override the forecast configuration that is set on the indicator. This override applies only to that data visualization.

Also in time series data visualizations, you are not limited to forecasts on Performance Analytics indicators. If you have a subscription version of Performance Analytics, you can generate forecasts for any data source except tables. For more information, see [Create time series data visualizations](../../reporting/task/create-dv-time-series-ac.md).

**Related topics**  


[Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#)

## Configure forecasts on an indicator

In the record of an automated indicator, configure forecasts as they will appear on the Analytics Hub, Performance Analytics widgets, and time series data visualizations.

### Before you begin

Role required: pa\_power\_user, pa\_admin, admin

### Procedure

1.  Navigate to **Performance Analytics** &gt; **Indicators** &gt; **Automated indicators**.

2.  Open the automated indicator that you want to configure forecasts for.

3.  Navigate to the **Forecasting** tab.

4.  Set the following values:

<table id="table_h5s_nhr_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Forecast method used

</td><td>

The statistical method the system uses to forecast values for this indicator. The default value is Auto, meaning that the system chooses a method that best fits the data. For more information, see [Selecting the forecast method](c_ForecastingData.md#).

</td></tr><tr><td>

Periods to forecast

</td><td>

Number of data periods in the future to forecast scores for.**Note:** The length of the periods is based on the indicator frequency. For more information, see [Indicator forecast periods](c_ForecastingData.md#).

</td></tr><tr><td>

Forecast lower limit

</td><td>

The lowest meaningful value of a forecast score. If a score lower than this value is forecast, this value is displayed instead.

</td></tr><tr><td>

Forecast upper limit

</td><td>

The highest meaningful value of a forecast score. If a score higher than this value is forecast, this value is displayed instead.

</td></tr></tbody>
</table>5.  Select which scores to base the forecast on.

<table id="choicetable_jhq_bkr_5xb"><tbody><tr><td id="d227652e308">

**All scores**

</td><td>

All the scores that have been collected for this indicator

</td></tr><tr><td id="d227652e317">

**Previous periods**

</td><td>

The number of data periods before the present to base forecasts on. These data periods are the same length as the ones in **Periods to forecast**.If you select Previous periods, also specify the number of periods in the **Periods** field.

</td></tr><tr><td id="d227652e334">

**Fixed start**

</td><td>

All scores collected after a start date. If you select Fixed start, also specify the **Start date**.

</td></tr></tbody>
</table>
## Selecting the forecast method

If you are a statistics expert, you can select a forecast method manually. By default, the instance chooses the best method for you automatically, based on the fit of the method.

To determine the best fitting forecast method, the instance generates forecasts using each forecast method with your historical data. The instance then compares those forecasts with the latest data based on how far ahead you want to forecast. The instance performs this evaluation each time it displays the forecast. Therefore, collecting additional scores or changing the forecast period can alter which forecast method is used.

For example, if you configure an indicator with a daily frequency to forecast ahead two periods, the instance applies each forecasting method to your historical data that is older than two weeks. Then the instance compares those forecasts against the latest two weeks of data. The forecast that most closely fits the latest two weeks of data is then recalculated using the entire data set. The instance shows the results of this final calculation in the Analytics Hub or in KPI Details.

### Forecast methods

Performance Analytics can use the following standard forecast methods.

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
</table>## Indicator forecast periods

Depending on the frequency of the score, a different period length is selected. Consult the table to find out the length of the period that is used for your series.

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

## Forecasting and targets

When forecasting is enabled for an indicator and there is a global target defined, the forecast shows when the target will be reached.

Additionally, the instance sends a notification 14 days before it expects the target to be reached. You can change how many days ahead the notification is sent by setting the **pa.job.forecast.target.days\_to\_check** property.

This functionality is available only for global targets. Thresholds and personal targets do not interact with forecasts.

**Related topics**  


[Performance Analytics targets and thresholds](pa-targets-thresholds.md)

## Forecasting with time series aggregations

If you apply a time series aggregation to an indicator, the forecast period length changes. The change depends on the type of the time series.

|Time aggregate|Effect on forecast period|Example|
|--------------|-------------------------|-------|
|Running|The number of points in the period is equal to the "range" field value.|For a 7-day running sum, the forecast period has 7 data points. For a 28-day running sum, it has 28 data points.|
|By period|The selected period is treated as if it were the indicator frequency.|A "By week" time aggregate applied to a daily indicator has 13 data points per forecast period, which is a quarter long. This forecast period is the same as for a weekly indicator with no time aggregate.|
|To date|The period length matches the time span of the aggregation. The number of data points per period is a product of this time span and the indicator frequency.|See the rest of this section.|

For an indicator with the Daily frequency, you have the following number of data points per period for to-date aggregations:

|Week to date|Month to date|Quarter to date|Year to date|
|------------|-------------|---------------|------------|
|7|30|91|365|

With one exception, indicators with non-daily frequencies support only year-to-date among to-date time aggregations. Monthly indicators are the exception. They also support quarter-to-date time aggregations. A monthly indicator with a quarter-to-date aggregation has three data points per period. The number of data points per forecast period for different indicator frequencies with year-to-date aggregations follows:

|Indicator frequency|Data points per period, year to date|
|-------------------|------------------------------------|
|Daily|365|
|Weekly|52|
|Four-weekly|13|
|Biweekly|26|
|Quarterly \(fiscal\)|4|

**Related topics**  


[Applying time series aggregations](applying-time-series-aggregations.md#)

## Displaying indicator score forecasts

In the classic environment, show the forecasts on a time series widget or the Analytics Hub. On a configurable workspace, show the forecasts on a time series data visualization or KPI Details.

To show the forecast on a time series widget, select **Show forecast** in the **Display Settings** section of the Widget form. You can also show the 95% confidence interval of the forecast, by selecting **Show forecast range**. For more information, see [Time series widgets](../reference/time-series-widgets.md).

To show the forecast on the Analytics Hub, click the chart settings icon \(![](../image/Cogwheel.png)\) and enable the **Forecast** option. Similarly, in KPI Details, open **Chart options** and enable **Forecast**.

To show the forecast in a time series data visualization, expand the Additional settings and turn on **Show forecast**. You have the option then to show the forecast range. You can override the forecast configuration for the indicator on this specific data visualization by opening **Configure forecast**.

To show the forecast for an indicator on KPI Details, turn forecasting on in the [Chart options in KPI Details](../../par-for-workspace/reference/chart-options.md).

**Related topics**  


[Additional settings for time series widgets](../reference/optional-settings-ts-widgets.md#)

[Analytics Hub for a specific indicator](view-scorecard.md)

[Indicator data options for time series data visualizations](../../reporting/reference/config-dv-time-series-ind-data.md)

[Examining indicators with KPI Details](../../par-for-workspace/reference/kpi-details-components.md)

