---
title: Find alert records in Express List using text search
description: Perform a text search for alert records in a filtered list of alerts.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Find alert records in Express List using text search

Perform a text search for alert records in a filtered list of alerts.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

Event Management searches through the alerts that you're currently seeing in the Express List based on the filters and time range you have set. It searches in the following predefined fields even if they aren’t visible: **Metric name**, **Node**, **Alert number**, **Alert Tags**, and **Description**. It treats the text that you enter as a single string rather than individual words.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon ![](../../event-management/image/express-list1.png).

3.  In the Search filtered alerts field, enter the search text.

    -   Ensure that the text string meets or exceeds the minimum character requirement specified in the notification message.
    -   The maximum character limit is 50.
    -   The search isn’t case-sensitive.
    **Note:** The minimum character requirement is determined by the **evt\_mgmt.express\_list.min\_search\_chars** system property setting.

4.  Expand the search to all alerts, including secondary alerts that are a part of alert groups, by selecting **Switch search scope** and then selecting **Extended**.

5.  Perform the search by selecting the check icon ![check icon](../../agent-client-collector/image/check-icon.png) or pressing **Enter**.


## Result

The results match both the filters that you have applied and the string you entered in the Search filtered alerts field. In the resulting alert records, the string is highlighted and the filters show the number of records that match the string. Recent searches are saved and accessible from the Search filtered alerts field.

