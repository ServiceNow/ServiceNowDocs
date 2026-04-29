---
title: Scan for users who have scripted
description: Scan your instance to find users who have scripted within a specific time frame. The scan queries the audit logs and identifies any user who has performed write or update to a table having script field.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-04-09"
reading_time_minutes: 2
keywords: [scripting governance tool, scan for scripting users, conditional script writer group, scripting access audit]
breadcrumb: [Use SGT, Scripting Governance Tool, Access Management]
---

# Scan for users who have scripted

Scan your instance to find users who have scripted within a specific time frame. The scan queries the audit logs and identifies any user who has performed write or update to a table having script field.

## Before you begin

Role required: security\_admin

**Important:** You must have elevate your role `security_admin`. See [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Scripting Governance Tool**.

2.  Select **Scan for scripting users**.

3.  Select a time period from the drop-down list.

    -   7 days
    -   15 days
    -   30 days
    -   90 days
    -   120 days
    -   180 days
    ![image.sgt-scan-scripting]

    The default value is **180 days**.

4.  Select how you want to run the scan.

    -   Run this scan now — starts the scan immediately.
    -   Schedule this scan — runs the scan at a time you specify.
5.  Select **Done** to scan.

6.  Select the scan record from **View scan** section.

    The following details are available on the **View scan** section.

    |Label|Description|
    |-----|-----------|
    |Scan number|A unique identifier for the scan, for example `SGTSCAN0000001`.|
    |Status|Status of the scan|
    |Completed|Completion state of the scan|
    |Scheduled|Scheduled time of execution for the scan|
    |Created by|User who initiated the scan|
    |Action|Actions the scan took|

    ![image.sgt-view-scans]

7.  Select the scan record to open the scan results page.

    The scan results page opens and displays the following information:

    -   Scan record number — a unique identifier for the scan, for example `SGTSCAN0000001`.
    -   Date range — the start and end timestamps of the period that was scanned.
    -   Users that have scripted — the total count of users in the **Conditional Script Writer** group and has &lt;&gt; role who modified at least one script field within the scanned period.
    -   Users that have not scripted — the total count of users in the group who made no scripting changes within the scanned period. These users are candidates for access review and removal.
    -   Users that have scripted table — a detailed list of active scripters, showing each user's Name, Last scripted date, Title, and Department.
    **Note:** If the **Users that have scripted count** is zero and the table shows `No data to display`, no users in the ServiceNow AI Platform have scripted within the selected time period.

    ![image.sgt-view-scans-result]

8.  Review the results and identify users who require action.

9.  To act on the results, select **Manage conditional script writers** on the scan results page.

    The **Manage users in the conditional script writer group** opens, where you can review group membership and remove users who no longer require scripting access using the **Schedule removal** option. To learn more about how to schedule removal, see [Remove users from the Conditional Script Writer group](remove-conditional-script-writer-users.md).


## Result

The scan produces a clear picture of active and inactive scripters on the ServiceNow AI Platform.

## What to do next

After reviewing the scan results, remove any users from the **Conditional Script Writer** group who no longer require scripting access. Removing a user from the group does not affect any other permissions they hold on the ServiceNow AI Platform.

