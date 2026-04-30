---
title: The lookup function: commands and syntax
description: Use the lookup function to return information from a user-managed table.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-11-03"
reading_time_minutes: 2
breadcrumb: [Setting up enrichments and rules scripting, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The lookup function: commands and syntax

Use the lookup function to return information from a user-managed table.

ServiceNow CPQ uses a SQL-based query language to look up user-managed tables.

The lookup function returns up to 10,000 rows from a table and times out after 30 seconds if the search is still querying. For information about uploading CSV files into managed tables, see [Matrix Loader: CSV table upload](../task/cpq-matrix-loader-csv-table-upload.md).

To learn about best practices for using the lookup function, see [Minimizing table queries](table_queries.md).

## Supported commands

-   SELECT selects columns from a table \(separated by “,”\)
-   FROM selects the table that the query will take data from
-   WHERE sets the conditions where the other columns will be searched from
-   AND conjoins two WHERE conditions \(both must be true\)
-   OR conjoins two WHERE conditions \(either can be true\)

## Syntax

Example query:

```
var tableResults = lookup("SELECT column1, column2 FROM tableName WHERE column3 = :key1 OR (column4 != :key2 AND column5 IN :list)", {"key1": "value", "key2":cfg.[singleFieldName], "list":cfg.[multiFieldName]});
```

The first parameter is the SQL-based command string used to query the managed table.

The second parameter is the key-value map to be inserted into the query. The values can be constants, variables, or fields.

The tableResults variable holds the resulting array. This variable cannot be returned itself. Results must be referenced by index \(`tableResults[0], tableResults[1]...`\) and can contain any number of results, or none.

If you receive the error “...Index '0' is out of bounds…” when working with table lookup, you are probably trying to reference an empty array. We recommend running a null check on your table results.

Comparators:

-   **=**

    Is equal to

-   **!=**

    Is not equal to

-   **&gt;**

    Is greater than

-   **&lt;**

    Is less than

-   **&gt;=**

    Is greater than or equal to

-   **IN**

    Is equal to any \(in a set\)


The format for IN works for any collection in the following format:

```
lookup("SELECT column1 FROM table WHERE column2 IN (:options)",{options = cfg. [multi picklistField]});
```

**Related topics**  


[Minimizing table queries](table_queries.md)

[Indexes and natural keys for managed tables](cpq-indexes-and-natural-keys-for-managed-tables.md)

