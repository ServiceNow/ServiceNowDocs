---
title: Scheduled export reference qualifiers
description: Use reference qualifiers to specify the users and groups in the recipients field of scheduled exports.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Schedule the export of dashboards and data visualizations, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Scheduled export reference qualifiers

Use reference qualifiers to specify the users and groups in the recipients field of scheduled exports.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Open the **par\_notification\_email\_recipients** table.

3.  Press Ctrl+Click on the Preview Users button ![info button](../../performance-analytics/image/InfoIcon.png)next to Users on the **Columns** tab to open the Users dictionary entry.

    Point to the Users Column label to see this button.![Preview Users and Preview Groups buttons on the Columns list of Par Notification Email Recipients](../image/preview-buttons-sched-export.png)

4.  If you're in the wrong application, select the link to edit the record.

    ![Mismatched application message with link to edit the record](../image/app-mismatch-msg-sched-export.png)

5.  On the Reference Specification tab of the dictionary entry, use the condition builder to add filter conditions to the User list.

    For example, configure the reference qualifier condition \[Name\] \[starts with\] \[b\]. Only users whose names start with the letter B will show up in the list of users in the recipients list when configuring an export.

6.  Select **Update**.

7.  Press Ctrl+Click on the Preview Groups button ![info button](../../performance-analytics/image/InfoIcon.png)next to Groups on the **Columns** tab to open the Users dictionary entry.

    Point to the Groups Column label to see this button.

8.  On the Reference Specification tab, use the condition builder to add filter conditions to the Groups list.

    For example, configure the reference qualifier condition \[Name\] \[does not contain\] \[Itil\]. Groups whose names contain the string `itil` will not show up in the list of groups in the recipients list when configuring an export.

9.  Select **Update**.


**Parent Topic:**[Schedule the export of dashboards and data visualizations](schedule-export-dboards-data-viz.md)

