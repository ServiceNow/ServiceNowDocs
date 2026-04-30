---
title: Mute a CI's alerts in Express List
description: Mute a CI's alerts in Express List to avoid alerts being issued when replacing or upgrading the CI.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Mute a CI's alerts in Express List

Mute a CI's alerts in Express List to avoid alerts being issued when replacing or upgrading the CI.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

**Note:** The evt\_mgmt\_user role is view-only and does not have permission to perform this action.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  Select the alert row check box.

    **Note:** You can perform the action on up to 1,000 alerts simultaneously by selecting the **Select All** check box in the Active alerts list. ![Select All check box.](../image/el-select-all.png)

4.  From the **Close** drop-down list, select **Put in Maintenance**.


## Result

Alerts are muted for the configuration items of that alert.

