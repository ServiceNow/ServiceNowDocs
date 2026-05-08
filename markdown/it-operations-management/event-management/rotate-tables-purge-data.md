---
title: Rotate event and alert table for cleanup
description: The growth of data tables impedes performance. Preserve instance performance by event table rotation and alert table cleanup for status and alert history retention.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Rotate event and alert table for cleanup

The growth of data tables impedes performance. Preserve instance performance by event table rotation and alert table cleanup for status and alert history retention.

## Containing the growth of event tables

By default, the Event Management event \[em\_event\] table uses table rotation. The table rotation schedule ensures that new data is written to one of the tables in the rotation group. According to the value of **Clean base rotation** setting, the base table is deleted and then a new round of writing the tables in a daily rotation commences. By default, this table deletion occurs after seven rotations.

To back up events to a custom table, see [Event Management configuration preferences](../reference/r_EMBestPractice.md).

## Containing the growth of alert tables

By default, a scheduled job cleans out the alert \[em\_alert\] table. Table cleanup is done also for impact status and alert history table.

-   **[Modify event table rotation](../task/event-table-rotation.md)**  
Table rotation is used by Event Management, by default, to contain the growth of event \[em\_event\] tables within the rotation table group.
-   **[Purge impact status and alert history](../task/t_EMConfigurePurge.md)**  
Automatically cleans up outdated impact statuses and alert history from the database to free up space, improve system performance, and ensure only relevant data is retained.
-   **[Alert table clean up](../task/auto-close-alerts.md)**  
The Scheduled Jobs feature runs a script to automatically close alerts in the Alerts \[em\_alert\] table that meet specific conditions, helping reduce alert noise and keep the system clean and efficient.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

**Related topics**  


[Purge impact status and alert history](../task/t_EMConfigurePurge.md)

[Alert table clean up](../task/auto-close-alerts.md)

[bundle-platadm.c_TableRotation]

