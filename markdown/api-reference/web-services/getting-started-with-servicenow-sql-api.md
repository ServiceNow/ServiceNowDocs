---
title: Getting started with ServiceNow SQL API
description: The ServiceNow SQL API provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Getting started with ServiceNow SQL API

The ServiceNow SQL API provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.

The ServiceNow SQL API plugin uses ServiceNow web services support for a query-only interface. By default, the plugin supports only SELECT statements, allowing external applications to query authorized tables. It permits a limited set of additional SQL commands and enables you to compose more complex queries to retrieve only relevant data.

## What you can achieve with SQL API

With the SQL API, you can:

-   Connect Your BI Tools: Integrate standard BI platforms such as Power BI, DBeaver, DBvisualizer, and other ODBC/JDBC-compatible tools directly with your ServiceNow data.
-   Query Data Securely: Access data through read-only operations that help avoid unintended modifications to your ServiceNow records. Allow access only to the desired tables.
-   Eliminate Data Duplication: Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Combine Data Sources: Merge your ServiceNow data with external datasets in your analytical platforms for comprehensive analysis.
-   Optimize Data Transfer: Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

## How SQL API works

When you connect your BI tool to your ServiceNow instance through the SQL API, you establish a standard database connection using ODBC or JDBC APIs. After connecting, you can write SQL queries to retrieve data from your ServiceNow tables and fields. The API processes your queries and returns results in standard tabular format, which your BI tool can then visualize, analyze, or export.

## Pass-through query support

The SQL API supports pass-through queries, that means you can write SQL statements that execute directly on your ServiceNow data. This enables you to:

-   Apply WHERE clauses to filter data at the source.
-   Perform aggregations \(COUNT, SUM, AVG, etc.\) on the ServiceNow side.
-   Join multiple ServiceNow tables in a single query. The query engine only supports INNER and LEFT OUTER joins currently.
-   Limit result sets to reduce data transfer.

By processing queries at the source, you reduce the amount of data transferred over the network and improve overall query performance.

## Security and access control

Your current ServiceNow security model still applies when you access the SQL API. The API implements the ServiceNow ACL model, which means:

-   You can only access data that your ServiceNow role and permissions allow.
-   All identity and access management protocols are enforced at the API level.
-   Your queries follow table-level, row level, field level, query level, and record-level security rules.
-   By default, the SQL API checks access at the table, row, and field level for every query, following ServiceNow's secure-by-default approach. The SQL API validates all ACLs in your instance record by record, which may result in longer response times. This is expected.

    If your use case does not require row and field-level checks — for example, a Business Intelligence integration — you can turn them off by assigning the `sn_sql_api_privileged_mode` role to the service account. Table-level ACL checks always remain in effect and cannot be turned off.

-   Authentication is required for all connections.

Additionally, the SQL API is read-only by design. You cannot perform INSERT, UPDATE, or DELETE operations through this interface. This helps that your analytical work cannot accidentally modify production data.

## What to explore next

To learn more about configuring and using SQL API, see:

-   [SQL API architecture](sql-api-architecture.md)
-   [Configuring SQL API](configuring-sql-api.md)
-   [Install SQL API plugin on your ServiceNow instance](install-sql-api-plugin.md)
-   [Common use cases for SQL API](common-use-cases-for-sql-api.md)
-   [SQL API reference information](../reference/troubleshooting.md)

-   **[SQL API architecture](sql-api-architecture.md)**  
The SQL API architecture demonstrates how the SQL API plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.
-   **[Supported SQL functions](../reference/supported-sql-functions.md)**  
Common SQL functions used in SQL API for querying and analyzing incident data.
-   **[Common use cases for SQL API](common-use-cases-for-sql-api.md)**  
The SQL API supports business intelligence reporting, ad-hoc data analysis, and custom report development.

**Parent Topic:**[Access your ServiceNow data using SQL API](accessing-your-servicenow-data-using-sql-api.md)

