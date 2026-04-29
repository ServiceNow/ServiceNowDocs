---
title: Analyzing table relationships
description: The schema map shows the selected table in yellow, typically centered, and all tables related to that table, typically shown at the sides.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View table refs and extensions, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Analyzing table relationships

The schema map shows the selected table in yellow, typically centered, and all tables related to that table, typically shown at the sides.

![](../../../use/using-forms/image/SchemaMapv31.png "Example schema map")

From this map:

-   The check boxes at the top allow you to control which relationships to display. Select or clear a relationship type to display or hide tables with that relationship to the selected table.
-   Each related table has a colored bar indicating the relationship to the selected table.
-   You can point to the connector lines to display the details of a relationship between the two tables.

**Note:** Since relationships are shown as single lines for simplicity, the diagrams rendered are not entity relationship diagrams.

Using the Table Selector:

To view a schema map as a list, point to the table selector in the right corner:![List view of tables.](../../../use/using-forms/image/SchemaMapv32.png)

You can:

-   Click a table in the list to scroll the schema map to that table.
-   Click the eye icon beside a listed table to hide or show that table in the schema map.
-   Click the pin icon in the selector to keep the list open.

Using Related Tables:

Right-click a table node header to display a context menu with these functions:

-   **Focus on this table**: Make the selected table the new focus table and redraw the schema map based on the new selection.

    The new focus table is added as a breadcrumb at the top, allowing you to return to the previous table at any time.

-   **Go to list**: Display the list of records for the table.
-   **Go to dictionary**: Display the system dictionary, filtered for the selected table.

To hide a related table from view, click the eye icon in the node header \(the node can be made visible again with the table selector\).

For tables that are part of their own derivation hierarchy, click the expand button \(**+**\) in the node header to add their derivation hierarchy to the schema map.

## Viewing More Information

Click the expand button \(**+**\) beside **Columns** to expand the table fields.

![Expanded view of tables.](../../../use/using-forms/image/ERD10.png)

The reference fields show a red notation of the table they refer to.

If any tables extend from a table, their columns are displayed in reverse derivation order. For example:

![Server is derived from Computer, which is derived from Hardware, which is derived from Configuration Item.](../../../use/using-forms/image/SchemaMapRelatedTables.png)

Here, the Server `[cmdb_ci_server]` table extends from Computer `[cmdb_ci_computer]`, Hardware`[cmdb_ci_hardware]`, and Configuration Item `[cmdb_ci]`, and displays the columns from those tables.

Similarly, the Computer table displays the columns from the Hardware and Configuration Item tables.

**Parent Topic:**[Viewing table references and extensions](c_SchemaMapForTables.md)

