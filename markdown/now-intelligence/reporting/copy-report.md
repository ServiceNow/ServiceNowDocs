---
title: Copy a report
description: Users who cannot create their own global reports can modify a global report, and then save a personal version of the report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Copy a report

Users who cannot create their own global reports can modify a global report, and then save a personal version of the report.

## Before you begin

Role required: report\_admin. On upgraded instances, other users may have the right to copy a report using these instructions based on access control.

## About this task

If you save a global report as a group or personal report, the platform copies the report. The security state of the report is not changed.

**Note:**

-   If you open a personal report and save it as a group or global report, only the security state is changed. The report itself is not copied.
-   When you select **Insert and Stay** to copy a report, sharing settings are not copied to the new report.

This topic refers to Reporting in the Core UI. If your instance is a new Australia instance or migrated to Platform Analytics experience, see [Duplicate a visualization in the Visualization Designer](duplicate-dv-ac.md).

## Procedure

1.  Navigate to **sys\_report.list**.

2.  Select the report you want to copy.

3.  On the report's form, select **View Report**.

4.  Select the arrow next to the **Save** button or next to the Share icon \(![Share icon](../../dashboards/image/icon-share-db.png)\).

    If you have permission to change the report, you see the **Save** button. You only see the arrow if you don't have permission to change the original report.

5.  Select **Insert and Stay**.

    |With the Save button|Without the Save button|
    |--------------------|-----------------------|
    |![Save menu with Insert and Stay selected.](../image/copy-report-with-save-button.png)|![Arrow menu with Insert and Stay selected.](../image/copy-report-without-save-button.png)|

    The Insert and Stay action creates a copy of the report that you can modify.

6.  Modify the report.

    See [Report types](../reference/report-types-creation-details-rd.md).

7.  Change the report visibility.

    In the upper right side of the report form, click the **Sharing** icon \(![](../../../common/image/Form_ShareIcon.png)\) and select **Share**.


**Parent Topic:**[Using reporting](../concept/c_GenerateReports.md)

**Related topics**  


[Share a Core UI report](t_ShareASetting.md)

