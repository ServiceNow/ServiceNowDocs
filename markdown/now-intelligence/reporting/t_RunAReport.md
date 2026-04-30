---
title: View a report
description: Open a report in the Report Designer to view current data in an existing report.You can create a pie or bar chart report directly from a platform list. If you have a reporting role you can also save, distribute, and export these reports.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View a report

Open a report in the Report Designer to view current data in an existing report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

To administer reports, reporting roles, and report sources, navigate to **Reports** &gt; **Administration** and select the area to administer.

This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [View data visualizations](../../performance-analytics/concept/view-data-visualizations.md).

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View/Run** to view the list of existing reports.

    If you don't see the report that you want to view, select **All** to see the complete list of reports.

    On instances with Unified Analytics enabled, and on new Zurich instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

2.  Select the title of the report that you want to run.

3.  Select **Create a report** if you want to create a new report visualization.

    ![truncated reports list with the All and Create a report options outlined in red](../image/run-report.png)


## Result

The report is shown in the Report Designer.

## What to do next

[Create a report](t_CreateYourOwnReport.md#)

**Parent Topic:**[Using reporting](../concept/c_GenerateReports.md)

**Related topics**  


[Administering reports](../concept/c_AdminsteringReports.md)

## Run a report from a list

You can create a pie or bar chart report directly from a platform list. If you have a reporting role you can also save, distribute, and export these reports.

### Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

To create a different kind of report, see [Create a report](t_CreateYourOwnReport.md#).

### Procedure

1.  Navigate to the list, for example, `incidents.list`.

2.  Right-click the header of the column that contains the values you want to be displayed as the bars or slices in the report.

3.  Select **Pie Chart** or **Bar Chart**.

    ![Run a pie or bar report from a list](../image/run-report-from-list.png)

    The report is generated and opened in the Report Designer.


### What to do next

-   [Share the report using the Report Designer](t_ShareASetting.md).
-   [Publish the report](t_PublishAReport.md#) by generating a URL to share with other users.

**Related topics**  


[Pie charts](../concept/c_CreatePieCharts.md#)

[Vertical and horizontal bar reports](../concept/c_CreateBarCharts.md#)

