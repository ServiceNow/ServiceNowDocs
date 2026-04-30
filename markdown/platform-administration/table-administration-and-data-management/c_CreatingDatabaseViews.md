---
title: Database view creation
description: Create a database view to join tables. You can then create a report based on the database view.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Database view creation

Create a database view to join tables. You can then create a report based on the database view.

Use the **Database Views** module to create a database view that joins tables to create a pseudo-table that combines data from each table in the view. You can create a report on this data by adding the database view as a table in a report. Accessing the database view does not require database access.

1.  [Create a database view](t_CreateADatabaseView.md)  
Create the database view.
2.  [Add a table to the database view](t_AddATableToTheDatabaseView.md)  
Specify the table to join to the database view.
3.  [Example left join in creating a database view](example-left-join-db-view.md)  
This example shows the proper settings when using left-joins to add tables to a database view.
4.  [Specify a field to return](../concept/c_SpecifyAFieldToReturn.md)  
Restrict or specify a field that you want returned by the joined table.
5.  [Relabel a column](t_RelabelAColumn.md)  
Sometimes, two different tables may have fields of the same name that are both important \(such as two tables with a sys\_updated\_on field\). For clarity, relabel one of the fields.
6.  [Specify the number of records to return](../concept/c_SpecifyTheNumberOfRecordsToReturn.md)  
Specify the number of records to return for a database view when the view is used in a script.
7.  [Test the database view](t_TestTheDatabaseView.md)  
Verify that the database view works correctly.

**Parent Topic:**[Working with database views for reporting](../concept/c_DatabaseViews.md)

**Related topics**  


[Displaying function results in a database view](displaying-function-results-in-a-database-view.md)

[Using disjunctions in complex queries](../concept/c_UseDisjunctionsInComplexQueries.md)

[Database views in the base system](../reference/r_DatabaseViewsInTheBaseSystem.md)

