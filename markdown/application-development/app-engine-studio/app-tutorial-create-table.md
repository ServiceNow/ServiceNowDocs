---
title: Create a data table
description: Create a table to store the data for your application.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building a data model, App creation tutorial, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create a data table

Create a table to store the data for your application.

## Before you begin

Role required: admin, sn\_app\_eng\_studio.user, or delegated developer

## About this task

The first phase in building the data model for the employee travel request application is to create a table. In our tutorial, we create a blank table that extends the Task table.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Create a data table](app-tutorial-create-table.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Configure a data table](app-tutorial-configure-table.md)

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Share data between tables](app-tutorial-share-data.md)

</td></tr></tbody>
</table>This procedure covers the first part of the task demonstrated in the tutorial video. The rest of the procedure is outlined in the next topic [Configure a data table](app-tutorial-configure-table.md).

Follow along to create a table for the employee travel request application.

Third video in the app creation tutorial series. Create and configure a data table to capture the necessary data for your application. 

|Timestamp|Section|
|---------|-------|
|0:10|Create a data table.|
|0:14|Create a table by extending the Task table.|
|0:21|Define table properties.|
|0:33|Add permissions to your table.|

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  Select the travel request application.

3.  On the application dashboard, select **+ Add** next to **Data**.

4.  Select **Create a blank table**.

    A blank table enables you to create the fields, rows, and columns in your table from scratch. You can import existing data, such as spreadsheets or PDFs, to create the table for your application.

5.  Select **Continue**.

6.  Select **Create from an extensible table**.

    Extensible tables are tables with built-in capabilities and functionality that you can use to create new tables. If you don't want to create a table from an extensible table, you can create a table from scratch by selecting **Create new table**.

7.  Select **Task** from the **Table** list.

    ![The Task table is one of the extensible tables available in the ServiceNow AI Platform.](../image/app-tutorial-select-task-table.png)

    The Task table is one of the commonly extended tables in the ServiceNow AI Platform. The Task table includes built-in functionality for approvals and assignments, which we need for the table in our tutorial application.

8.  Select **Continue**.

9.  Define the properties of your new table.

    We define the following properties for the table in our tutorial:

    |Field|Description|Tutorial table properties|
    |-----|-----------|-------------------------|
    |Table label|Unique label to identify the table.|`Travel request`|
    |Table name|Database name for the table. Auto-populates based on the **Table label** that you provided.|No action needed|
    |Table name prefix|Database prefix for the table. Auto-populates based on the application that you created the table in.|No action needed|
    |Make extensible|Option to enable other tables to share data from this table. For more information, see [Table extension](../concept/add-data.md#section_ebj_sdb_d5b).|No action needed|
    |Auto-number|Option to track table records with a unique number.|Select the check mark|
    |Prefix|Abbreviated name of the table to append to the beginning of record numbers.|`TRA`|
    |Starting number|Number to identify the first record created for your table.|No action needed|
    |Number of digits|Maximum number of digits for the record number.|No action needed|

10. Select **Continue**.

11. Control who has access to content in the table by adding permissions to each existing role, or creating new roles.

    **Note:** At least one role must have read access for you to be able to preview the table.

    In our tutorial, we grant the following permissions to the admin and user roles.

<table id="table_uqw_tvb_hdc"><thead><tr><th>

Role

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

**All**

</td></tr><tr><td>

User

</td><td>

-   **Create**
-   **Read**


</td></tr></tbody>
</table>12. Select **Continue** to add the roles to your new table.

13. Select **Edit table** to continue setting up your new table.


## Result

You have created a table for your application.

## What to do next

Complete the setup of your table by proceeding to the next phase: [Configure a data table](app-tutorial-configure-table.md)

