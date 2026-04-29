---
title: Example left join in creating a database view
description: This example shows the proper settings when using left-joins to add tables to a database view.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Joining tables, Work with database views, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Example left join in creating a database view

This example shows the proper settings when using left-joins to add tables to a database view.

## Before you begin

Role required: admin

## About this task

The following procedure shows how to create a database view that includes a list of Catalog Tasks and their parents. Most of the steps take place on the View Table form.

![View Table form in the database view after a left-join has been added.](../image/Dbviews4.png)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Database Views**.

2.  Select the view you want to edit.

    The Database View page appears. In the View Tables related list, specify the tables you want in the database view.

3.  In the **View Tables** related list, select **New**.

4.  Add a **Left join** check box to the form by [Configuring the form layout](../../../administer/form-administration/concept/configure-form-layout.md#).

5.  Add the Catalog Task \[sc\_task\] table to the database view by filling in the form with the following data and then select **Submit**. Joined tables are ordered left to right from lowest to highest **Order** values.

    |Field|Value|
    |-----|-----|
    |Table|Catalog Task \[sc\_task\]|
    |Variable prefix|cat|
    |Order|100|
    |Where clause|Leave blank|

    The Database View page appears with the Catalog Task table in the View Tables table.

6.  In the **View Tables** table, select **New** and add the Requested Item \[sc\_req\_item\] table to the database view by filling in the form with the following data and then selecting **Submit**. Joined tables are ordered left to right from lowest to highest **Order** values.

    |Field|Value|
    |-----|-----|
    |Table|Requested Item \[sc\_req\_item\]|
    |Variable prefix|item|
    |Order|200|
    |Where clause|cat\_parent=item\_sys\_id|
    |Left join check box|True|

    The Database View page appears with the Requested Item table in the View Tables table.

7.  In the **View Tables** table, select **New** and add the Request \[sc\_request\] table to the database view by filling in the form with the following data and then selecting **Submit**.

    |Field|Value|
    |-----|-----|
    |Table|Request \[sc\_request\]|
    |Variable prefix|req|
    |Order|300|
    |Where clause|cat\_parent=req\_sys\_id|
    |Left join check box|True|

    The Database View page appears with the Request table in the View Tables table.

8.  In the **View Tables** table, select **New** and add the User \[sys\_user\] table to the database view by filling in the form with the following data and then selecting **Submit**.

    |Field|Value|
    |-----|-----|
    |Table|User \[sys\_user\]|
    |Variable prefix|user|
    |Order|400|
    |Where clause|cat\_opened\_by=user\_sys\_id|
    |Left join check box|False|

    -   The Database View page appears with the User table in the View Tables table.
    -   If the parent record of Catalog Task is a Requested Item, all the fields in the Request table will be blank.
    -   If the parent record is a Request, all the fields in Requested Item will be blank.
    -   Because of the two left joins, the Catalog Task record returns even if the parent is empty or is not a Requested Item or Request.
    -   Because User is not a left join, there must be a matching user in sys\_user for the row’s Opened By field for the Catalog Task row to return.
9.  Perform the following steps to experiment and learn more about how left joins impact database views.

    If you make the left join in:

    -   User true, rows that have an empty **Created By** return.
    -   Requested Item false, only Catalog Tasks that have a Requested Item as a parent return.
    -   Request false, only Catalog Tasks that have a Request as a parent return.
    -   Requested Item and Request false, no rows return because nothing can have a Requested Item and a Request as parents.

**Parent Topic:**[Joining tables using database views](c_CreatingDatabaseViews.md)

**Previous topic:**[Add a table to the database view](t_AddATableToTheDatabaseView.md)

**Next topic:**[Specify a field to return](../concept/c_SpecifyAFieldToReturn.md)

