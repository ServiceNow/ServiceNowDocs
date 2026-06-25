---
title: Multiple data sources
description: Some visualization types support multiple data sources, while others do not. If your data visualization supports multiple data sources, the data sources must all be of the same type: all tables, all indicators, or all another type. Here's a simple example of a report based on the Indicator and Problem tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/multiple-data-sources.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Selecting data sources, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Multiple data sources

Some visualization types support multiple data sources, while others do not. If your data visualization supports multiple data sources, the data sources must all be of the same type: all tables, all indicators, or all another type.

|Visualization type|Multiple data source support|
|------------------|----------------------------|
|All time series \(line, column, spline, area, and others\)|Supported|
|All scores \(single score, dial, gauge\)|Not supported|
|All bars \(horizontal, vertical, Pareto\)|Supported|
|Heatmap|Not supported|
|Pies and donuts|Not supported|
|Pivot table|Supported|
|Bubble|Supported|
|Boxplot|Not supported|
|Calendar report|Not supported|
|Geomap|Not supported|
|Indicator scorecard|Not supported|
|Analytics list|Not supported|

**Warning:** If you select multiple data sources for a visualization and then change the visualization type to one that does not support multiple data sources, you keep only the first data source. Switching back to a visualization type that supports multiple data sources does not restore the previously selected data sources.

**Parent Topic:**[Selecting data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/selecting-data-sources.md)

**Related topics**  


[Select a table data source for a data visualization]()

[Select an indicator data source for a data visualization]()

[Select a Workflow Data Fabric data source for a data visualization]()

[Usage Insights data sources for data visualizations]()

## Example data visualization based on multiple data sources

Here's a simple example of a report based on the Indicator and Problem tables.

### Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/report-view-access-control.md) and [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/platform-analytics-roles.md).

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  For the purposes of this example, create a Vertical bar visualization.

    For more information, see [Create a horizontal or vertical bar data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-bar-ac.md).

4.  Under Data sources, select **+ Add data source**.

5.  Add the Incident \[incident\] table as a data source, with the custom condition `Active is true`.

    \[Omitted image "dv-active-true.png"\] Alt text: The Active is true condition on the Incident table data source.

6.  Select **+ Add data source** again and add the Problem \[problem\] table, also with the condition `Active is true`.

    Data sources for a visualization must all be of the same type. Here they are tables.

7.  Group both data sources by Assignment Group.

    The second source is grouped automatically by the same field as the first source.

    \[Omitted image "dv-group-by-multisource.png"\] Alt text: Group by assignment group for two table sources.

8.  To make the visualization easier to read, under **Chart variation**, select `Side-by-side`.

9.  Select Save and name the visualization `Incidents and Problems by Assignment Group`.


### Result

\[Omitted image "dv-ex-two-data-sources.png"\] Alt text: A vertical bar data visualization of Incident and Problem table data.

