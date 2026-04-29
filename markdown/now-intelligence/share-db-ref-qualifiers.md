---
title: Dashboard sharing reference qualifiers
description: Use reference qualifiers to limit the users, groups, and roles in the recipients field of shared dashboards.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Share a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Dashboard sharing reference qualifiers

Use reference qualifiers to limit the users, groups, and roles in the recipients field of shared dashboards.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Open the **par\_dashboard\_permission** table.

3.  Press Ctrl+Click on the Preview Users button ![info button](../../performance-analytics/image/InfoIcon.png)next to Users on the **Columns** tab to open the Users dictionary entry.

    Point to the Users Column label to see this button.![Preview Users and Preview Groups buttons on the Columns list of Par Notification Email Recipients](../image/preview-buttons-sched-export.png)

4.  If you're in the wrong application, select the link to edit the record.

    ![Mismatched application message with link to edit the record](../image/app-mismatch-msg-sched-export.png)

5.  On the Reference Specification tab of the dictionary entry, use the condition builder to add filter conditions to the User list.

    For example, configure the reference qualifier condition \[Name\] \[starts with\] \[b\]. Only users whose names start with the letter B will show up in the list of users in the recipients list when sharing a dashboard.

6.  Select **Update**.


## What to do next

Perform the same actions on the Group and Role columns to limit sharing with those categories of recipient.

**Parent Topic:**[Share a Platform Analytics dashboard](../../dashboards/task/share-db-in-ac.md)

