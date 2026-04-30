---
title: Find alert records in Express List using free-text search
description: Perform a free-text search for alert records in a filtered list of alerts.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Find alert records in Express List using free-text search

Perform a free-text search for alert records in a filtered list of alerts.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

Event Management searches through the alerts that you're currently seeing in the Express List based on the filters and time range you have set. It searches in the following predefined fields, even if they aren’t visible: Metric name, Node, Alert number, Alert Tags, and Description. It treats the text that you enter as a single string, not individual words.

The results match both the filters that you have applied and the string you have entered in the search field. In the resulting alert records, the entire string you searched by appears highlighted, and the available filters show the number of records that match the string. Recent searches are saved and accessible from the search field.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express List icon \(![Express List icon](../../event-management/image/express-list1.png)\).

3.  In the Search field, enter the free text to search by.

    The free-text string must be from 3 through 50 characters long. The search isn’t case-sensitive.

4.  Select the check icon ![Check icon](../../agent-client-collector/image/check-icon.png) or press **Enter** to perform the search.


