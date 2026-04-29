---
title: Using Performance Analytics with external data
description: Performance Analytics on external data sources enables you to perform detailed analysis on data that is not in your ServiceNow instance.Performance Analytics supports only the database formats that ServiceNow supports by default. If a customer adds a JDBC driver for an unsupported database format, Performance Analytics does not support that database format as an external data source.Create an external indicator to define what data to evaluate and the SQL statement used to determine the indicator score.Create an external breakdown to define what elements are available to break down external indicator scores.Associate an external indicator and external breakdown to define how to collect breakdown scores for the indicator.Test your external indicators and breakdowns to ensure you can connect to the external data source and collect the data you expect.When using Performance Analytics with external data you must filter SQL statements that collect scores by date.Certain Performance Analytics functionality is not available when you measure external data.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Using Performance Analytics with external data

Performance Analytics on external data sources enables you to perform detailed analysis on data that is not in your ServiceNow instance.

When you collect scores on external data, Performance Analytics stores scores and breakdown elements from the external data on your instance. The raw data being analyzed remains on the external data source and is not copied to your instance. This functionality enables you to analyze and share metrics without duplicating the underlying data.

Performance Analytics external data collection uses three types of configuration records:

-   An external indicator which specifies the JDBC data source and SQL statement used to collect scores.
-   An external breakdown which specifies the JDBC data source and SQL statement used to specify breakdown elements.
-   An external indicator breakdown which defines the relationship between an external indicator, and breakdown, and the SQL statement used to collect scores for each breakdown element for that indicator.

**Important:** These topics do not apply to external data accessed through Workflow Data Fabric tables. You can create an indicator or breakdown source for a Workflow Data Fabric table normally.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

## Supported database formats for external data

Performance Analytics supports only the database formats that ServiceNow supports by default. If a customer adds a JDBC driver for an unsupported database format, Performance Analytics does not support that database format as an external data source.

|SQL Server Type|Port|
|---------------|----|
|MySQL|3306|
|Microsoft SQL Server|1433|
|Oracle|1521|

**Related topics**  


