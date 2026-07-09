---
title: Restore archived records and related records
description: Restore one or more archive records and any related records back into the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dmc-restore-archived-records.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage data growth in Data Management, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Restore archived records and related records

Restore one or more archive records and any related records back into the primary table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the table with archived records that you want to restore in one of the following ways.

    1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Console**.

    2.  Select the **Tables** tab.

    3.  Find the table with records that you want to restore.

        Tables with archived records have the Archive value in the Status column.

2.  Select **View records**.

3.  Select one or more records that you want to restore.

4.  Restore the selected records using one of the following options.

    -   Select the **Restore All Records Matching Conditions** related link.
    -   Open the **Actions on selected rows...** drop-down, and then select **Restore Selected**.
5.  In the Bulk Restore Request Success confirmation dialog box that appears, select **OK**.


## Result

One or more records are restored to the primary table. The corresponding archive records are deleted from the archive table.

## What to do next

View the restore date and time in the **Restored** column in the Archive Log related list.

