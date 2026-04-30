---
title: Test the database view
description: Verify that the database view works correctly.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-05-13"
reading_time_minutes: 1
breadcrumb: [Database view creation, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Test the database view

Verify that the database view works correctly.

## Before you begin

Role required: admin.

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Database Views**.

2.  Select the database view that you want to test.

3.  Test the view by clicking the **Try It** related link.

    **Note:** If you do not see the Try It link, the tables necessary for the view do not exist. If this problem occurs, it is possible that you did not activate the necessary plugins to create the supporting tables.

    The database view runs and a list of items is displayed. If you have specified fields in the **View Fields** related list for each table, the output is limited to those fields. If you specified view fields and the view does not display correctly, review the **View Fields** related list for each table and ensure that you include fields from the **Where clause**.


## Output of the sample Incident Metrics database view

![Output of the sample Incident Metrics database view](../image/database-view-output.png)

## What to do next

To use the database view in a data visualization, select it from the data sources. Database views are listed under tables.

![image.db-view-selection]

You can create any visualization type using the database view. This example shows the database view visualized as vertical bar.

![image.db-view-used-in-data-vis]

**Parent Topic:**[Database view creation](c_CreatingDatabaseViews.md)

**Previous topic:**[Specify the number of records to return](../concept/c_SpecifyTheNumberOfRecordsToReturn.md)

**Next topic:**[Displaying function results in a database view](displaying-function-results-in-a-database-view.md)

