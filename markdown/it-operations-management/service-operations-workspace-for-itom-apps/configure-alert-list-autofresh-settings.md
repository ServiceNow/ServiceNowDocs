---
title: Configure auto-refresh settings for alert lists
description: Set up auto-refresh settings for alert lists to ensure real-time updates and seamless monitoring. This enhances the accuracy and timeliness of the information displayed, enabling quicker response times and improving overall system reliability and performance.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace, Configuring Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Configure auto-refresh settings for alert lists

Set up auto-refresh settings for alert lists to ensure real-time updates and seamless monitoring. This enhances the accuracy and timeliness of the information displayed, enabling quicker response times and improving overall system reliability and performance.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

By default, alerts in the alert lists are automatically updated \(auto-refresh\) whenever an action is performed on an alert. You can configure the amount of time, in seconds, after which the alert list refreshes following an action. You can also disable auto-refresh and configure how often the alert list is updated. This is useful when many alerts are being processed continuously, to prevent excessive refreshing.

**Note:** Set Read Role permissions to the Event Management user \(evt\_mgmt\_user\). Otherwise, the property will not be available.

## Procedure

1.  Navigate to **All** and in the search field, enter `sys_properties_list.do`.

    The System Properties window opens.

2.  Search for the following properties and configure their values as required.

<table id="table_hxm_j1h_ktb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`evt_mgmt.ai_refresh_time_to_wait_after_manual_action`

</td><td>

Alert list refresh time \(in milliseconds\) after a manual action has been performed on the alert.

 If multiple actions have been performed successively, the refresh time begins anew after the last action. This ensures that the alert list reflects the latest state and updates promptly following user interactions.

</td></tr><tr><td>

`evt_mgmt.ai_refresh_time_interval`

</td><td>

If an alert update is received within the defined time interval \(5000 milliseconds\), no immediate refresh will occur for updates during that period. Instead, the system will perform another refresh at the end of the time interval to ensure the alert list reflects the most current information available.

</td></tr><tr><td>

`evt_mgmt.disable_lists_auto_refresh`

</td><td>

Disables the auto-refresh process of the alert lists.You can create a new list on the **Alert Lists Auto Refresh** page by entering **em\_alert\_lists\_auto\_refresh.list** in the navigation pane. To prevent automatic refresh of the list, clear the **Enable Refresh** option.

</td></tr></tbody>
</table>
