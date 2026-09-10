---
title: Live Connect architecture
description: Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/sql-api-architecture.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Live Connect architecture

Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.

## Architecture overview

Live Connect uses ServiceNow web services to provide a query-only interface. This architecture enables direct connections from ODBC and JDBC-compatible tools to your ServiceNow data without data export or replication.

The diagram shows the high‑level architecture of how the Live Connect connects external BI tools to ServiceNow tables via ODBC and JDBC drivers, while enforcing security and access controls.

\[Omitted image "sql-api-architechture.png"\] Alt text: Architecture diagram showing SQL API interaction with ServiceNow system components

## Key architectural components

The Live Connect architecture consists of the following key components:

-   **Client applications**

    External BI tools and data analysis platforms such as Pyramid Analytics,Power BI, Tableau, DBeaver, and DBvisualizer that connect using ODBC or JDBC protocols.

-   **ODBC/JDBC drivers**

    Industry-standard database drivers that enable client applications to establish connections and execute SQL queries against ServiceNow data.

-   **ServiceNow Instance**

    Inside the ServiceNow instance, three layers handle the request:

    Security layer: In this layer, six controls are applied in sequence:

    1.  IP Access Policy
    2.  Rate Limit
    3.  Auth + Role check
    4.  egress\_sql ACL
    5.  Strict Security Mode
    6.  WDF Token Metering
    REST layer: There are separate dedicated services for each driver \(ODBC REST Service and JDBC REST Service\). Both services are restricted to SELECT-only queries and rate limited. They are accessible only by the driver internally.

    Database tier: Queries reach the Primary DB first \(read-only, used as fallback if no replica\), but are preferably routed to a Read Replica. The Read Replica isolates BI workload from the primary database and handles all JDBC/ODBC SELECTs.


## How the architecture works

When you connect your BI tool to ServiceNow through the Live Connect, the following process occurs:

1.  Your BI tool establishes a standard database connection using either ODBC or JDBC APIs.
2.  The connection request is authenticated against ServiceNow user credentials configured for Live Connect access.
3.  After authentication, you can write SQL queries to retrieve data from authorized ServiceNow tables and fields.
4.  The Live Connect processes your queries through the security services layer, applying all security controls and access restrictions.
5.  Query results are returned in standard tabular format, which your BI tool can visualize, analyze, or export.

**Parent Topic:**[Getting started with ServiceNow Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/getting-started-with-servicenow-sql-api.md)

