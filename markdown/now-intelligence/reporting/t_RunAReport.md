---
title: View a report
description: Open a report in the Report Designer to view current data in an existing report.You can create a pie or bar chart report directly from a platform list. If you have a reporting role you can also save, distribute, and export these reports.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View a report

Open a report in the Report Designer to view current data in an existing report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

To administer reports, reporting roles, and report sources, navigate to **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select the area to administer.

This topic refers to Reporting in the Core UI. On net new Australia instances and instances migrated to Platform Analytics experience, Reporting functionality is replaced with Data Visualizations. For more information, see [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to view the list of existing Core UI reports and Platform Analytics experience data visualizations.

2.  ![Data visualizations library with both Core and Next Experience visualizations in the same list](../image/library-core-ne-dvs.png)

3.  Select the title of the report that you want to run.

4.  Select **Create data visualization** if you want to create a new data visualization.


## Result

The report is shown in the Visualization Designer.

## What to do next

[Create a report](t_CreateYourOwnReport.md#)

**Parent Topic:**[Using reporting](../concept/c_GenerateReports.md)

**Related topics**  


[Administering reports](../concept/c_AdminsteringReports.md)

## Run a report from a list

You can create a pie or bar chart report directly from a platform list. If you have a reporting role you can also save, distribute, and export these reports.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

This topic refers to Reporting in the Core UI. On net new Australia instances and instances migrated to Platform Analytics experience, Reporting functionality is replaced with Data Visualizations. For more information, see [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md). When you follow these steps, the resulting Pie chart or Bar chart is opened in the Visualization designer.

Users with the report\_admin role can create different kinds of reports in the Report Designer, see [Create a report](t_CreateYourOwnReport.md#).

### Procedure

1.  Navigate to the list, for example, `incident.list`.

2.  Right-click the header of the column that contains the values you want to be displayed as the bars or slices in the report.

3.  Select **Pie Chart** or **Bar Chart**.

    ![Run a pie or bar report from a list](../image/run-report-from-list.png)

    The Bar Chart and Pie Chart options are available on choice and reference fields. Choice fields include **Approval** and **State**. Reference fields include **Assigned to** and **Opened by**.

    The report is generated and opened in the Visualization Designer.


### What to do next

-   [Share the report using the Report Designer](t_ShareASetting.md).
-   [Publish the report](t_PublishAReport.md#) by generating a URL to share with other users.

**Related topics**  


[Pie charts](../concept/c_CreatePieCharts.md#)

[Vertical and horizontal bar reports](../concept/c_CreateBarCharts.md#)

