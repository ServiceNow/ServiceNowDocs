---
title: Indicator data options for funnel visualizations
description: When you select an indicator data source for the funnel visualization, the following data configuration options are available.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a funnel visualization, Data visualization in ITOM, AIOps Dashboards in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Indicator data options for funnel visualizations

When you select an indicator data source for the funnel visualization, the following data configuration options are available.

You can either select a single indicator and use the **Group by** field to calculate stage values, or select multiple indicators without a breakdown, where each indicator’s value represents a funnel stage.

<table id="table_rpg_zw3_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown

</td><td>

Provides a way to segment data using fields like Alert Severity or Alert Status. Each condition includes a **Breakdown** field, an **Operator**, and an **Element** that defines the target value. All conditions are applied using AND logic, meaning data must meet every specified criterion to be included in the visualization.

</td></tr><tr><td class="sub-head" colspan="2">

Header and border

</td></tr><tr><td>

Show header

</td><td>

Option for visibility setting for the widget header.

</td></tr><tr><td>

Show header separator

</td><td>

Option to display a dividing line below the header.

</td></tr><tr><td>

Chart title

</td><td>

Text shown as the title of the chart.

</td></tr><tr><td>

Description

</td><td>

Optional explanatory text shown below the title.

</td></tr><tr><td>

Wrap title

</td><td>

Option to wrap long titles onto multiple lines.

</td></tr><tr><td>

Show border

</td><td>

Option for border visibility setting for the widget container.

</td></tr><tr><td>

Header background color

</td><td>

Background color setting for the header area.

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Data sources

</td><td>

Available inputs that supply data to the visualization.

</td></tr><tr><td colspan="2">

Metric

</td></tr><tr><td>

Label

</td><td>

Custom name for the selected metric. By default, the label matches the data source name.

</td></tr><tr><td>

Select an aggregation

</td><td>

Aggregation type applied to the metric \(e.g., sum, average\). The default is Count, which displays the number of records selected.**Note:** Select **Count Distinct** to count only unique records. For example, when generating a report of users with one or more roles from a list, you count each user only once. Without this option, users with multiple roles are counted more than once.

</td></tr><tr><td>

Field

</td><td>

Source field from the data set for the selected metric.**Note:** The data appears in a format that matches the field type. For example, an integer field like **Priority** is shown as a number. A duration field like **Business duration** from the \[Incident\] table is displayed in days, hours, and minutes.

If function fields were created in Report Designer for the table, they are available in the drop-down list. For more information, see [Report on function fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/function-fields-reporting.md).

</td></tr><tr><td>

Format values

</td><td>

Formatting style for displaying metric values. Select to open the Formatting values dialog.For more information, see [Value formatting in reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/value-formatting-reports.md).

</td></tr><tr><td colspan="2">

Group

</td></tr><tr><td>

Field for incident

</td><td>

Field used specifically to group incident data.

</td></tr><tr><td>

Max number of groups

</td><td>

Limit on the number of groups shown in the visualization.

</td></tr><tr><td>

Show others

</td><td>

Option to group excess data into an **Others** category.

</td></tr><tr><td colspan="2">

Data update

</td></tr><tr><td>

Follow filter

</td><td>

Follows filters set at the page level. When selected, the visualization reflects workspace filters. When not selected, the visualization ignores all page-level filters.

</td></tr><tr><td>

Show filter icon

</td><td>

Option to display the filter icon and the number of filters affecting the visualization. If the check box is not selected, the icon and filter count are hidden.

</td></tr><tr><td>

Refresh after being away for X min

</td><td>

Trigger based on time spent away from the dashboard within the same workspace, including the Platform Analytics experience. Defines the number of minutes after which the visualization automatically refreshes when you return.Do not confuse this setting with **Scheduled repetition** on inline dashboards, which refreshes the entire dashboard only while it remains open.

</td></tr><tr><td colspan="2">

Info messages

</td></tr><tr><td>

Set custom message when no data

</td><td>

Custom text displayed when no data is available for the visualization.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr><td>

Set color type

</td><td>

Color scheme applied to different data values or ranges.

</td></tr><tr><td>

Chart interaction

</td><td>

User actions supported within the chart, such as hover or select.

</td></tr></tbody>
</table>**Parent Topic:**[Create a funnel visualization](../task/create-funnel-visualization.md)

