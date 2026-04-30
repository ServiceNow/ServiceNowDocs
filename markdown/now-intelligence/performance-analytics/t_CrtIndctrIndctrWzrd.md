---
title: Create an automated indicator with a wizard
description: Quickly create a Performance Analytics automated indicator with breakdowns, widgets, and data collection jobs for that indicator. You still need to be trained in Performance Analytics and to have planned your KPIs to use this wizard.There are several options for creating widgets to display the indicator data when creating an indicator and related records. You can create any or all of the available widget types.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an automated indicator with a wizard

Quickly create a Performance Analytics automated indicator with breakdowns, widgets, and data collection jobs for that indicator. You still need to be trained in Performance Analytics and to have planned your KPIs to use this wizard.

## Before you begin

Familiarize yourself with [Performance Analytics concepts](../concept/c_PerformanceAnalytics.md) and create indicators only as part of an analytics strategy. Plan your KPIs with [KPI Composer](../concept/designing-pa-solution.md). Study the [Workflow for creating indicators](workflow-automated-indicators.md).

Ensure that there is at least one indicator source and a data collection job for the indicator source facts table.

**Warning:** The wizard does not support the creation of indicators with business or fiscal calendars.

Role required: pa\_contributor, pa\_data\_collector, pa\_power\_user, or pa\_admin

## About this task

These instructions are for using a wizard to create a simple automated indicator quickly. If you need access to the full range of indicator parameters, see [Create an automated indicator](t_CreateAnAutomatedIndicator.md#).

**Note:** If you are using domain separation, the indicator is created in the domain that you are currently in.

## Procedure

1.  Navigate to **Indicators** &gt; **Create New**.

2.  Fill in the **General** tab.

<table id="table_zx3_tsp_vgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator name

</td><td>

A descriptive name, such as `Average number of open incidents`.

</td></tr><tr><td>

Description

</td><td>

An optional text description of the indicator. Can include purpose and internal logic. Descriptions can help you and other users remember the purpose of an indicator.

</td></tr><tr><td>

Direction

</td><td>

Select one of the following:-   **None**: The indicator has no preferred trend up or down.
-   **Minimize**: The indicator score should decrease over time.
-   **Maximize**: The indicator score should increase over time.


</td></tr><tr><td>

Unit

</td><td>

The unit of the score of the indicator. Possible units include:-   **\#**: Simple number \(default\)
-   **$**: Dollars
-   **%**: Percent


</td></tr><tr><td>

Group

</td><td>

The indicator group to which the indicator belongs, if any.

</td></tr></tbody>
</table>3.  Click **Next** and fill in the **Data Source** tab.

<table id="table_p33_hvp_vgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator Source

</td><td>

A selection of the available indicator sources. An indicator source is a data source that refers to a ServiceNow AI Platform table and one or more conditions that filter the records on that table. After you select the source, you can select **Preview records for this indicator source**.If you are using domain separation, you can select only indicator sources to which you have visibility.

</td></tr><tr><td>

Aggregate

</td><td>

The aggregate function to apply when calculating the indicator on the indicator source. **Count** counts the number of records. **Count distinct** counts the number of unique values rather than the total number of records. For example, if the name of a user appears more than once in a list, the user is only counted once. Other choices perform the specified aggregate operation, such as summing the values in a field across records.

</td></tr><tr><td>

Field/Script

</td><td>

For any aggregate other than **Count**, you must specify either a field in the table that the indicator source uses, or a script. The aggregate function applies to either the value in the field or the value that the script returns.

</td></tr><tr><td>

Conditions

</td><td>

An optional list of values and operations to apply to fields in the table that the indicator source uses. These conditions stack with any conditions that are specified in the indicator source.Several limitations exist for conditions on indicators. For more information, see the step for adding additional conditions in [Create an automated indicator](t_CreateAnAutomatedIndicator.md#).

</td></tr></tbody>
</table>4.  In the **Breakdowns** tab, select which of the available breakdowns to apply to this indicator.

    For two levels of breakdown to apply, also select **Collect breakdown matrix**.

5.  In the **Data Collection** tab, select the data collection job that will collect scores for this indicator.

    Scores will be collected depending on the schedule of the job. You can also run the job manually.

6.  To collect scores from the past and create a trend, select **Collect data from the past** and specify the time period.

    This job runs only once, when you create the indicator. Not all indicators allow retrospective score collection. As an alternative, manually associate a Historical data collection job with the indicator and run it.

7.  In the **Widgets** tab, select any combination of time series, last score, and breakdown widgets to create.

    You can also put the widgets in the tab of an existing dashboard. For more information about creating and displaying widgets from this wizard, see [Indicator creation widget options](t_CrtIndctrIndctrWzrd.md#).

8.  In the Summary tab, review the changes, then click **Apply**.

    The indicator is created and linked to the selected indicator source, breakdowns, and data collection job. Any widgets associated with the indicator are created and added to the specified dashboard tab.

9.  Click **Create another indicator** to restart the process with a new indicator.


## What to do next

If the data collection job is configured to collect scores from the past, a temporary data collection job with a **Run** value of **Once** is created. You can delete this job record after the job runs.

**Related topics**  


[Create an automated indicator](t_CreateAnAutomatedIndicator.md#)

[Indicator sources](../concept/c_IndicatorSources.md#)

[Collecting indicator scores](../concept/c_ClctData.md)

## Indicator creation widget options

There are several options for creating widgets to display the indicator data when creating an indicator and related records. You can create any or all of the available widget types.

<table id="table_brb_hj1_3s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2" align="center">

Time series widget options

</td></tr><tr><td>

Time series widget

</td><td>

Select this check box to create a time series widget to display the indicator data.

</td></tr><tr><td>

Time series

</td><td>

Runs a function on the indicator scores for a specific time period, such as a 7-day sum or average. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr><tr><td>

Visualization

</td><td>

Select the chart type to use to display the data, such as **Line** or **Column**.

</td></tr></tbody>
</table><table id="table_latest-score"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Latest score widget

</td><td>

Select the check box to create a score widget with a **Visualization** value of **Latest Score** to display the indicator data.

</td></tr><tr><td>

Time series

</td><td>

Runs a function on the indicator scores for a specific time period, such as a 7-day sum or average. For more information, see [Applying time series aggregations](../concept/applying-time-series-aggregations.md#).**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation on a widget for an indicator that uses such a calendar.

</td></tr><tr><td>

Periods back

</td><td>

Select the number of periods to compare the score with. For example, if the **Time series** is **By week SUM**, enter a **Periods back** value of **4** to compare the current score with scores from the past 4 weeks.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Breakdown widgets|Select this check box to create a breakdown widget with a scorecard visualization for each breakdown applied to this indicator.|

|Field|Description|
|-----|-----------|
|Put the widgets on a new tab on dashboard|Select a dashboard you want to add these widgets to. If you do not select a dashboard, widget records are created but they are not added to any dashboard.|
|New tab name|Enter a name for the new tab created to display these widgets. This field is required if you select a dashboard.|

**Related topics**  


[Performance Analytics widgets](../concept/c_Widgets.md)

