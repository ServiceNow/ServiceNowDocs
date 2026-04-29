---
title: Enable and disable live updates for alert lists
description: Choose live updates for alert lists to receive real-time updates, or disable live updates and refresh the alert list manually.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Enable and disable live updates for alert lists

Choose live updates for alert lists to receive real-time updates, or disable live updates and refresh the alert list manually.

## Before you begin

Role required: evt\_mgmt\_user, evt\_mgmt\_operator, or evt\_mgmt\_admin

## About this task

By default, the toggle for live updates is off, and you must enable it to receive live alert updates. Once enabled, the alert list automatically updates whenever an action is performed on an alert. Live updates enhance the accuracy and timeliness of the information displayed, enabling quicker response times, and improving overall system reliability and performance.

To update the alert list manually, you can switch the live updates toggle to off. Manual updates are useful when many alerts are being processed continuously, to avoid excessive refreshing.

**Note:** Set Read Role permissions to the Event Management user \(evt\_mgmt\_user\). Otherwise, the property won't be available.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the List icon: ![List icon](../image/list-icon-sow-itom.png).

3.  Select the **Default lists** tab.

4.  Under **Alerts**, select the list where you want to enable or disable live updates.

    **Note:** Live updates aren’t available for the **All Alert** list.

5.  At the top of the alert list, select the toggle switch to turn live updates on or off.

    -   When live updates are turned on, the setting is saved for future logins by the same user.
    -   When live updates are off, the refresh button displays a counter to show the number of changes since the last refresh. You can select the refresh button anytime to update the list manually.

