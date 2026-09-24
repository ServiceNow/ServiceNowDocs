---
title: Create a data visualization from a list
description: You can create a Platform Analytics vertical bar or pie data visualization from inside a Core UI list. If you have a data visualization role, you can save, share, export, or duplicate the visualization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-data-viz-from-list.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a data visualization from a list

You can create a Platform Analytics vertical bar or pie data visualization from inside a Core UI list. If you have a data visualization role, you can save, share, export, or duplicate the visualization.

## Before you begin

Role required: You need a role that gives access to the list. To save, share, export, or duplicate the visualization, you need itil, viz\_creator, or a role that contains viz\_creator, such as any of the reporting roles.

## About this task

If you're on a new instance or an instance that has fully migrated to Platform Analytics, follow this procedure. Otherwise, you create a Core UI pie or bar report, instead. In this case, see [Run a report from a list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/t_RunAReport.md).

Specifically, whether this feature creates Platform Analytics or Core UI bars and pies is linked to whether both Platform Analytics and Core UI dashboards are available in the dashboard libraries. To combine all dashboards in the library, and thus to open Platform Analytics visualizations from a list, set the property **com.glide.par.unified\_analytics.enabled** to `true`.

## Procedure

1.  Navigate to the list.

2.  Select and hold \(or right-click\) the header of the column that contains the values you want to be displayed as the bars or slices in the visualization.

3.  Select **Pie Chart** or **Bar Chart**.

    \[Omitted image "run-report-from-list.png"\] Alt text: Create a pie or bar data visualization from a list

    The data visualization is generated and opened in the Visualization Designer.


**Parent Topic:**[Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/creating-data-visualizations.md)

