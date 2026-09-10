---
title: Find alert records in Express List using text search
description: Perform a text search for alert records in a filtered list of alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/el-free-text-search.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assign and manage alerts, Express List, Event Management, ITOM AIOps, IT Operations Management]
---

# Find alert records in Express List using text search

Perform a text search for alert records in a filtered list of alerts.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

Event Management searches through the alerts that you're currently seeing in the Express List based on the filters and time range you have set. It searches in the following predefined fields even if they aren’t visible: **Metric name**, **Node**, **Alert number**, **Alert Tags**, and **Description**. It treats the text that you enter as a single string rather than individual words. The selected alert list mode determines which alert types are displayed and included in the search. **Essential** mode displays primary and single alerts only. **Extended** mode displays all alert types, including secondary alerts.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  Select **Essential** or **Extended** from the **Switch search scope** menu.

    **Essential** includes primary and single alerts. **Extended** includes all alert types, including secondary alerts.

4.  In the **Search filtered alerts** field, enter the search text.

    -   Ensure that the text string meets or exceeds the minimum character requirement specified in the notification message.
    -   The maximum character limit is 50.
    -   The search isn’t case-sensitive.
    **Note:** The minimum character requirement is determined by the **evt\_mgmt.express\_list.min\_search\_chars** system property setting.

5.  Perform the search by selecting the check icon \[Omitted image "check-icon.png"\] or pressing **Enter**.


## Result

The results match both the filters that you have applied and the string you entered in the Search filtered alerts field. In the resulting alert records, the string is highlighted and the filters show the number of records that match the string. Recent searches are saved and accessible from the Search filtered alerts field.