[JDBC type data source](https://www.servicenow.com/docs/access?context=r_JDBCTypeDataSource&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

## Create an indicator for external data

Create an external indicator to define what data to evaluate and the SQL statement used to determine the indicator score.

### Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **External Indicators** and click **New**.

2.  Give the indicator a descriptive **Name**.

3.  In the **Frequency** field, specify the frequency of data points for the indicator, such as **Daily**, **Weekly**, or **Monthly**.

4.  In the **Source** tab, select a **Data Source** to collect scores from.

    Only JDBC type data sources are supported by Performance Analytics. Refer to the data sources documentation for information on setting up data sources.

    **Note:** The SQL Statement and Import set table defined in the data source are not used by Performance Analytics.

5.  Specify the **SQL Statement** to use to calculate the score value.

    The SQL statement must return an aggregate value with the alias **value**, and should filter data based on a date field.

    **Important:** The aggregate alias must be **value**.

    For a simple indicator, the SQL statement will be something like `SELECT count(*) AS value FROM... WHERE DATE(date_field) >= DATE(${start_at})`.

    For more complex indicators, you may also need a condition that DATE is earlier than the date that DATEADD returns. Here a monthly indicator with complex data has the SQL statement `SELECT count(*) AS value FROM... WHERE DATE(date_field) >= DATE(${start_at}) AND DATE(date_field) < DATEADD(month, 1, ${start_at})`.

6.  If you prefer that the score of this indicator increases or decreases over time, select **Maximize** or **Minimize** in the **Direction** field.

    Analytical tools and graphic displays use this **Direction** with this indicator.

    **Tip:** Set a direction whenever you can. All key indicators should be set to Maximize or Minimize.

    |Value|Use case|
    |-----|--------|
    |**Maximize**|Select if an increase in this indicator score is desired. For example, consider selecting **Maximize** for an indicator that shows revenue. Analytic tools and graphic elements reflect that an increase in this indicator score is good and a decrease is bad.|
    |**Minimize**|Select if a decrease in this indicator score is desired. For example, consider selecting **Minimize** for an indicator that shows costs. Analytic tools and graphic elements reflect that a decrease in this indicator score is good and an increase is bad.|
    |**None**|Select if the direction of change in this score doesn’t matter to your business.|

7.  Under Indicator properties, specify any of these properties:

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

The unit of measurement for the score, such as number, days, or percentages.To collect scores in the system reference currency on a Price, Currency, or FX Currency field, select **Use reference currency**. For more information, see [Indicator scores in reference currency](indicator-scores-reference-currency.md).

 If you select % or a time period as the unit, consider excluding some types of time series from being applied to the indicator. For more information, see [Exclude time series from an indicator](c_ExcludingTimeSeriesFromIndicators.md).

If you select Time as the unit, the time is given as Days, Hours, and Minutes. If the system property **glide.ui.duration.seconds.enabled** exists and is true, seconds are also displayed. In this case, seconds are also displayed for all-time fields on the instance and are included in exports to Microsoft Excel.

</td></tr><tr id="row_precision"><td>

Precision

</td><td>

The number of digits behind the decimal separator. For more information, see [Rounding and precision in indicators](r_FormulaRounding.md).This field isn’t available when the unit is **Use reference currency**. In this case, the precision is inherited from the reference currency.

</td></tr><tr><td>

Number format

</td><td>

The abbreviations used for large numbers, thousands through quintillions. For more information, see [Rounding and precision in indicators](r_FormulaRounding.md).

</td></tr></tbody>
</table>8.  In the **Access control** tab, set whether to save this indicator to the library and whether to limit the visibility of the indicator by user, group, or role.

    Activating **Show in library** means that the indicator will be available in the following places:

    -   The Platform Analytics indicator library
    -   KPI Details
    -   Analytics Hub, but only on upgraded instances that haven’t fully migrated to Platform Analytics
9.  In the **Other** tab, set various miscellaneous properties.

<table id="table_hft_ltv_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_default-time-series"><td>

Default time series

</td><td>

A predefined analytical function, like a 7-days running average, to apply to the indicator instead of showing the raw scores of the indicator.

 For more information, see [Applying time series aggregations](applying-time-series-aggregations.md#).

**Note:** You can’t set the default time series for an indicator that uses a business or fiscal calendar. These calendars do not support time series aggregations.

</td></tr><tr id="row_live-group-profile"><td>

Live group profile

</td><td>

Live Group Profile \[live\_group\_profile\] record for a Live Feed group. Specify a group profile to cause that group to get notifications about this indicator.

 For more information about this social application on the ServiceNow AI Platform, see [Live Feed](https://www.servicenow.com/docs/access?context=c_GetStartedWithLiveFeed&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr id="row_order"><td>

Order

</td><td>

Number indicating the order in which indicators are displayed in the Analytics Hub. Indicators with the lowest value are displayed at the top of the list. If no values are provided in the **Order** field, indicators are displayed from a to z using the **Name** field. To use the order field, you must enter order numbers for all indicators. If you put in numbers for only a few indicators, the order in which indicators are displayed reverts to a to z.

 Not used in Platform Analytics experience.

</td></tr><tr><td>

Default chart type

</td><td>

Set a default chart type \(line, column, spline, or area\) for this indicator. When opening the Analytics Hub or KPI Details for this indicator for the first time, the default chart type is used. If the chart type is changed in the Analytics Hub or KPI Details, that preference is remembered.

</td></tr><tr id="row_render-cont-lines"><td>

Render continuous lines

</td><td>

When selected, the Analytics Hub and KPI Details show unbroken data lines for this indicator, even when there’s no data for a specific date. This behavior may be useful when displaying datasets with varied starting dates or for data that aren’t regularly updated, such as stock information.

 Continuous lines aren’t rendered when a time series is set on the indicator or the Analytics Hub or KPI Details.

</td></tr><tr><td>

Show real-time score

</td><td>

When selected, the Analytics Hub and KPI Details can show the score of this indicator in real time, as well as the current state of associated records. Clear this check box when indicator data isn’t available in real time, such as in an integration that uses data from a third-party source. For more information, see [Real-time scores](real-time-scores.md).

 Note: A condition must be set on the indicator or the associated indicator source for real-time scores to be displayed.

</td></tr></tbody>
</table>    For example, in the Other tab you can configure an indicator as follows:

    -   By default, it shows a 30-day running sum of scores in widgets. You can override this default in the Analytics Hub, KPI Details, dashboard widgets, or workspace data visualization.
    -   The IT Live Group is notified of changes to the indicator.
    -   The indicator is listed third in the Analytics Hub list of indicators. All other indicators also have their position specified. This setting does not affect the order of indicators on KPI Details.
    -   The default chart type is Spline on KPI Details.
    -   Data lines for the indicator are shown unbroken, even when data is missing.
    -   KPI Details can show the score of this indicator in real time.
    ![The Other tab on an indicator with settings previously listed](../image/auto-ind-other-tab.png)

10. In the **Forecasting** tab, set the forecast method, the number of data collection periods to forecast, the amount of historical data to base the forecast on, and the upper and lower limits of forecast values.

    For more information, see [Performance Analytics scores forecasts](c_ForecastingData.md#).

11. Save the indicator.

12. Press **Test Collection**.

    This action tests the main query of the indicator.


### What to do next

If you want to collect breakdown scores for the indicator, define an external breakdown and associate it with the indicator.

## Create a breakdown using external data

Create an external breakdown to define what elements are available to break down external indicator scores.

### Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

### About this task

By default an external breakdown can contain a maximum of 5000 elements. This limit is controlled by the property **com.snc.pa.dc.max\_external\_elements**.

External breakdown elements are stored on the pa\_ext\_elements tables.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **External Breakdowns**.

2.  Click **New**.

3.  Select a **Data Source** that contains the records you want to use as [breakdown elements](performance-analytics-glossary.md#).

    Only JDBC type data sources are supported by Performance Analytics. Refer to the data sources documentation for information on setting up data sources.

    **Note:** The SQL Statement and Import set table defined in the data source are not used by Performance Analytics.

4.  Specify a **SQL Statement** to select the breakdown elements.

    The SQL Statement must return the unique key for each breakdown element with the alias **id** and the element display name with the alias **name**,such as `SELECT guid AS id, user_name AS name FROM...`.

    **Important:** The unique key alias must be **id** and the display name alias must be **name**.

5.  Save the breakdown.

6.  Press **Test Collection**.

    This action tests the query that selects the breakdown elements.


### What to do next

After defining how to collect breakdown elements, associate the external breakdown with one or more external indicators.

## Configure an external indicator to use an external breakdown

Associate an external indicator and external breakdown to define how to collect breakdown scores for the indicator.

### Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **External Indicators**.

2.  Select an indicator.

3.  In the **Breakdowns** related list, click **New**.

4.  Select the external **Breakdown** to apply to this indicator.

5.  In the **SQL statement** field, enter a SQL statement that calculates the score value for each breakdown element.

    The SQL statement should use the same aggregate function as the indicator SQL statement, such as COUNT. The SQL statement must return the aggregate value with the alias **value** and the breakdown element unique key with the alias **id**. The SQL statement must also group the data by the column that contains the breakdown element values.

    For example, `SELECT count(*) AS value, guid as id FROM... WHERE DATE(date_field) >= DATE({$start_at}) GROUP BY guid`

    **Important:** The aggregate alias must be **value** and the breakdown unique key alias must be **id**.

6.  Save your changes.

7.  Press **Test Collection**.

    This action tests the SQL statement that calculates the score value for the breakdown element.


### What to do next

Repeat the previous steps to add additional breakdowns to the indicator. Test the SQL statement after adding each one.

## Test external indicators and breakdowns

Test your external indicators and breakdowns to ensure you can connect to the external data source and collect the data you expect.

### Before you begin

Role required: pa\_admin, pa\_power\_user, or admin

### About this task

Test an indicator to test the query for that indicator and the queries for all breakdown elements. Test a breakdown to test the query used to determine available breakdown elements.

No scores or breakdown elements are saved when you test an indicator or breakdown.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **External Indicators** or **Performance Analytics** &gt; **External Breakdowns**.

2.  Select the indicator or breakdown that you want to test.

3.  Click the **Test** button.

    If the query runs successfully, the number of scores or breakdown elements that would be collected appears. If an error occurs during testing, the error message appears.


### What to do next

After confirming that all queries run successfully and return the data you expect, add the external indicator to a data collection job to begin collecting scores.

## Filtering external data by date

When using Performance Analytics with external data you must filter SQL statements that collect scores by date.

In indicator and indicator breakdown SQL statements, filter the query by date, such as `WHERE DATE(my_date_field) >= DATE(${start_at})`. It is not necessary to filter breakdown SQL statements by date as breakdown SQL statements collect only elements and not scores.

The variable $\{start\_at\} contains the date of the period being collected in the format YYYYMMDD. For daily indicators this value is always the date being collected. For indicators with longer collection frequencies, such as weekly or monthly, the date is the first day of the collection period. The date that the data collection job runs on does not affect this variable.

When you test an indicator or breakdown, the $\{start\_at\} variable is always set to the current date.

## Limitations when using Performance Analytics with external data

Certain Performance Analytics functionality is not available when you measure external data.

-   You cannot collect snapshots
-   You cannot view real-time scores
-   You cannot apply 2nd-level breakdowns
-   You cannot use widget visualizations that depend on 2nd-level breakdowns with external data. This includes pivot and heatmap visualizations.
-   Because snapshots are not available, you cannot view changes in collected records

