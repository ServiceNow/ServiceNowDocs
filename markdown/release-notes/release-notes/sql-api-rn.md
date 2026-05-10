---
title: SQL API Release Notes
description: The ServiceNow SQL API enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. SQL API is only available with RaptorDB Professional.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-03"
reading_time_minutes: 2
---

# SQL API Release Notes

The ServiceNow® SQL API enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. SQL API is only available with RaptorDB Professional.

## SQL API highlights for the Australia release

-   Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Access data using read-only operations to avoid unintended changes to your ServiceNow records. Allow access only to the desired tables.
-   Integrate standard BI platforms such as Power BI, DBvisualizer, and other ODBC or JDBC-compatible tools directly with your ServiceNow data.
-   Merge your ServiceNow data with external datasets in your analytical platforms for comprehensive analysis.
-   Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

For more information, see [Access your ServiceNow data using SQL API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md).

**Important:** SQL API is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important upgrade information for SQL API

ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Professional entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see [Configuring SQL API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md).

## SQL API features

-   **[Access your ServiceNow data using SQL API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)**

    The ServiceNow Store SQL API enables you to access your ServiceNow Store instance data through ODBC and JDBC drivers. Using SQL API, you can directly access your instance data from third-party BI tools and other data analysis applications without exporting or replicating your data. The ServiceNow SQL API plugin uses ServiceNow web services support for a query-only interface.


## Activation information

SQL API is a ServiceNow feature that is available with the activation of SQL API plugin \(com.glide.rest.sqlapiserver\). The ServiceNow instance requires RaptorDB Professional entitlement to activate the SQL API server-side plugin. The SQL API drivers are freely available for download by anyone with a valid account to the ServiceNow Store. However, the SQL API client would not be able to connect to the ServiceNow instance until the server-side plugin is enabled. For more information, see [Install SQL API plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-sql-api-plugin.md).

## Plugin information

-   **New plugin**

    The following plugin is new in Australia:

    SQL API \(com.glide.rest.sqlapiserver\): Unified installer for the ServiceNow ODBC and JDBC server‑side plugin. This plugin works with ServiceNow client‑side drivers to enable clients to query and retrieve data from a ServiceNow instance using ODBC and JDBC API standards. You can download and install the client‑side drivers on your client machines from the ServiceNow Store.


## Additional requirements

You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the SQL API queries. You can download the ODBC and JDBC drivers from ServiceNow Store.

## Related ServiceNow applications and features

-   **[RaptorDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/raptordb.md)**

    RaptorDB Professional is a licensed database that supports ServiceNow AI Platform generative AI and machine-scale data use cases, user growth, applications, workloads, and analytics.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

