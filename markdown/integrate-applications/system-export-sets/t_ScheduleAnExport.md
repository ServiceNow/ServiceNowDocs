---
title: Schedule an export
description: You can schedule an export to regularly push data from an export set to a remote destination. By setting up a recurring, scheduled export you are able to regularly push data to an external location, such as for reporting or for preserving a snapshot of the data.Delta exports include only the records that changed since the last scheduled export.When scheduling an export set, you can access certain JavaScript objects.
locale: en-US
release: australia
product: System Export Sets
classification: system-export-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Schedule an export

You can schedule an export to regularly push data from an export set to a remote destination. By setting up a recurring, scheduled export you are able to regularly push data to an external location, such as for reporting or for preserving a snapshot of the data.

## Before you begin

Role required: export\_set\_scheduler or export\_set\_admin

## About this task

You can configure scheduled export sets to export only new or changed records using delta exports.

## Procedure

1.  Navigate to **All** &gt; **System Export Sets** &gt; **Administration** &gt; **Scheduled Exports**.

2.  Click **New**.

3.  Fill in the following fields.

<table id="table_ktt_k4y_lr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for this scheduled export.

</td></tr><tr><td>

Export set

</td><td>

Select the export set to schedule.

</td></tr><tr><td>

Run as

</td><td>

Select the user to run the scheduled export as. Ensure the user has any roles needed to view the data to export.

</td></tr><tr><td>

Run

</td><td>

Select the frequency for scheduled export.

</td></tr><tr><td>

Day

</td><td>

Select which day of the week or month to run this scheduled export on. This field appears when the **Run** field is set to **Weekly** or **Monthly**

</td></tr><tr><td>

Repeat interval

</td><td>

Enter the number of days and hours to wait before repeating this scheduled export. This field appears when the **Run** field is set to **Periodically**.

</td></tr><tr><td>

Time

</td><td>

Enter the time of day to run the scheduled export.

</td></tr><tr><td colspan="2">

Delta Exports

</td></tr><tr><td>

Enable delta exports

</td><td>

Select this check box to enable delta functionality for this scheduled export. When selected, only new or changed records are exported.

</td></tr><tr><td>

Delta on or after

</td><td>

Select **Updated** to export all records that changed since the last export, including new records. Select **Created** to export only new records created after the last export.**Note:** If the export definition already includes a filter condition on the sys\_updated\_on or sys\_created\_on fields, enabling delta exports will prevent you from saving the scheduled data export record. An error appears at the top of the form in this event.

</td></tr><tr><td>

Last export scheduled run

</td><td>

Leave this field blank to export all records from the export definition. When using delta exports, this field is set automatically each time the scheduled export runs. Records updated or created after this date and time are included in the export delta, depending on the **Delta on or after** value.

</td></tr><tr><td colspan="2">

Scripts

</td></tr><tr><td>

Conditional

</td><td>

Select this check box to run the schedule only when a condition is met.

</td></tr><tr><td>

Condition

</td><td>

Write the script to be used to evaluate whether the export should run. This field is visible if you select the **Conditional** check box.

</td></tr><tr><td>

Execute pre-export script

</td><td>

Select this check box to run a script before the export begins.

</td></tr><tr><td>

Pre script

</td><td>

Write the script you want to run before the data is exported. This field is visible if you selected the **Execute pre-export script** check box.

</td></tr><tr><td>

Execute post-export script

</td><td>

Select this check box to run a script after the export finishes.

</td></tr><tr><td>

Post script

</td><td>

Write the script you want to run after the export finishes. This field is visible if you selected the **Execute post-export script** check box.

</td></tr><tr><td>

Parallel export

</td><td>

Select this check box to enable parallel exports. See [Parallel exports](../concept/parallel-exports.md).

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

You can click the **Execute Now** button to run the export immediately and confirm the data is exported as expected.

## Scheduled export set delta exports

Delta exports include only the records that changed since the last scheduled export.

You can use delta export for regular tables only, such as the task and problem tables.

**Important:** You cannot use delta export for a database view table, which is a virtual table that joins physical tables.

A database view does not include system fields such as sys\_created on, sys\_created by and sys\_updated on. Because the system date fields are not included in the database view, you cannot use delta exports with database views since there is no way to know when the table was last updated.

## Scheduled export set scripting options

When scheduling an export set, you can access certain JavaScript objects.

Use these objects in scheduled export set scripts, such as the **Pre-script** and **Post-script** fields.

-   **cancel**

    Set this object to true to stop the export action. Any child export sets are also cancelled if the parent is cancelled. This object is available only in the **Pre-script** field.

    Example: Use the **Pre-script** field to evaluate the conditions of the export and determine whether to cancel the export process. To cancel the export process, use the following call:

    ```
    cancel = true;
    ```

-   **export\_set**

    Get the GlideRecord object for the new export set. This variable allows you to query the following columns from the sys\_export\_set table:

    -   name
    -   sys\_id
    -   state
    -   table\_name
    This object is available in both the **Pre-script** and **Post-script** fields.

    Example: If you want to use information from the export set, you can specify one of the properties of the export\_set variable.

    ```
    var x = export_set.sys_id;
    ```


