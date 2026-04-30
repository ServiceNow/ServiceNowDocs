---
title: Modify the log source retention period
description: Modify the period that Health Log Analytics retains logs from a specific source. You can calculate the impact of your intended change on storage to help you make an informed decision.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Storage space for log retention in Health Log Analytics, Health Log Analytics administration, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Modify the log source retention period

Modify the period that Health Log Analytics retains logs from a specific source. You can calculate the impact of your intended change on storage to help you make an informed decision.

## Before you begin

This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). To activate it, contact your ServiceNow account manager or ServiceNow Support.

To display **Log source retention** in the filter navigator:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Enter the property name **sn\_occ.activate\_log\_source\_retention** in the Search box.
3.  Ensure that the property value is set to **true**.

Role required: evt\_mgmt\_admin

## About this task

By default, the log retention duration per source is set to three days. You can change this number to 7, 14, or 30 days. For more information, see [Storage space for log retention in Health Log Analytics](../concept/hla-log-retention-space.md). Note that longer log retention results in higher storage usage.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Log source retention**.

2.  Calculate how changing the retention period for logs from a particular source affects storage.

    1.  Open a log source record.

    2.  In the Related Links section, select **Calculate how retention impacts storage**.

    3.  From the New retention list, select the proposed number of retention days for logs from this source.

    4.  Select **Calculate**.

        The **Projected storage usage \(GB\)** field displays the amount of storage space in GB that the source would use if the new policy were implemented.

        **Note:** Health Log Analytics bases its calculation of projected storage usage on the volume of log data that was streamed in the past. The estimate could change as the volume of streamed log data varies.

    5.  Compare the projected usage to the amount of storage needed for the current policy that is shown in the **Current storage usage \(GB\)** field.

    6.  Select **Cancel** to close the dialog box.

3.  Update the log retention policy per source or for several sources together.

    -   To update log retention for a single source:
        1.  Open a log source record.
        2.  From the Retention days list, select the required number of retention days for logs from this source.
        3.  Select **Update**.
    -   To update log retention for multiple sources:
        1.  Select several log source records.
        2.  From the Actions on selected rows choice list, select **Update multiple source retentions**.
        3.  From the New retention policy list, select the required number of retention days for logs from the selected sources.
        4.  Select **Update**.
    The updated policy takes effect in up to 15 minutes.

4.  Restore the default log retention policy per source or for all log sources.

    -   To restore the default policy for a single source:

        1.  Open a log source record from the table.
        2.  In the Related Links section of the record, select **Restore default**.
        The log retention policy for this log source reverts to the default value of three days.

    -   To restore the default policy for all sources:

        1.  In the Related Links section, select **Restore defaults**.
        2.  In the confirmation dialog, select **Continue**.
        The log retention policy for all log sources reverts to the default value of three days.


**Parent Topic:**[Storage space for log retention in Health Log Analytics](../concept/hla-log-retention-space.md)

