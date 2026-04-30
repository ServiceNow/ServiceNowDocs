---
title: Purge impact status and alert history
description: Automatically cleans up outdated impact statuses and alert history from the database to free up space, improve system performance, and ensure only relevant data is retained.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rotate event tables and alert table cleanup, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Purge impact status and alert history

Automatically cleans up outdated impact statuses and alert history from the database to free up space, improve system performance, and ensure only relevant data is retained.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

If records are older than 90 days, by default they are purged. If records are retained for a longer period, larger volumes of data are stored, and performance may be impacted. The data cleanup is done by two jobs: Event Management - Clean Alert History Table and Event Management - Clean Impact Status Table.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Event Management Properties**.

2.  To shorten the retention period, use the highlighted properties.

    ![Event Management Properties](../image/em-purge-properties.png)


-   **[Clean alert history and impact status tables](clean-alert-tables.md)**  
Schedule jobs to mark and remove old alert records in the Alert History \[em\_alert\_history\] and Impact Status \[em\_impact\_status\] tables, to prevent the tables from becoming overloaded with data.

**Parent Topic:**[Rotate event tables and alert table cleanup](../concept/rotate-tables-purge-data.md)

**Related topics**  


[Rotate event tables and alert table cleanup](../concept/rotate-tables-purge-data.md)

[Modify event table rotation](event-table-rotation.md)

[Clean alert history and impact status tables](clean-alert-tables.md)

[Alert table clean up](auto-close-alerts.md)

