---
title: Export a list report
description: You can export a list report to Excel, PDF, or CSV by scheduling an export of the report.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [List reports, Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Export a list report

You can export a list report to Excel, PDF, or CSV by scheduling an export of the report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin.

**Note:** Administrator-created restrictions may prevent users with these roles from seeing the **Schedule** option.

This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Export a visualization from the Visualization Designer](../../par-for-workspace/task/export-visualization-vd.md).

Illustration of the steps in this procedure for exporting a Core UI list report to Excel 

## Procedure

1.  Navigate to **Reports** &gt; **View / Run**.

2.  Open the list report that you want to export.

3.  Select the **Sharing** icon \(![Sharing icon](../../dashboards/image/icon-share-db.png)\) and select **Schedule**.

4.  Schedule the export of a saved list report in the desired format.

    Specify **Type** as PDF, PDF-landscape, Excel, or CSV. Excel displays report duration values in milliseconds, rather than the "&lt;x&gt; days &lt;y&gt; hours" format. For more information, see [Schedule emails of reports](t_ScheduleAReport.md#).

    ![Schedule a list report to Excel](../image/export-list-rep-excel-sched.png)


## Result

The recipients of the scheduled report will receive it in the form specified.

