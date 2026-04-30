---
title: Schedule a data import
description: Schedule imports to make it possible to specify that certain import operations occur at a regular interval.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Importing data using import sets, Import sets, Imports, Data and Automation]
---

# Schedule a data import

Schedule imports to make it possible to specify that certain import operations occur at a regular interval.

## Before you begin

Role required: import\_scheduler, import\_admin, or admin

**Warning:**

Giving the user the import\_scheduler role is equivalent to giving the user the admin role, because the import\_scheduler has the ability to execute scripts with administrator level privileges.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_r53_5hm_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the scheduled data import.

</td></tr><tr><td>

Data source

</td><td>

Data source record that defines the data to import.If you select a remote data source, it refreshes using the remote connection before the import begins.

The transform map or robust transformer used for the data import is connected to the selected data source. You can view the transform map or robust transformer by opening the data source record and viewing the Transforms and Robust Transformer tabs.

</td></tr><tr><td>

Run as

</td><td>

Name of a user whose credentials the import job uses. If you do not specify a value, the import job runs as the guest user.

</td></tr><tr><td>

Active

</td><td>

Option to activate the scheduled import.

</td></tr><tr><td>

Use connection

</td><td>

Option to specify the connection alias for the scheduled import. This option is available for Data Sources configured to use a connection alias.

</td></tr><tr><td>

Connection

</td><td>

Connection to use for the scheduled import. Select the default parent alias or any of its children's aliases. This field is available when **Use connection** is checked.

 The sys\_id for the selected connection alias is stored in the Glide session. It can be accessed in the script for the custom data source or in any transform script using the code `gs.getSession().getClientData('connection_credential_alias_override')`.

</td></tr><tr><td>

Run

</td><td>

Frequency at which you want to run the import.

</td></tr><tr><td>

Day

</td><td>

Day on which to run the import. Visible only if you select Weekly or **Monthly** from the Run list.

</td></tr><tr><td>

Time

</td><td>

Time that you want the import to begin. Do not schedule multiple imports at the same time. Running multiple imports at the same time might negatively impact performance or cause an instance outage.

</td></tr><tr><td>

Repeat interval

</td><td>

Period that must elapse before the import repeats. Visible only if you set **Run** to Periodically.

</td></tr><tr><td>

Starting

</td><td class="icon">

Date on which the import should begin \(selected using the select date and time icon \(![Select date and time.](../image/view-calendar-icon.png)\). Visible only if you set **Run** to Periodically.

</td></tr><tr><td>

Parent

</td><td>

The parent import set to which this import set belongs, and after which this import should run. Visible only if you set **Run** to After Parent Runs.

</td></tr><tr><td>

Conditional

</td><td>

Option to specify a script that defines the conditions that must evaluate to true before the import runs.

</td></tr><tr><td>

Condition

</td><td>

Script that evaluates whether an import should run. Visible only if you select **Conditional**.

</td></tr><tr><td>

Concurrent Import

</td><td>

Option to run a concurrent import. A concurrent import splits the data into multiple import sets and runs the import sets concurrently to reduce processing time for large data sets.**Note:** A concurrent import does not transform data in a predictable order. If order matters, do not run a concurrent import.

 For more information, see [Concurrent imports](../concept/concurrent-imports.md).

</td></tr><tr><td>

Partition Method

</td><td>

Method used to allocate each data set record to an import set:-   **Round Robin**: The system sets partitions automatically.

Assume that there are 20 records and 4 import sets. The system allocates record 1 to import set 1, record 2 to import set 2, record 3 to import set 3, and record 4 to import set 4. The system then allocates record 5 to import set 1, record 6 to import set 2, record 7 to import set 3, and record 8 to import set 4. This pattern continues until all records are assigned to import sets.

When the allocation finishes, import set 1 contains records 1, 5, 9, 13, 17. Import set 2 contains records 2, 6, 10, 14, 18. Import set 3 contains records 3, 7, 11, 15, and 19. Import set 4 contains records 4, 8, 12, 16, and 20.

-   **Custom Script**: Sets the partitions with a **Partition Script** that you provide.
-   **Custom size**: Sets the partition size to the **Partition Size** specified.

After the system processes the first partition, the data from that partition can be transformed, even though the other partitions have not finished processing.

</td></tr><tr><td>

Partition Script

</td><td>

Script used to return a partition key. The system ensures that data set rows with the same partition key go to the same import set.Visible only if you set **Partition Method** to **Custom Script**.

</td></tr><tr><td>

Partition Size

</td><td>

The number of records in each partition.Visible only if you select a **Partition Method** of **Custom size**.

</td></tr><tr><td>

Execute pre-import script

</td><td>

Option to specify a script to run before the import happens.

</td></tr><tr><td>

Prescript

</td><td>

Script to run before the data imports. Visible only if you select **Execute pre-import script**.

</td></tr><tr><td>

Execute post-import script

</td><td>

Option to run a script after the import happens.

</td></tr><tr><td>

Post script

</td><td>

Script to run after the import happens. Visible only if you select **Execute post-import script**.**Note:** For concurrent imports, the script runs after the last **Import Set Transformer** job completes.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  To stop an import that is taking too much time, navigate to **System Import Sets** &gt; **Advanced** &gt; **Progress**.

    1.  Open the Progress Worker that you must cancel.

    2.  Click the **Cancel job** related link.

6.  To display a list of executions records, click **Executions**.

7.  From the Executions list, select the execution record that you want to display.

    The execution record shows:

    -   The execution number.
    -   The schedule import name.
    -   The import set name.
    -   The execution context number.
8.  To display details about the executions, select the executions contexts record that you want to display.


-   **[Scheduled data import scripting options](../reference/r_DataImportScriptingOptions.md)**  
Multiple JavaScript objects are available in the Scheduled Data Import **Pre script** and **Post script** fields.

**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

