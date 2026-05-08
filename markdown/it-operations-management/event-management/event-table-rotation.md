---
title: Modify event table rotation
description: Table rotation is used by Event Management, by default, to contain the growth of event \[em\_event\] tables within the rotation table group.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rotate event and alert table for cleanup, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Modify event table rotation

Table rotation is used by Event Management, by default, to contain the growth of event \[em\_event\] tables within the rotation table group.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Table rotation ensures that event tables grow to a reasonable size.

Each table rotation has a schedule, according to which new data is written to one of the tables in the rotation group. A table rotation group includes the original table plus several additional tables. After the rotation procedure has written the last table in a rotation, the rotation overwrites the first table in the rotation. By default, the table rotation for Event Management is to rotate the em\_table to an offload table and the base table cleanup takes place after seven table rotations. For information about backing up events to a custom table, see [Event Management configuration preferences](../reference/r_EMBestPractice.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Table Rotations**.

2.  Select the \[em\_event\] table rotation group to modify.

3.  Edit the required fields.

4.  Select **Update**.


**Parent Topic:**[Rotate event and alert table for cleanup](../concept/rotate-tables-purge-data.md)

**Related topics**  


[bundle-platadm.c_TableRotation]

[bundle-platadm.t_ApplyTableRotation]

[Rotate event and alert table for cleanup](../concept/rotate-tables-purge-data.md)

