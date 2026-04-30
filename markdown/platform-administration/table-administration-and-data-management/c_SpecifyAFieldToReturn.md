---
title: Specify a field to return
description: Restrict or specify a field that you want returned by the joined table.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-02-07"
reading_time_minutes: 1
breadcrumb: [Joining tables, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify a field to return

Restrict or specify a field that you want returned by the joined table.

## Before you begin

Role required: admin

## About this task

You can restrict the fields displayed in the database view output by adding fields to the View Tables related list.

When you restrict fields, you must create a View Field record for the join field from the Where clause in the parent record. If you omit a record for this field, it cannot be returned, and the join fails.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Database Views**.

2.  Select the database view you want to add a field to return to.

3.  In the database view record, select a view table, and then select **New** in the View Fields related list.

4.  In the View Field form, select the field you want to display in the database view output.

    If no fields are defined in the View Fields related list, all fields are returned. If any fields are defined, then only those fields are returned. For example, you can restrict the display if there are fields that should not be viewable to all users.

    ![View Field form](../image/database-views-view-field-form.png "View Field form")

    In this example, the Where clause uses the sys\_id field from the Incident table to establish the join. For the join to succeed with a restricted field list, you must include a record for the sys\_id field in the View Fields related list.


## What to do next

Verify your changes using the **Try It** related link in the database view record. See [Test the database view](../task/t_TestTheDatabaseView.md).

**Parent Topic:**[Joining tables using database views](../task/c_CreatingDatabaseViews.md)

**Previous topic:**[Example left join in creating a database view](../task/example-left-join-db-view.md)

**Next topic:**[Relabel a column](../task/t_RelabelAColumn.md)

