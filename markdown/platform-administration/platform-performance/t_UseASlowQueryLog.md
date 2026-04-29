---
title: Use a slow query log
description: Administrators can use slow query logs to gain insight into how queries are affecting platform performance. The Slow Queries log aggregates data for similar queries. Use slow query data to evaluate the need for new indexes, changes to existing indexes, or changes to frequent queries.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolving slow queries, Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Use a slow query log

Administrators can use slow query logs to gain insight into how queries are affecting platform performance. The Slow Queries log aggregates data for similar queries. Use slow query data to evaluate the need for new indexes, changes to existing indexes, or changes to frequent queries.

## Before you begin

Role required: admin

## About this task

Queries are similar when they select from the same table and query the same field in the where clause, but search for different values in the field. For example, these queries are aggregated as similar queries.

```
SELECT * FROM sys_user WHERE name="ITIL User"
SELECT * FROM sys_user WHERE name="System Administrator"
```

Aggregating similar query data allows administrators to monitor the performance impact of slow queries and of queries that occur frequently. The log reports data for similar queries where the total execution time exceeds 5 seconds.

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Stats** &gt; **Slow Queries**

2.  Open a query record for more details.

    For a description of the field values in the query record, see [Query record form fields](../reference/query-record-fields.md).

3.  To see what the database is doing to retrieve the data, click **Explain Plan**.

    The query plan is reported in the **MySQL Explain Plan** related list. Use the query plan to evaluate the need for new indexes or changes to existing indexes. For more information, see [MySQL explain plan documentation](http://dev.mysql.com/doc/refman/5.5/en/execution-plan-information.html).

    This feature works on other supported databases, including MongoDB and Oracle.

4.  To generate an index suggestion for a slow query, click **Index Suggestion**.

    For details, see [Generate an index suggestion for a slow query](generate-index-suggestion.md).


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

