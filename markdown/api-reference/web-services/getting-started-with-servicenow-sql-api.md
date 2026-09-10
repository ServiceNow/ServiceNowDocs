---
title: Getting started with ServiceNow Live Connect
description: The ServiceNow Live Connect provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/getting-started-with-servicenow-sql-api.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Getting started with ServiceNow Live Connect

The ServiceNow Live Connect provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.

The ServiceNow Live Connect plugin uses ServiceNow web services support for a query-only interface. By default, the plugin supports only SELECT statements, allowing external applications to query authorized tables. It permits a limited set of additional SQL commands and enables you to compose more complex queries to retrieve only relevant data.

## What you can achieve with Live Connect

With the Live Connect, you can:

-   Connect your BI tools: Integrate standard BI platforms such as Power BI, DBeaver, DBvisualizer, and other ODBC/JDBC-compatible tools directly with your ServiceNow data.
-   Query data securely: Access data through read-only operations that help avoid unintended modifications to your ServiceNow records. Allow access only to the desired tables.
-   Eliminate data duplication: Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Combine data sources: Merge your ServiceNow data with external datasets in your analytical platforms for comprehensive analysis.
-   Optimize data transfer: Write targeted SQL queries to retrieve only the data you need, reducing network overhead for data pipeline and data transformation, and improving performance.

## How Live Connect works

When you connect your BI tool to your ServiceNow instance through the Live Connect, you establish a standard database connection using ODBC or JDBC APIs. After connecting, you can write SQL queries to retrieve data from your ServiceNow tables and fields.

The API processes your queries and returns results in standard tabular format, which your BI tool can then visualize, analyze, or export.

## Pass-through query support

The Live Connect supports pass-through queries, meaning you can write SQL statements that execute directly on your ServiceNow data. This enables you to:

-   Apply WHERE clauses to filter data at the source.
-   Perform aggregations \(COUNT, SUM, AVG, etc.\) on the ServiceNow side.
-   Join multiple ServiceNow tables in a single query. The query engine supports only INNER and LEFT OUTER joins.
-   Limit result sets to reduce data transfer.

By processing queries at the source, you reduce the amount of data transferred over the network and improve overall query performance.

## Security and access control

Your current ServiceNow security model still applies when you access the Live Connect. The API implements the ServiceNow ACL model, which means:

-   You can only access data that your ServiceNow role and permissions allow.
-   All identity and access management protocols are enforced at the API level.
-   Your queries follow table-level, row level, field level, query level, and record-level security rules.
-   By default, the Live Connect checks access at the table, row, and field level for every query, following ServiceNow's secure-by-default approach. The Live Connect validates all ACLs in your instance record by record, which may result in longer response times. This is expected.

    If your use case does not require row and field-level checks — for example, a Business Intelligence integration — you can turn them off by assigning the `sn_sql_api_privileged_mode` role to the service account. Table-level ACL checks always remain in effect and cannot be turned off.

-   Authentication is required for all connections.

Additionally, the Live Connect is read-only by design. You cannot perform INSERT, UPDATE, or DELETE operations through this interface. This helps prevent accidentally modify production data.

## What to explore next

To learn more about configuring and using Live Connect, see:

-   [Live Connect architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/sql-api-architecture.md)
-   [Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configuring-sql-api.md)
-   [Install Live Connect plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-sql-api-plugin.md)
-   [Common use cases for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/common-use-cases-for-sql-api.md)
-   [Live Connect reference information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/troubleshooting.md)

-   **[Live Connect architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/sql-api-architecture.md)**  
The Live Connect architecture demonstrates how the Live Connect plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.
-   **[Supported SQL functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/supported-sql-functions.md)**  
Common SQL functions used in Live Connect for querying and analyzing incident data.
-   **[Common use cases for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/common-use-cases-for-sql-api.md)**  
The Live Connect supports business intelligence reporting, ad-hoc data analysis, and custom report development.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

