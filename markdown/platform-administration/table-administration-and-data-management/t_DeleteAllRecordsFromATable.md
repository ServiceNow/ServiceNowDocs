---
title: Delete all records from a table
description: You may decide to delete all the records on a table without deleting the table itself. For example, the administrator may want to delete all incidents on a test instance without deleting the incident table itself.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Deleting custom tables, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Delete all records from a table

You may decide to delete all the records on a table without deleting the table itself. For example, the administrator may want to delete all incidents on a test instance without deleting the incident table itself.

## Before you begin

Role required: admin

## About this task

When you prepare to delete many records from a table, consider the following guidelines to minimize impact on performance.

-   Limit the number of records to be deleted in a single delete action to prevent the table from being locked. Use the setLimit\(\) method described at setLimit.
-   Minimize triggering an excessive number of business rules as a result of this deletion. Use the setWorkflow\(Boolean e\) method described at setWorkflow.

**Note:** Deleting all records for a table also deletes records from tables that extend the table.

There are several methods for deleting table records. Depending on the number of records to be deleted, choose the method that would be most efficient in your environment. Use these methods with caution. Before performing this procedure, be sure that you do not need any of the records.

## Procedure

-   From the **Tables and Columns** module, complete the following steps.

    1.  Navigate to **System Definition** &gt; **Tables &amp; Columns**.

    2.  Select the table for which to delete records.

        **Note:** If the table you want to delete records from belongs to a scoped application, select that application in the scope picker. Alternatively, configure scope-to-scope access. See Restricted caller access privilege settings.

        ![Tables and Columns](../image/tables_and_columns.png)

        **Note:** Some system tables do not allow this method of deleting records, for example, you cannot delete all user records \[sys\_user\]. The list of tables does not include system tables that you cannot delete records from.

    3.  Click **Delete all records**.

    4.  In the confirmation dialog box, enter `delete` and click **OK**.

-   From a list view, complete the following steps.

    1.  In List v2, navigate to the list view that displays the table records, click the context menu, and then navigate to **Show**.

    2.  In List v3, click **&lt;Number&gt; rows per page** in the footer.

    3.  Set the number of rows per page to display the max number.

    4.  Select all the rows on the page.

    5.  Click **Actions on selected rows**, and then click **Delete**.

    6.  Continue deleting all rows on a page until all records are deleted.


## Result

The selected table is empty of records. The table still exists, and any references to the table on other tables \(such as business rules or reference fields\) are preserved.

**Parent Topic:**[Deleting custom tables](../concept/c_DeleteATable.md)

