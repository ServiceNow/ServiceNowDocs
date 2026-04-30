---
title: Manual indicators
description: Manual indicators do not use scores collected from a database. Manual indicators are typically used for data that cannot be retrieved from the ServiceNow instance because it comes from an outside system, such as customer data from a third-party sales system.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Manual indicators

Manual indicators do not use scores collected from a database. Manual indicators are typically used for data that cannot be retrieved from the ServiceNow instance because it comes from an outside system, such as customer data from a third-party sales system.

## Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

## About this task

Manual indicators are not associated with an indicator source. Scores for manual indicators are not generated automatically by a data collection job. Instead, populate these indicators by adding scores to the scoresheet manually.

**Note:**

-   You must have a subscription for Performance Analytics to create indicators.
-   If you are using domain separation, the indicator is created in the domain that you are currently in.

## Procedure

1.  Use one of the following navigation paths:

    -   If you are on an upgraded instance that has not migrated to Platform Analytics, navigate to **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Manual Indicators** and select **New**.
    -   If you are on a new instance or have migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Manual Indicators** and select **New**.
2.  In the **Name** field, give the indicator a descriptive name, such as Number of Critical Incidents.

3.  In the **Frequency** field, select the frequency at which scores are set.

    The default value is **Daily**.

    **Note:** The frequency for a manual indicator specifies how to visualize its data. For example, if you set the data points per day or per month in the charts, the setting also affects the scoresheet, so it determines whether you can enter daily or monthly values.

4.  If you prefer that the score of this indicator increases or decreases over time, select **Maximize** or **Minimize** in the **Direction** field.

    Analytical tools and graphic displays use this **Direction** with this indicator.

    **Tip:** Set a direction whenever you can. All key indicators should be set to Maximize or Minimize.

    |Value|Use case|
    |-----|--------|
    |**Maximize**|Select if an increase in this indicator score is desired. For example, consider selecting **Maximize** for an indicator that shows revenue. Analytic tools and graphic elements reflect that an increase in this indicator score is good and a decrease is bad.|
    |**Minimize**|Select if a decrease in this indicator score is desired. For example, consider selecting **Minimize** for an indicator that shows costs. Analytic tools and graphic elements reflect that a decrease in this indicator score is good and an increase is bad.|
    |**None**|Select if the direction of change in this score does not matter to your business.|

5.  Specify any of these indicator properties:

<table id="table_uh3_vsv_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_key"><td>

Key

</td><td>

Identifies the indicator as a key indicator. Used only to filter the list of indicators in **Performance Analytics** &gt; **Analytics Hub**. Not used in Platform Analytics experience.

</td></tr><tr id="row_unit"><td>

Unit

</td><td>

The unit of measurement for the score, such as number, days, or percentages.To collect scores in the system reference currency on a Price, Currency, or FX Currency field, select **Use reference currency**. For more information, see [Indicator scores in reference currency](../concept/indicator-scores-reference-currency.md).

 If you select % or a time period as the unit, consider excluding some types of time series from being applied to the indicator. For more information, see [Exclude time series from an indicator](../concept/c_ExcludingTimeSeriesFromIndicators.md).

If you select Time as the unit, the time is given as Days, Hours, and Minutes. If the system property **glide.ui.duration.seconds.enabled** exists and is true, seconds are also displayed. In this case, seconds are also displayed for all time fields on the instance and are included in exports to Microsoft Excel.

</td></tr><tr id="row_precision"><td>

Precision

</td><td>

The number of digits behind the decimal separator. For more information, see [Rounding and precision in indicators](../concept/r_FormulaRounding.md).This field is not available when the unit is **Use reference currency**. In this case, the precision is inherited from the reference currency.

</td></tr><tr><td>

Number format

</td><td>

The abbreviations used for large numbers, thousands through quintillions. For more information, see [Rounding and precision in indicators](../concept/r_FormulaRounding.md).

</td></tr></tbody>
</table>6.  In the **Access control** tab, set whether to save this indicator to the library and whether to limit the visibility of the indicator by user, group, or role.

    Activating **Show in library** means that the indicator will be available in the following places:

    -   The list of KPIs in the Platform Analytics experience library
    -   KPI Details
    -   Analytics Hub, but only on upgraded instances that have not fully migrated to Platform Analytics
7.  In the **Access Control** tab, set which user is the **Contributor** authorized to populate the indicator scores.

    You can select only a user with the pa\_admin, pa\_power\_user or pa\_contributor role.

8.  In the **Other** tab, set various miscellaneous properties.

<table id="table_ert_z5v_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default time series

</td><td>

A predefined analytical function, like a 7-days running average, to apply to the indicator instead of showing the raw scores of the indicator.

 For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).

**Note:** You cannot set the default time series for an indicator that uses a business or fiscal calendar. These calendars do not support time series aggregations.

</td></tr><tr><td>

Live group profile

</td><td>

Live Group Profile \[live\_group\_profile\] record for a Live Feed group. Specify a group profile to cause that group to get notifications about this indicator.

 For more information about this social application on the ServiceNow AI Platform, see [Live Feed](https://www.servicenow.com/docs/access?context=c_GetStartedWithLiveFeed&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Value when nil

</td><td>

The value that is inserted as the score when no value is collected. This value applies only to the indicator score. It does not impact scores for breakdown elements.

</td></tr><tr><td>

Order

</td><td>

Number indicating the order in which indicators are displayed in the Analytics Hub. Indicators with the lowest value are displayed at the top of the list. If no values are provided in the **Order** field, indicators are displayed from a to z using the **Name** field. To use the order field, you must enter order numbers for all indicators. If you put in numbers for only a few indicators, the order in which indicators are displayed reverts to a to z.

 Not used in Platform Analytics experience.

</td></tr><tr><td>

Render continuous lines

</td><td>

When selected, the Analytics Hub and KPI Details show unbroken data lines for this indicator, even when there is no data for a specific date. This behavior may be useful when displaying data sets with varied starting dates or for data that are not regularly updated, such as stock information.

 Continuous lines are not rendered when a time series is set on the indicator or the Analytics Hub or KPI Details.

</td></tr></tbody>
</table>9.  In the **Forecasting** tab, set the forecast method, the number of data collection periods to forecast, the amount of historical data to base the forecast on, and the upper and lower limits of forecast values.

    For more information, see [Performance Analytics scores forecasts](../concept/c_ForecastingData.md#).


## What to do next

Create manual breakdowns and assign them to this indicator. Then, manually add scores.

**Related topics**  


[Manual breakdowns](../concept/manual-breakdowns.md#)

[Add or edit indicator scores manually](t_ManuallyAddingScoresForIndicators.md)

