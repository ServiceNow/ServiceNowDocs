---
title: Integrate Live Connect Drivers with third-party BI tools
description: Configure ServiceNow Live Connect drivers to connect with third-party business intelligence and database tools for direct data access and analysis.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/configure-drivers-bi-tools.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Integrate Live Connect Drivers with third-party BI tools

Configure ServiceNow Live Connect drivers to connect with third-party business intelligence and database tools for direct data access and analysis.

After installing and configuring the Live Connect drivers on your client machine, you can connect them to ODBC and JDBC-compatible tools. Supported tools include Pyramid Analytics, Tableau, Power BI, and DB Visualizer.

You can query ServiceNow data directly from your analytics platform without data export or replication. Before connecting a BI tool, complete the instance and driver setup described in [Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md).

**Note:** The instructions for third-party tools are illustrative. Consult tool-specific documentation for the latest updates.

## General connection considerations

Note the following when connecting third-party BI tools to ServiceNow Live Connect drivers:

-   All connections are read-only. Third-party tools can't modify ServiceNow data through Live Connect.
-   Query performance depends on network connectivity, query complexity, and the amount of data retrieved. Use TOP, LIMIT, and WHERE clauses to filter results and avoid timeout errors.
-   Security permissions are enforced at the ServiceNow level. The connected tool can only access tables and records permitted by the user account's roles and ACL configuration.
-   Strict security is enabled by default. When you query data, Live Connect validates your access at the row level and field level using the ACLs. As a result, you may notice longer query response times. This is expected behavior, consistent with how GlideRecordSecure works. You can assign the **sn\_live\_connect\_privileged\_mode** role to specific accounts \(not globally\) to disable row and field-level ACL checks for those accounts only. Table-level access control remains in effect.
-   The default query timeout is 5 minutes. If your query exceeds this limit, it is terminated.
-   Monitor your SQL query rate to stay within the 500 queries per hour limitation.
-   Consider using separate user accounts \(personal or service accounts\) for different teams or projects to maintain granular access control.

## Supported BI tools

While Power BI Desktop and DB Visualizer are specifically documented examples, the Live Connect drivers support any ODBC or JDBC-compatible application. Other commonly used tools include:

-   Pyramid Analytics
-   Tableau Desktop and Tableau Server
-   Microsoft Excel \(via ODBC connection\)
-   SQL Server Management Studio
-   DBeaver and other universal database tools
-   Custom applications using ODBC or JDBC APIs

Each tool has its own connection configuration interface, but the underlying connection parameters \(instance URL, user account credentials, driver selection\) remain consistent across all platforms.

-   **[Power BI Desktop data import mode and limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/power-bi-import-mode-and-limits.md)**  
The ServiceNow ODBC driver for Power BI Desktop supports only import mode, not DirectQuery. Understanding this distinction helps you plan refresh schedules and avoid dataset size and large-table filtering issues in your reports.
-   **[Connect Power BI Desktop to ODBC driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/connect-power-bi-odbc.md)**  
Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.
-   **[Connect DB Visualizer to JDBC driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/connect-dbvisualizer-jdbc.md)**  
Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

