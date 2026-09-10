---
title: Getting started with ServiceNow Live Connect
description: The ServiceNow Live Connect provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/getting-started-with-servicenow-sql-api.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 5
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Getting started with ServiceNow Live Connect

The ServiceNow Live Connect provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.

The ServiceNow Live Connect plugin uses ServiceNow web services support for a query-only interface. By default, the plugin supports only SELECT statements, allowing external applications to query authorized tables. It permits a limited set of additional SQL commands and enables you to compose more complex queries to retrieve only relevant data.

## What you can achieve with Live Connect

With the Live Connect, you can:

-   Optimize data transfer: Write targeted SQL queries to retrieve only the data you need, reducing network overhead for data pipeline and data transformation, and improving performance.
-   Connect your BI tools: Integrate standard BI platforms such as Pyramid Analytics, Power BI, Tableau, DBeaver, DBvisualizer, and other ODBC/JDBC-compatible tools directly with your ServiceNow data.
-   Query data securely: Access data through read-only operations that help avoid unintended modifications to your ServiceNow records. Allow access only to the desired tables.
-   Eliminate data duplication: Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Combine data sources: Merge your ServiceNow data with third-party datasets in your analytical platforms for comprehensive analysis.

## How Live Connect works

When you connect your BI tool to your ServiceNow instance through the Live Connect, you establish a standard database connection using ODBC or JDBC APIs. After connecting, you can write SQL queries to retrieve data from your ServiceNow tables and fields.

The API processes your queries and returns results in standard tabular format, which your BI tool can then visualize, analyze, or export.

## Pass-through query support

Live Connect supports pass-through queries, meaning you can write SQL statements that run directly on your ServiceNow data. This enables you to:

-   Apply WHERE clauses to filter data at the source.
-   Perform aggregations \(COUNT, SUM, AVG, etc.\) on the ServiceNow side.
-   Join multiple ServiceNow tables in a single query. The query engine supports INNER and LEFT OUTER joins.
-   Limit result sets to reduce data transfer.

By processing queries at the source, you reduce the amount of data transferred over the network and improve overall query performance.

## Supported SQL functions

Live Connect does not support the full ANSI SQL standard. The query engine supports a subset of SQL functions optimized for read-only data access and analysis.

For a complete list of supported SQL functions with examples and usage guidelines, see [Supported SQL functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/supported-sql-functions.md).

## Security and access control

Your current ServiceNow security model still applies when you access data using Live Connect. The API implements the ServiceNow ACL model, which means:

-   You can only access data that your ServiceNow role and permissions allow.
-   All identity and access management protocols are enforced at the API level.
-   Your queries follow table-level, row level, field level, and query level rules.
-   Live Connect checks access at the table, row, and field level for every query, following ServiceNow's secure-by-default approach. The Live Connect validates all ACLs in your instance record by record, which may result in longer response times. This is expected.

    If your use case does not require row and field-level checks, you can turn them off by assigning the **sn\_live\_connect\_privileged\_mode** role to the user account \(personal or service account\). Only users with the security\_admin role can assign this role.

    Table-level ACL checks remain in effect and can't be turned off.

-   Authentication is required for all connections.

Additionally, Live Connect is read-only by design. You can't perform INSERT, UPDATE, or DELETE operations through this interface. This helps prevent accidental modification of production data.

## Authentication methods

Live Connect supports multiple authentication methods to meet various security requirements and conformance standards.

**Note:** OAuth 2.0 support is available starting with Australia Patch6.

|Authentication Encryption Method|Recommended use case|
|--------------------------------|--------------------|
|Basic Authentication|SSL/TLS \(traffic only\)|Legacy systems; non-regulated environments.|
|OAuth 2.0|TLS 1.2+|Client credentials and authorization code flows. Provides token-based access without exposing credentials directly.|
|Client Certificate \(mTLS\)|TLS 1.2+ with mutual authentication|Recommended for service-to-service integration and highest security requirements. Requires certificate management infrastructure.|

## Third-party client authentication requirements

Any third-party BI tool, database client, or application connecting to ServiceNow via Live Connect must support the same authentication and encryption methods as configured on your ServiceNow instance.

Before integrating a third-party tool, verify the following:

-   Your selected authentication method \(OAuth 2.0 or Client Certificates for FedRAMP conformance\)
-   TLS 1.2 or higher encryption
-   Certificate validation \(if using mTLS\)
-   Token refresh mechanisms \(if using OAuth\)

Consult your BI tool's documentation or contact your vendor to confirm compatibility before configuring Live Connect connections.

## What to explore next

To learn more about configuring and using Live Connect, see:

-   [Live Connect architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/sql-api-architecture.md)
-   [Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)
-   [Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-sql-api-plugin.md)
-   [Use cases for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/common-use-cases-for-sql-api.md)
-   [Live Connect reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/troubleshooting.md)

-   **[Live Connect architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/sql-api-architecture.md)**  
Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.
-   **[Use cases for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/common-use-cases-for-sql-api.md)**  
 Live Connect supports business intelligence \(BI\) reporting, ad-hoc data analysis, and custom report development.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

