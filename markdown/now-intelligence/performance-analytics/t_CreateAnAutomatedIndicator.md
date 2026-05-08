---
title: Create an automated indicator
description: To analyze the performance of a business process that is recorded in a ServiceNow table, use an automated indicator. If a suitable indicator is not provided in a Platform Analytics Solution, create a new one.After you create an automated indicator with the required settings, you can configure optional, advanced settings.Business and fiscal calendars do not have standard periods. Performance Analytics has introduced several innovations to accommodate these custom periods. Your workflow for creating indicators differs accordingly.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [Automated indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an automated indicator

To analyze the performance of a business process that is recorded in a ServiceNow table, use an automated indicator. If a suitable indicator is not provided in a Platform Analytics Solution, create a new one.

## Before you begin

**Note:** Before creating this indicator, check whether your instance supports Data Snapshots. If it does, see whether you can and want to create this indicator in Data Snapshots, which is simpler and allows unlimited breakdowns. For more information, see [Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md).

You must have a suitable indicator source, as explained in [Automated indicators](../concept/automated-indicators.md). You also should design your KPIs as part of a business strategy before you create them, as described in [Design your Performance Analytics solution with KPI Composer](../concept/designing-pa-solution.md) and [Planning your indicators](../concept/planning-indicators.md). Also familiarize yourself with the [Workflow for creating indicators](workflow-automated-indicators.md).

**Note:**

-   You must have a subscription for Performance Analytics to create indicators.
-   If you’re using domain separation, the indicator is created in the domain that you’re currently in.

Role required: pa\_power\_user, pa\_admin, or admin

## About this task

This form provides all the many options for creating an automated indicator. To create a simple automated indicator quickly, see [Create an automated indicator with a wizard](t_CrtIndctrIndctrWzrd.md#). However, for deeper information about indicator options and for tips, read this topic first.

## Procedure

1.  Use one of the following navigation paths:

    -   If you are on an upgraded instance that hasn’t migrated to Platform Analytics, navigate to **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** and select **New**.
    -   If you are on a new instance or have migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Automated Indicators** and select **New**.
2.  In the **Name** field, give the indicator a descriptive name, such as Number of Critical Incidents.

3.  Add a meaningful **Description** to help other users understand the purpose of this indicator.

4.  Scroll to Indicator properties.

5.  If you prefer that the score of this indicator increases or decreases over time, select **Maximize** or **Minimize** in the **Direction** field.

    Analytical tools and graphic displays use this **Direction** with this indicator.

    **Tip:** Set a direction whenever you can. All key indicators should be set to Maximize or Minimize.

    |Value|Use case|
    |-----|--------|
    |**Maximize**|Select if an increase in this indicator score is desired. For example, consider selecting **Maximize** for an indicator that shows revenue. Analytic tools and graphic elements reflect that an increase in this indicator score is good and a decrease is bad.|
    |**Minimize**|Select if a decrease in this indicator score is desired. For example, consider selecting **Minimize** for an indicator that shows costs. Analytic tools and graphic elements reflect that a decrease in this indicator score is good and an increase is bad.|
    |**None**|Select if the direction of change in this score doesn’t matter to your business.|

6.  Scroll to the **Source** tab and select an **Indicator Source**.

    Entering a partial name in the field filters the list of available indicator sources accordingly.

    If you are using domain separation, you can select only indicator sources to which you have visibility.

7.  In the **Aggregate** field of the **Source** tab, select the aggregate function to apply to the data from the indicator source.

    **Count** counts the number of records. **Count distinct** counts the number of unique values rather than the total number of records. For example, if the name of a user appears more than once in a list, the user is only counted once. Other choices perform the specified aggregate operation, such as summing the values in a field across records.

    If you select a Sum, Minimum, or Maximum aggregate, consider excluding some types of time series from being applied to the indicator. For more information, see [Exclude time series from an indicator](../concept/c_ExcludingTimeSeriesFromIndicators.md).

    **Tip:** Try to avoid using the Average aggregate, because that aggregate can complicate the use of time series. Instead, create a Sum automated indicator and a Count automated indicator. Then create a formula indicator that divides the Sum indicator by the Count indicator to calculate the average.

8.  Complete any remaining fields in the Source tab.

    If the **Aggregate** is set to **Count**, only the **Collect records** and **Value when nil** fields are available.

<table id="table_o41_btv_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Collect records

</td><td>

Check box to indicate if the individual record sys\_ids are stored when the indicator is collected. Selecting this check box enables you to drill down to those details in the Analytics Hub and widgets. When available, collected records appear on the **Records** tab.

**Tip:** Generally avoid collecting records with aggregates other than Count and Sum. Users rarely want to see the records that go into a Min or Max, and the number of records in a Count Distinct may differ from the score. Consider collecting records for indicators with these other aggregates only if a user asks for them.

 You must enable this option for the main indicator of a Spotlight group. Otherwise, the Spotlight group can’t evaluate a snapshot of collected records. For more information, see [Evaluating a snapshot or platform data](create-spotlight-group.md#).

</td></tr><tr><td>

Scripted

</td><td>

A check box to indicate if the value should be aggregated based on a script. This option is available only if **Aggregate** isn’t set to **Count**. Clear the **Scripted** check box to aggregate the values in a field.

</td></tr><tr><td>

Field

</td><td>

The field to perform the aggregate operation on. This field appears only if **Aggregate** isn’t **Count** and **Scripted** isn’t selected.

</td></tr><tr><td>

Script

</td><td>

Select a script or create a script for the aggregation. This option is available only if the **Scripted** check box is selected.For more information, see [Scripting in Performance Analytics](../concept/pa-scripts.md#).

</td></tr><tr><td>

Value when nil

</td><td>

The value that is inserted as the score when no value is collected. This value is inserted whether or not breakdowns are applied.This value isn’t used to calculate formulas or aggregates, such as an average.

</td></tr></tbody>
</table>    For example, the indicator Summed age of open incidents uses the Sum aggregate. Because it uses this aggregate, it must have either a field or a script specified. In this case, it’s scripted and uses the Incident.Age.Hours script.

    ![The Incident.Age.Hours script on the Summed age of open incidents indicator](../image/auto-ind-scripted.png)

9.  Expand the context menu and select **Save**.

    ![Save option in the context menu](../image/auto-indicator-save.png)

10. Set the periodicity of the indicator if you’re prompted to do so after saving.

    You’re prompted to set the periodicity only in the following circumstances:

    -   The indicator source for this indicator uses a business or fiscal calendar.
    -   This indicator is the first one that uses that calendar.
    These settings apply to all indicators with the same calendar frequency, unless you override the settings in the **Collection periods** tab. For more information, see the section "Indicators with business calendars."

    1.  In the Related Links section, select **Configure periodicity**.

        A PA Business Calendar Retention Period record opens.

    2.  In the **Number of entries to establish seasonality** field, enter the number of time periods, as defined in the business calendar or schedule entries, that are necessary to find seasonal patterns.

        For more information about business calendar entries, see Creating business calendars.

    3.  Set the number of time periods, as defined in the business calendar or schedule entries, to retain scores and snapshots.

        A default value of one is provided, but you should consider changing it.

11. In the **Jobs** related list, select jobs that support your indicator source.

    Usually you have one Historic job and one update job that matches the indicator frequency, such as \[PA Incident\] Historic Data Collection and \[PA Incident\] Daily Data Collection. These jobs support the Incidents.\* data sources.

12. Perform one of the following procedures:

    -   If no prompts appear to take further action and the indicator meets your requirements, press **Manage Breakdowns** to add breakdowns to your indicator. For more information, see [Assign and map breakdowns](create-breakdown-mapping.md#)
    -   If you are prompted to take further action or you have designed a more elaborate indicator, complete the advanced indicator settings.

**Parent Topic:**[Automated indicators](../concept/automated-indicators.md)

**Previous topic:**[Automated indicators](../concept/automated-indicators.md)

**Next topic:**[Assign and map breakdowns](create-breakdown-mapping.md#)

**Related topics**  


[Create an indicator group](t_CreatingIndicatorGroups.md)

[Collect and manage a matrix of breakdowns](create-breakdown-mapping.md#)

## Advanced indicator settings

After you create an automated indicator with the required settings, you can configure optional, advanced settings.

### Before you begin

You have created and saved an automated indicator.

Role required: pa\_power\_user

### Procedure

1.  Under Indicator properties, specify any of these properties:

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

If you select Time as the unit, the time is given as Days, Hours, and Minutes. If the system property **glide.ui.duration.seconds.enabled** exists and is true, seconds are also displayed. In this case, seconds are also displayed for all-time fields on the instance and are included in exports to Microsoft Excel.

</td></tr><tr id="row_precision"><td>

Precision

</td><td>

The number of digits behind the decimal separator. For more information, see [Rounding and precision in indicators](../concept/r_FormulaRounding.md).This field isn’t available when the unit is **Use reference currency**. In this case, the precision is inherited from the reference currency.

</td></tr><tr><td>

Number format

</td><td>

The abbreviations used for large numbers, thousands through quintillions. For more information, see [Rounding and precision in indicators](../concept/r_FormulaRounding.md).

</td></tr></tbody>
</table>2.  In the **Additional Conditions** tab, add conditions to limit the set of records that the indicator evaluates.

    The conditions in the indicator apply in addition to the conditions in the indicator source.

    For real-time scores to be displayed, a condition must be set in the indicator or indicator source.

    For more information, see [Conditional filters and operators for indicators and breakdowns](../concept/condition-operators-ind-bkdowns.md).

3.  In the **Access control** tab, set whether to save this indicator to the library and whether to limit the visibility of the indicator by user, group, or role.

    Activating **Show in library** means that the indicator will be available in the following places:

    -   The Platform Analytics indicator library
    -   KPI Details
    -   Analytics Hub, but only on upgraded instances that haven’t fully migrated to Platform Analytics
4.  In the **Other** tab, set various miscellaneous properties.

<table id="table_hft_ltv_q2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_default-time-series"><td>

Default time series

</td><td>

A predefined analytical function, like a 7-days running average, to apply to the indicator instead of showing the raw scores of the indicator.

 For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).

**Note:** You can’t set the default time series for an indicator that uses a business or fiscal calendar. These calendars do not support time series aggregations.

</td></tr><tr id="row_live-group-profile"><td>

Live group profile

</td><td>

Live Group Profile \[live\_group\_profile\] record for a Live Feed group. Specify a group profile to cause that group to get notifications about this indicator.

 For more information about this social application on the ServiceNow AI Platform, see Live Feed.

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

When selected, the Analytics Hub and KPI Details can show the score of this indicator in real time, as well as the current state of associated records. Clear this check box when indicator data isn’t available in real time, such as in an integration that uses data from a third-party source. For more information, see [Real-time scores](../concept/real-time-scores.md).

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

5.  In the **Collect breakdown matrix fields** tab, you can enable second-level breakdowns for the indicator, such as Open Incidents by Category by Priority.

    Enabling second-level breakdowns can significantly impact performance. For more information, see [Collect and manage a matrix of breakdowns](create-breakdown-mapping.md#).

6.  In the **Collection periods** tab, override the properties that set the maximum number of periods prior to today for which scores and snapshots are collected and kept.

7.  In the **Forecasting** tab, set the forecast method, the number of data collection periods to forecast, the amount of historical data to base the forecast on, and the upper and lower limits of forecast values.

    For more information, see [Performance Analytics scores forecasts](../concept/c_ForecastingData.md#).

8.  In the **Statistics exclusion** tab, select any statistics that you do not want to show on KPI Details or the Analytics Hub.

    For example, you might not want to show the Change % for an indicator with a percentage unit.

9.  Press **Manage Breakdowns**.

    If you also see a button to **Enable data snapshots**, your instance supports unlimited breakdowns. For more information, see [Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md).


## Indicators with business calendars

Business and fiscal calendars do not have standard periods. Performance Analytics has introduced several innovations to accommodate these custom periods. Your workflow for creating indicators differs accordingly.

**Important:** The **Create New** indicator creation wizard does not support indicators based on business or fiscal calendars.

### Differences in how periods are defined

Unlike the standard calendar, business calendars have custom periods based on business calendar entries. To accommodate this difference, the following properties are defined differently on indicators that use business or fiscal calendars:

-   The indicator frequency is derived from the business calendar instead of from a static list of choices. The Frequency column of the indicator record is ignored. Instead, the Calendar frequency column is used.
-   For forecasting, you have to specify the number of periods that are needed to find seasonal patterns. This value cannot be determined automatically from the calendar period, like for standard calendars. You set this value for each calendar frequency, in PA Business Calendar Retention Periods \[pa\_calendars\_retention\] records.
-   You have to set the number of calendar periods to retain scores and [snapshots](../concept/performance-analytics-glossary.md#). The system properties that set the default numbers of calendar periods for retaining data are ignored. Instead, set these numbers for each calendar frequency in PA Business Calendar Retention Periods records.

### PA Business Calendar Retention Periods records and overriding them

When you first create an indicator that uses a particular calendar frequency, you are prompted to complete a PA Business Calendar Retention Periods record. Any indicators you make in the future with that calendar frequency use the same PA Business Calendar Retention Periods record.

You can override the settings in a PA Business Calendar Retention Periods record for a specific indicator. Override the defaults in the **Collection periods** tab of the indicator record, the same as for standard calendar indicators. However, when you first select **Override retention periods**, you see the default retention periods for a Daily indicator with a standard calendar. These values are display artifacts only and you can ignore them. Put in the values you want, and they will override the PA Business Calendar Retention Periods record values.

**Note:** You cannot override the **Number of entries to establish seasonality** value from the PA Business Calendar Retention Periods record.

### Business calendar groups

When you select an entry in the **Calendar** field other than the standard calendar, you actually select a business or fiscal calendar group. Both business and fiscal calendar groups are listed under **Business calendar** &gt; **Business Calendar Groups**. Each business or fiscal calendar group contains a set of business calendars, which you select under **Calendar frequency**. Each business calendar in turn contains a set of either business calendar or schedule entries, for business and fiscal calendars, respectively.

The process for generating a fiscal calendar automatically creates a fiscal calendar group. For business calendars, the creator of the business calendar must also create the business calendar group, manually. If you have any questions, contact the admin responsible for creating business calendars. For more information, see Create a Business Calendar Group.

### Automated indicators in formulas

A formula indicator can include [automated indicators](../concept/performance-analytics-glossary.md#) that use business calendars. The formula indicator must use the same business calendar as at least one of the contributing automated indicators. For more information, see [Create a formula indicator](t_CreateAFormulaIndicator.md).

