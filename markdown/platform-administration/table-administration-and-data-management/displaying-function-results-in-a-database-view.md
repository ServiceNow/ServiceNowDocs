---
title: Displaying function results in a database view
description: Enhance the display of a database view by adding a function field to the output to display function results.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Displaying function results in a database view

Enhance the display of a database view by adding a function field to the output to display function results.

Function fields perform common database transformations and calculations on fields in the system. Function fields do not store any data, but rather display the results of a database query when the function is executed.

For example, you could identify incidents with ineffective descriptions of fewer than 10 characters by adding a function field that calculates the length of the **Short description** field.

-   **[Create a function field to perform a database function](create-a-function-field-to-perform-a-database-function.md)**  
Create a function field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.
-   **[Display function results in a database view](display-function-results-in-a-database-view.md)**  
Add a function field to the output of a database view to see function results.

**Parent Topic:**[Working with database views for reporting](../concept/c_DatabaseViews.md)

**Related topics**  


[Database view creation](c_CreatingDatabaseViews.md)

[Using disjunctions in complex queries](../concept/c_UseDisjunctionsInComplexQueries.md)

[Database views in the base system](../reference/r_DatabaseViewsInTheBaseSystem.md)

