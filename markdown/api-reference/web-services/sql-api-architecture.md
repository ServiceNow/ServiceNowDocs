---
title: Live Connect architecture
description: Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/sql-api-architecture.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Live Connect architecture

Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.

## Architecture overview

Live Connect uses ServiceNow web services to provide a query-only interface. This architecture enables direct connections from ODBC and JDBC-compatible tools to your ServiceNow data without data export or replication.

The diagram illustrates how the Live Connect connects external BI tools to ServiceNow tables through ODBC and JDBC drivers, with security and access controls applied at the connection layer.

\[Omitted image "sql-api-architechture.png"\] Alt text: Architecture diagram showing SQL API interaction with ServiceNow system components

## Key architectural components

The Live Connect architecture consists of the following key components:

-   **Client applications**

    External BI tools and data analysis platforms such as Pyramid Analytics,Power BI, Tableau, DBeaver, and DBvisualizer that connect using ODBC or JDBC protocols.

-   **ODBC/JDBC drivers**

    Industry-standard database drivers that enable client applications to establish connections and run the SQL queries against ServiceNow data.

-   **ServiceNow Instance**

    Three layers within the ServiceNow instance process each request:

<table><thead><tr><th>

Layer

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security layer

</td><td>

Six controls are applied in sequence: -   IP Access Policy
-   Rate Limit
-   Auth + Role check
-   egress\_sql ACL
-   Strict Security Mode
-   WDF Token Metering


</td></tr><tr><td>

REST layer

</td><td>

Separate dedicated services exist for each driver \(ODBC REST Service and JDBC REST Service\). Both services are restricted to SELECT-only queries and rate limited, and are accessible only by the driver internally.

</td></tr><tr><td>

Database tier

</td><td>

Queries reach the primary database first \(read-only, used as fallback if no replica\), but are preferably routed to a read replica. The read replica isolates BI workload from the primary database and handles all JDBC/ODBC SELECTs.

</td></tr></tbody>
</table>
## How the architecture works

When you connect your BI tool to ServiceNow through Live Connect, the following process occurs:

1.  Your BI tool establishes a standard database connection using either ODBC or JDBC APIs.
2.  The connection request is authenticated against ServiceNow user credentials configured for Live Connect access.
3.  After authentication, you can write SQL queries to retrieve data from authorized ServiceNow tables and fields.
4.  The Live Connect processes your queries through the security services layer, applying all security controls and access restrictions.
5.  Query results are returned in standard tabular format, which your BI tool can visualize, analyze, or export.

**Parent Topic:**[Getting started with ServiceNow Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/getting-started-with-servicenow-sql-api.md)

