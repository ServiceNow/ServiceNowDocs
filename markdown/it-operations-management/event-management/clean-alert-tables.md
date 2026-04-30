---
title: Clean alert history and impact status tables
description: Schedule jobs to mark and remove old alert records in the Alert History \[em\_alert\_history\] and Impact Status \[em\_impact\_status\] tables, to prevent the tables from becoming overloaded with data.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Purge impact status and alert history, Rotate event tables and alert table cleanup, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Clean alert history and impact status tables

Schedule jobs to mark and remove old alert records in the Alert History \[em\_alert\_history\] and Impact Status \[em\_impact\_status\] tables, to prevent the tables from becoming overloaded with data.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Schedule the following jobs to remove old alert records:

-   **Backfill**: Determines when alerts are to be marked for deletion.
-   **Clean**: Deletes the alerts.

**Note:** The records in the \[em\_alert\_history\] and \[em\_impact\_status\] tables are deleted by default after three months. This is controlled by the properties **evt\_mgmt.impact\_calculation.cleanup\_age\_seconds.em\_alert\_history** and **evt\_mgmt.impact\_calculation.cleanup\_age\_seconds.em\_impact\_status**. The default value is 7,776,000 seconds \(equivalent to 90 days\).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    The **Scheduled Jobs** page appears.

2.  To determine how often to mark alerts for deletion on the **Impact Status** table:

    1.  Locate and select the **Event Management - Backfill Impact Status Table** job.

        The **Scheduled Script Execution** page appears.

        ![Scheduled Script Execution page](../image/scheduled-script-execution.png "Scheduled Script Execution page")

    2.  In the **Repeat Interval** field, configure how often you want the job to run.

        To run the job immediately, select **Execute Now**.

    3.  Select **Update**.

3.  To remove old alerts from the **Impact Status** table:

    1.  Locate and select the **Event Management - Clean Impact Status Table** job.

        The **Scheduled Script Execution** page appears.

        ![Scheduled Script Execution page](../image/scheduled-scipt-execution-clean.png)

    2.  In the **Repeat Interval** field, configure how often you want the job to run.

        To run the job immediately, select **Execute Now**.

    3.  Select **Update**.

4.  Repeat steps [2](clean-alert-tables.md#2) and [3](clean-alert-tables.md#3) to perform the Backfill and Clean jobs on the **Alert History Table**.


**Parent Topic:**[Purge impact status and alert history](t_EMConfigurePurge.md)

