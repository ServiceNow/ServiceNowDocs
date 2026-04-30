---
title: Using disjunctions in complex queries
description: ServiceNow performs conjunction \(AND\) statements before disjunction \(OR\) statements in a query.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Using disjunctions in complex queries

ServiceNow performs conjunction \(AND\) statements before disjunction \(OR\) statements in a query.

When you create a complex query that combines AND and OR conditions, you must use parenthesis around disjunctions to ensure proper grouping of query elements.

## Example

Find all closed incidents \(state = 6\) that are either Priority 1 or Priority 2.

-   Correct query \(with parentheses\):

    ```
    (priority = 1 || priority = 2) && state = 6
    ```

    This query returns all closed incidents where the priority is 1 OR 2.

-   Incorrect query \(without parentheses\):

    ```
    priority = 1 || priority = 2 && state = 6
    ```

    Without parentheses, this query is evaluated as: priority = 1 OR \(priority = 2 AND state = 6\). This returns ALL Priority 1 incidents regardless of state, plus only the closed Priority 2 incidents.


<table id="table_kfj_vgn_yhc"><thead><tr><th>

Query

</th><th>

Evaluated as

</th><th>

Result

</th></tr></thead><tbody><tr><td>

```
(priority = 1 || priority = 2) && state = 6
```

</td><td>

\(P1 OR P2\) AND Closed

</td><td>

Closed P1 and P2 incidents only

</td></tr><tr><td>

```
priority = 1 || priority = 2 && state = 6
```

</td><td>

P1 OR \(P2 AND Closed\)

</td><td>

ALL P1 incidents + only closed P2

</td></tr></tbody>
</table>Always use parentheses around OR conditions when combining them with AND conditions. This ensures your query returns the expected results.

**Parent Topic:**[Working with database views for reporting](c_DatabaseViews.md)

**Related topics**  


[Database view creation](../task/c_CreatingDatabaseViews.md)

[Displaying function results in a database view](../task/displaying-function-results-in-a-database-view.md)

[Database views in the base system](../reference/r_DatabaseViewsInTheBaseSystem.md)

