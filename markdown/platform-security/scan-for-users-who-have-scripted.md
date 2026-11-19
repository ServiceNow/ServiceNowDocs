---
title: Scan for users who have scripted
description: Scan your instance to find users who have scripted within a specific time frame. The scan queries the audit logs and identifies any user who has performed write or update to a table having script field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/scan-for-users-who-have-scripted.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [scripting governance tool, scan for scripting users, conditional script writer group, scripting access audit]
breadcrumb: [Use Scripting Governance Tool, Scripting Governance Tool, Access Management]
---

# Scan for users who have scripted

Scan your instance to find users who have scripted within a specific time frame. The scan queries the audit logs and identifies any user who has performed write or update to a table having script field.

## Before you begin

Role required: security\_admin

**Important:** You must elevate your role to `security_admin`. See [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/t_ElevateToAPrivilegedRole.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Scripting Governance Tool**.

2.  Select **Scan for scripting users**.

3.  Select a time period from the drop-down list.

    -   **7 days**
    -   **15 days**
    -   **30 days**
    -   **90 days**
    -   **120 days**
    -   **180 days**
    \[Omitted image "sgt-scan-scripting.png"\] Alt text: Scan for scripting users

    The default value is **180 days**.

4.  Select how you want to run the scan.

    -   **Run this scan now** — starts the scan immediately.
    -   **Schedule this scan** — starts the scan at the date and time that you specify in the **Start this at** field.
5.  If you selected **Schedule this scan**, enter the date and time to start the scan in the **Start this at** field.

    This field appears only when **Schedule this scan** is selected. The field defaults to 24 hours from the current date and time. Select the calendar icon to choose a date and time, or enter the value in the `yyyy-MM-dd HH:mm:ss` format.

6.  Select **Done** to scan.

    For a scheduled scan, the **A scan has been scheduled.** message confirms that the scan is queued.

7.  Select the scan record from the **View scan** section.

    The following details are available on the **View scan** section.

    |Label|Description|
    |-----|-----------|
    |Scan number|Unique identifier for the scan.|
    |Status|Current state of the scan. Values include Scheduled and Completed.|
    |Completed|Date and time that the scan finished. Empty for a scan that hasn't run.|
    |Scheduled|Date and time that the scan is set to start.|
    |Created by|User who created the scan.|
    |Action|Available action for the scan. For a scheduled scan, **Cancel scheduled job** cancels the scan before it runs.|

    \[Omitted image "sgt-view-scans.png"\] Alt text: View scan

8.  Select the scan record to open the scan results page.

    The scan results page opens and displays the following information:

    -   Scan record number — a unique identifier for the scan, for example `SGTSCAN0000001`.
    -   Date range — the start and end timestamps of the period that was scanned.
    -   Users that have scripted — the total count of users in the **Conditional Script Writer** group and has &lt;&gt; role who modified at least one script field within the scanned period.
    -   Users that have not scripted — the total count of users in the group who made no scripting changes within the scanned period. These users are candidates for access review and removal.
    -   Users that have scripted table — a detailed list of active scripters, showing each user's Name, Last scripted date, Title, and Department.
    **Note:** If the **Users that have scripted count** is zero and the table shows `No data to display`, no users in the ServiceNow AI Platform have scripted within the selected time period.

    \[Omitted image "sgt-view-scans-result.png"\] Alt text: Scan results page

9.  Review the results and identify users who require action.

10. To act on the results, select **Manage conditional script writers** on the scan results page.

    The **Manage users in the conditional script writer group** opens, where you can review group membership and remove users who no longer require scripting access using the **Schedule removal** option. To learn more about how to schedule removal, see [Remove users from the Conditional Script Writer group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/remove-conditional-script-writer-users.md).


## Result

The scan produces a clear picture of active and inactive scripters on the ServiceNow AI Platform.

## What to do next

After reviewing the scan results, remove any users from the **Conditional Script Writer** group who no longer require scripting access. Removing a user from the group does not affect any other permissions they hold on the ServiceNow AI Platform.

