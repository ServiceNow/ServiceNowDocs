---
title: SQL API architecture
description: The SQL API architecture demonstrates how the SQL API plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# SQL API architecture

The SQL API architecture demonstrates how the SQL API plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.

The SQL API architecture provides a high-level view of how external Business Intelligence \(BI\) tools and data analysis platforms connect to your ServiceNow instance through standard database APIs. The architecture provides secure, read-only access to your ServiceNow data while maintaining all security controls and access restrictions.

## Architecture overview

The SQL API uses ServiceNow web services to provide a query-only interface. This architecture enables direct connections from ODBC and JDBC-compatible tools to your ServiceNow data without data export or replication.

The following diagram illustrates the high‑level architecture of how the SQL API connects external BI tools to ServiceNow tables via ODBC and JDBC drivers, while enforcing security and access controls.

![Architecture diagram showing SQL API interaction with ServiceNow system components](../image/sql-api-architechture.png "SQL API Architecture diagram")

## Key architectural components

The SQL API architecture consists of the following key components:

-   **Client applications**

    External BI tools and data analysis platforms such as Power BI, DBeaver, and DBvisualizer that connect using ODBC or JDBC protocols.

-   **ODBC/JDBC drivers**

    Industry-standard database drivers that enable client applications to establish connections and execute SQL queries against ServiceNow data.

-   **ServiceNow Instance**

    Inside the ServiceNow instance, three layers handle the request:

    -   Security layer: In this layer, four controls are applied in sequence:
        1.  IP Access Policy
        2.  Rate Limit
        3.  Auth + Role check
        4.  Encryption
    -   REST layer: There are separate dedicated services for each driver \(ODBC REST Service and JDBC REST Service\), both restricted to SELECT-only queries and rate limited, accessible only by the driver internally.
    -   Database tier: Queries reach the Primary DB first \(read-only, used as fallback if no replica\), but are preferably routed to a Read Replica, which isolates BI workload from the primary database and handles all JDBC/ODBC SELECTs. You must configure a Read Replica to route the SQL API queries. For more information, see [Route SQL API calls to Read Replica](../task/routing-sql-api-calls-to-read-replica.md).

## How the architecture works

When you connect your BI tool to ServiceNow through the SQL API, the following process occurs:

1.  Your BI tool establishes a standard database connection using either ODBC or JDBC APIs.
2.  The connection request is authenticated against ServiceNow user credentials configured for SQL API access.
3.  Once authenticated, you can write SQL queries to retrieve data from authorized ServiceNow tables and fields.
4.  The SQL API processes your queries through the security services layer, applying all security controls and access restrictions.
5.  Query results are returned in standard tabular format, which your BI tool can visualize, analyze, or export.

**Parent Topic:**[Getting started with ServiceNow SQL API](getting-started-with-servicenow-sql-api.md)

