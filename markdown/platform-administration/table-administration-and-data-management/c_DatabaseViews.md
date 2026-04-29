---
title: Working with database views for reporting
description: A database view defines table joins for reporting purposes.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Working with database views for reporting

A database view defines table joins for reporting purposes.

For example, a database view can join the Incident table to the Metric Definition and Metric Instance tables. This view can be used to report on incident metrics and may include fields from any of these three tables.

Several useful database views are installed with the Database View plugin and the Database Views for Service Management plugin. These database views cover most metric reporting needs and greatly reduce the need to define new ones.

Any user who can create a report can use database views as the report source. Access control follows this hierarchy:

1.  If ACLs exist on the database view itself, those ACLs are evaluated and take precedence.
2.  If no database view ACLs exist, the system honors ACLs from the underlying tables.

By design, database view ACLs override table-level ACLs.

**Note:**

-   The accumulated impact on performance grows as the number of tables that are included in the view and the number of records that those tables contain increases. To maximize the performance of the database view, ensure that the ‘where’ clauses that are defined in the database view are based on indexed fields.
-   A database view is not treated like a custom table, so there is no licensing impact.
-   Database view tables are not included in FTP exports.
-   Database views evaluate the ACLs of the parent table of a table included in the database view.

## Limitations

-   Database views cannot be created on tables that participate in table rotation.
-   It is not possible to edit data in the database view output.
-   Database view tables cannot be added as a data preserver in clone requests.
-   You can reference a table or database view from a different application scope in a Table Name field. However, if the field belongs to a table that extends sys\_metadata, the table or database view must belong to the same application scope as that table.

## ACLs and database views

You don't need to create ACLs on fields in the view. If field-level ACLs exist, the system evaluates them.

To require that read ACLs be added to the database views, set the **glide.security.expander.view.legacy** property to **true**. On upgraded instances, add this system property and set it to **true**.

When **glide.security.expander.view.legacy** is **true**, underlying table ACLs are ignored. When the property is **false** \(the default\), the underlying table ACLs are used if there are no database view ACLs.

You can still create additional ACLs on the database views. These ACLs are evaluated last and are always honored.

## Database view reserved words

Using the terms may cause unintended or undesirable performance. For more information, see the [MySQL reserved words document](https://dev.mysql.com/doc/refman/5.5/en/keywords.html).

-   **[Joining tables using database views](../task/c_CreatingDatabaseViews.md)**  
Join tables into a single view and then create a report based on that view.
-   **[Displaying function results in a database view](../task/displaying-function-results-in-a-database-view.md)**  
Enhance the display of a database view by adding a function field to the output to display function results.
-   **[Using disjunctions in complex queries](c_UseDisjunctionsInComplexQueries.md)**  
ServiceNow performs conjunction \(AND\) statements before disjunction \(OR\) statements in a query.
-   **[Database views in the base system](../reference/r_DatabaseViewsInTheBaseSystem.md)**  
Certain views are included in the base system with the Database Views and Database Views for Service Management plugins.

**Parent Topic:**[ServiceNow AI Platform tables and data](../../../administer/general/concept/tables-fields-and-forms.md)

