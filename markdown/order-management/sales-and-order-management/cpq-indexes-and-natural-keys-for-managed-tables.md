---
title: Indexes and natural keys for managed tables
description: Use indexes and natural keys to improve rule engine performance and speed up table lookups.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-17"
reading_time_minutes: 2
breadcrumb: [Configure the Matrix Loader, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Indexes and natural keys for managed tables

Use indexes and natural keys to improve rule engine performance and speed up table lookups.

ServiceNow CPQ supports the integration of natural keys and indexes for faster table lookups and heightened rules engine performance.

This enhancement to ServiceNow CPQ's table management system introduces compatibility with up to three natural keys per table and the addition of two indexed columns.

-   A natural key provides a means of unique identification for data in a table.
-   Indexed columns quickly locate data without having to search every row in the table every time the table is accessed.

**Note:** All columns designated as natural keys undergo automatic indexing, optimizing the efficiency of query operations. Indexed columns are not required to be unique, and can work alongside natural keys for multiple data retrieval options.

Lookup functions that reference a column in their SELECT clause can benefit from the addition of indexing the column, as searches can be performed faster with no changes needed to the script.

These features can be added to a column by editing the table schema. \(The schema editor opens automatically when you create a new table.\)

![Tables list](../images/cpq-tables-edit-schema.png)

![Edit table schema screen](../images/cpq-tables-edit-table-schema.png)

Because all natural keys are also indexed, checking the column does not allow the user to also check the Indexed column.

![Column details](../images/cpq-tables-column-options.png)

When the Natural Key column is checked, a keys icon displays in the table.

![Enrichment test](../images/cpq-tables-keys-icon.png)

Another icon indicates which columns are indexed.

![columns list](../images/cpq-tables-indexed-column-icon.png)

Since natural keys act as unique identifiers in the table, internal validation makes sure that each column in the table is unique.

When adding a natural key to a column with duplicate rows, the table does not allow the schema to save.

When exporting a table, the schema file indicates whether a column is indexed or is a natural key, so when the user imports the table to another environment, the schema’s column settings are saved.

## Reasons an import might fail

Some factors associated with natural keys and Indexes might hamper table import. These factors include:

-   There are more than three columns set to be natural keys in the schema
-   There are more than two columns set to be indexed in the schema
-   A column set to be a natural key contains duplicate rows

**Related topics**  


[Minimizing table queries](table_queries.md)

[The lookup function: commands and syntax](cpq-the-lookup-function-commands-and-syntax.md)

