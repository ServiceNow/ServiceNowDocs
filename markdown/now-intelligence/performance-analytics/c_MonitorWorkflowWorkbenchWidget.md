---
title: Monitor a workflow with a workbench process widget
description: A workbench process widget is a collection of indicators that tell a story. The widget enables you to analyze multiple facets of multiple indicators on one screen without drilling down. This widget is useful when you want to monitor a process or service that has a workflow.Create a workbench widget to monitor a process using multiple indicators.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Monitor a workflow with a workbench process widget

A workbench process widget is a collection of indicators that tell a story. The widget enables you to analyze multiple facets of multiple indicators on one screen without drilling down. This widget is useful when you want to monitor a process or service that has a workflow.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

You choose the main indicators on the top of the widget. Optionally, each main indicator can have a unique set of supporting indicators.

The widget has four interconnected sections that dynamically update. For example, when you click a main indicator its score, trend, supporting indicators, and breakdown information appear. Click or select a date on any visualization and the entire widget displays data for that day.

**Note:**

-   If real-time scores are supported for the main indicator and its applied breakdowns, you can view real-time scores. To view real-time scores, select **Real-time** in the date selector. Real-time scores are displayed only in the top pane of the workbench. For more information, see [Real-time scores](real-time-scores.md).
-   The timespan that the widget shows for each score trend depends on the frequency of the indicator. The timespans are: 60 days for daily, one year for weekly and monthly, three years for quarterly, and 12 years for yearly. You cannot set this time span. However, applying a time series aggregation in the widget changes the time span accordingly.

![Shows the different sections of the workbench process widget.](../image/WorkbenchProcessWidget.png "Workbench process widget")

The bottom section of the workbench process widget displays either available breakdowns or collected records for the selected indicator. Click the **Breakdowns** or **Records** tabs to display one or the other. If you select a supporting indicator that specifies an aggregate, such as the average age of open incidents, the **Records** tab is hidden.

When you create a workbench widget, you choose only main and supporting indicators. The score, trend, and breakdown sections of the widget are automatically configured and cannot be changed. However, you can change the order and appearance of indicators on the widget.

## Create a workbench process widget

Create a workbench widget to monitor a process using multiple indicators.

### Before you begin

-   Familiarize yourself with the structure of the workbench widget
-   Decide which main and supporting indicators to include
-   Role required: pa\_admin, pa\_power\_user, or admin

### Procedure

1.  Navigate to **All** &gt; **Performance Anaytics** &gt; **Widgets** and click **New**.

    A new widget record appears.

2.  **Name** the widget.

3.  In the **Type** field, select **Workbench**.

4.  Right-click the form header and select **Save**.

    The Main Widget Indicators related list appears.

5.  Add a main indicator to the workbench widget.

    Main indicators appear on the top of the widget. The maximum number of indicators you can add is specified in `com.snc.pa.widget.max_widget_indicators`. The default maximum number of widget indicators is seven.

    1.  Click **New** in the Main Widget Indicators related list.

    2.  Select an **Indicator**.

    3.  Set the **Order** to define where the indicator appears \(from let to right\).

    4.  Fill in other fields, as appropriate.

<table id="table_fgv_zdw_pt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown and Element

</td><td>

A breakdown element filters the data that appears in the indicator. If you select a breakdown you must select an element.

 For example, if your indicator is **Number of open Incidents** and you select **Breakdown** for **State** and **Active** for **Element**, only scores for incidents in the active state are included in the widget.

</td></tr><tr><td>

2nd Breakdown and Element

</td><td>

Adds a second breakdown element that filters the data that appears in indicator. If you select a 2nd breakdown you must select an element.

 For example, imagine your indicator is **Number of open incidents** and the first breakdown filters for active state. You then select **Category** for **2nd Breakdown** and **Software** for **Element**. The indicator will now display only scores for open incidents that are active and in the software category.

</td></tr><tr><td>

Time series

</td><td>

Adds the specified time period and aggregation to the widget's trend visualization.**Note:** Business and fiscal calendars do not support time series aggregations. You cannot set a time series aggregation for an indicator that uses such a calendar.

</td></tr><tr><td>

Follow element

</td><td>

Specifies that a breakdown element applied to the dashboard where the widget is added also applies to the indicator.

 If you specify a 2nd Breakdown, Follow element is ignored.

 **Warning:** Workbench widgets do not support multiple element selection on breakdown dashboards. If you select multiple elements on a breakdown dashboard with this widget, the widget ignores your selection.

 For more information, see [Configure widgets for breakdown dashboards](../task/set-up-widgets-for-breakdown-dashboards.md).

</td></tr><tr><td>

Followed breakdown

</td><td>

Specifies that only this breakdown applies to the indicator as a **Follow element**. All other breakdowns applied to a dashboard where the widget has been added will be ignored.

 If you do not specify a **Followed breakdown** all breakdowns applied to the dashboard will apply to the indicator.

</td></tr><tr><td>

Label

</td><td>

Specifies the name of the indicator on the widget. If you do not specify a Label, the name of the indicator is used.

</td></tr></tbody>
</table>    5.  To add supporting indicators, right-click the form header and select **Save**.

        Clicking **Save** instead of the **Submit** button saves the widget indicator but keeps the form open. The Supporting Widget indicators list appears at the bottom of the form after saving.

6.  Add supporting indicators to a main indicator.

    When you click a main indicator, its supporting indicators appear in the middle of the widget. You can add an unlimited number of supporting indicators.

    1.  If you are on the Widgets form, navigate to the **Main Widget Indicators** related list and open the **Widget Indicator** form for the main indicator that you want supporting widgets for.

        To open the **Widget Indicator** form, select the info icon ![Info icon](../../reporting/image/icon-info.png) for the main indicator, which opens a preview. Then select **Open Record** in the preview.

    2.  Click **New** in the **Supporting Widget Indicators** related list.

    3.  Select an **Indicator**.

    4.  Set the **Order** to define where indicator appears \(from left to right\).

    5.  Fill in other fields, as appropriate.

        You can configure supporting indicators the same way as main indicators. See step 5 for configuration options.

    6.  Click **Submit** to return to the Main Indicator record.

    7.  Repeat step 6 until you have added all supporting indicators.

7.  Click **Update**to return to the widget record.

8.  Repeat steps 5 - 7 until you have added all indicators.

9.  Select one of the main indicators as the **Default indicator**.

    This default indicator appears automatically when a user views the widget. If you do not specify a default indicator, the widget displays the main indicator with the lowest **Order** value first.

10. Click **Update** to save the widget.


### What to do next

Review the widget to ensure that the new indicators are correct. If you have not already, add the widget to a dashboard to view it.

