---
title: Usage Insights data options for pivot table data visualizations
description: When you select a Usage Insights data source for a pivot table visualization, the following Data configuration options are available.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Pivot table visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Usage Insights data options for pivot table data visualizations

When you select a Usage Insights data source for a pivot table visualization, the following Data configuration options are available.

**Important:** Pivot table visualizations are only suitable for Events data, not Users or Sessions. Only Events have a value to group by.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" id="heading-data" colspan="2">

Data

</td></tr><tr><td>

Data source

</td><td>

You have selected a Usage Insights data source in [Create a pivot table data visualization in the Visualization Designer](../task/create-dv-pivot-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

Metric

</td></tr><tr><td>

Metric

</td><td>

Label of the metric. By default it is the same as the name of the data source: Events or Sessions.For sessions, you can configure the metric to reflect the number of sessions, average session duration, average pages per session, or average sessions per user.

</td></tr><tr><td>

Format values

</td><td id="entry_format-values">

Select to open the **Formatting values** dialog. For more information, see [Value formatting in reports](value-formatting-reports.md#).

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Columns

</td><td>

Properties of the Usage Insights data source.

**Note:** Available only for Events and Sessions metrics, in which case it is mandatory.

</td></tr><tr><td>

Rows

</td><td>

Hierarchy of table fields with values displayed horizontally.

</td></tr><tr><td>

Event property

</td><td>

Choice of properties of the data source to select for a column or row.

</td></tr><tr><td>

Show row total

</td><td>

Show the total value of elements in each row.

</td></tr><tr><td>

Show column total

</td><td>

Show the total value of elements at the bottom of each column.

</td></tr><tr><td>

Show parent row totals

</td><td>

For a hierarchy of rows, show the total of all child rows per column, depending on metric aggregation.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show 0 when no data is available

</td><td>

When toggled on, shows empty \(NULL\) values as zero \(0\). Default is true.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon

</td><td>

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Refresh after being away for X min.

</td><td>

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td class="sub-head" colspan="2">

Info messages

</td></tr><tr><td>

Set custom message when no data

</td><td>

Option to configure a custom message that displays when no data is returned.

</td></tr><tr><td>

Illustration

</td><td>

An illustration to include in the message.

</td></tr><tr><td>

Heading

</td><td>

Header text of the message that describes why no data was returned.

</td></tr><tr><td>

Heading level

</td><td>

Header text size for the message that describes why no data was returned.

</td></tr><tr><td>

Content

</td><td>

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment

</td><td>

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>**Parent Topic:**[Create a pivot table data visualization in the Visualization Designer](../task/create-dv-pivot-ac.md)

