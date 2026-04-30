---
title: Alert table clean up
description: The Scheduled Jobs feature runs a script to automatically close alerts in the Alerts \[em\_alert\] table that meet specific conditions, helping reduce alert noise and keep the system clean and efficient.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rotate event tables and alert table cleanup, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert table clean up

The Scheduled Jobs feature runs a script to automatically close alerts in the Alerts \[em\_alert\] table that meet specific conditions, helping reduce alert noise and keep the system clean and efficient.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When the Event Management plugin is activated, by default a job is scheduled to run the `Event Management - auto close alerts` script to automatically close alerts in the alerts table that meet the specified conditions. The default retention policy for closed alerts is that the system deletes closed alerts if it is not updated for 90 days. For more information on the scheduled job, see [Table cleaner](https://www.servicenow.com/docs/access?context=table-cleaner&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Due to the high level of traffic to the table, you cannot audit the Alert table \[em\_alert\] as a whole. Instead, audit selected fields of interest on the table.

## Procedure

1.  Set the table to `audit = true`.

2.  Set `audit = true` on the relevant fields.

    To avoid an excess of audit records, audit only the fields that are necessary for auditing.


## Result

The `Event Management - auto close alerts` script runs automatically and repeatedly at the scheduled time and closes alerts that meet the specified conditions.

**Parent Topic:**[Rotate event tables and alert table cleanup](../concept/rotate-tables-purge-data.md)

**Related topics**  


[Rotate event tables and alert table cleanup](../concept/rotate-tables-purge-data.md)

[Modify event table rotation](event-table-rotation.md)

[Purge impact status and alert history](t_EMConfigurePurge.md)

