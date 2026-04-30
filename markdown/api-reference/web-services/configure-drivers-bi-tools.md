---
title: Integrate SQL API Drivers with third-party BI tools
description: Configure ServiceNow SQL API drivers to connect with third-party business intelligence and database tools for direct data access and analysis.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Integrate SQL API Drivers with third-party BI tools

Configure ServiceNow SQL API drivers to connect with third-party business intelligence and database tools for direct data access and analysis.

After installing and configuring the SQL API drivers on your client machine, you can connect them to third-party business intelligence and database tools. This integration enables you to query ServiceNow data directly from your preferred analytics platforms without requiring data export or replication.

The SQL API supports integration with a wide range of ODBC and JDBC-compatible tools, including Tableau, Power BI, Looker, DB Visualizer, and other standard BI platforms. By connecting these tools to your ServiceNow instance through the SQL API drivers, you can create dashboards, run ad-hoc queries, and perform comprehensive data analysis using live ServiceNow data.

**Important:**

Step-by-step instructions for third-party tools in this guide are illustrative — you must consult tool-specific documentation for latest updates.

## Prerequisites

Before connecting third-party tools to the SQL API drivers, confirm that you have completed the following:

-   The SQL API plugin is installed on your ServiceNow instance.
-   The SQL API is configured on your instance, including Service Account creation, ACL configuration, and IP filter setup.
-   The appropriate SQL API driver \(ODBC or JDBC\) is downloaded and installed on your client machine.
-   The driver is configured with your instance URL, Service Account credentials, and connection parameters.
-   Your client machine's IP address is included in the SQL API IP filter configuration.
-   The Service Account has the necessary roles \(sn\_odbc\_rest\_access or sn\_jdbc\_rest\_access\) and table-level access permissions.

## General connection considerations

When connecting third-party BI tools to ServiceNow SQL API drivers, keep the following considerations in mind:

-   All connections are read-only. Third-party tools cannot modify ServiceNow data through the SQL API.
-   Query performance depends on network connectivity, query complexity, and the amount of data being retrieved. Use WHERE clauses and column selection to optimize performance.
-   Security permissions are enforced at the ServiceNow level. The connected tool can only access tables and records permitted by the Service Account's roles and ACL configuration.
-   Strict security is enabled by default. When you query data, SQL API validates your access at the row level and field level using the ACLs. As a result, you may notice longer query response times. This is expected behavior, consistent with how GlideRecordSecure works. You can add the role **sn\_sql\_api\_privileged\_mode** to disable strict security at the service account level.
-   The default query timeout is 5 minutes. If your query exceeds this limit, it will be terminated.
-   Monitor your SQL query rate to stay within the 500 queries per hour limitation.
-   Consider using Service Account-specific connections for different teams or projects to maintain granular access control.

## Supported BI tools

While Power BI Desktop and DB Visualizer are specifically documented examples in this guide, the SQL API drivers support any ODBC or JDBC-compatible application. Other commonly used tools include:

-   Tableau Desktop and Tableau Server
-   Looker and Looker Studio
-   Microsoft Excel \(via ODBC connection\)
-   SQL Server Management Studio
-   DBeaver and other universal database tools
-   Custom applications using ODBC or JDBC APIs

Each tool has its own connection configuration interface, but the underlying connection parameters \(instance URL, Service Account credentials, driver selection\) remain consistent across all platforms.

-   **[Connect Power BI Desktop to ODBC driver](../task/connect-power-bi-odbc.md)**  
Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.
-   **[Connect DB Visualizer to JDBC driver](../task/connect-dbvisualizer-jdbc.md)**  
Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.

**Parent Topic:**[Access your ServiceNow data using SQL API](../concept/accessing-your-servicenow-data-using-sql-api.md)

