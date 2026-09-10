---
title: SQL API Release Notes
description: The ServiceNow Live Connect enables RaptorDB Pro users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Pro. The ServiceNow Live Connect enables RaptorDB Pro users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Pro.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2026-03-09"
reading_time_minutes: 2
---

# SQL API Release Notes

The ServiceNow® Live Connect enables RaptorDB Pro users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Pro.

## About SQL API

-   Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Access data using read-only operations to prevent unintended changes to your ServiceNow records. Allow access only to the desired tables.
-   Integrate standard BI platforms such as Power BI, DBvisualizer, and other ODBC/JDBC-compatible tools directly with your ServiceNow data.
-   Merge your ServiceNow data with third-party datasets in your data lakes and analytical platforms for comprehensive analysis.
-   Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

For more information, see .

## Activation and other requirements

**Important:** Live Connect is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Live Connect is a ServiceNow feature that is available with the activation of Live Connect plugin \(com.glide.rest.sqlapiserver\). The ServiceNow instance requires RaptorDB Pro entitlement to activate the SQL API server-side plugin. The SQL API drivers are freely available for download by anyone with a valid account to the ServiceNow Store. However, the SQL API client would not be able to connect to the ServiceNow instance until the server-side plugin is enabled. For more information, see .

-   **Upgrade information**

    ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Pro entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see .

-   **Additional requirements**

    You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the Live Connect queries. You can download the ODBC and JDBC drivers from ServiceNow store.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-admin-rn-landing.md)

## Zurich

The ServiceNow® Live Connect enables RaptorDB Pro users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Pro.

### What's new

-   ****

    The ServiceNow Live Connect enables you to access your ServiceNow instance data through ODBC and JDBC drivers. Using SQL API, you can directly access your instance data from third-party BI tools and other data analysis applications without exporting or replicating your data. The ServiceNow Live Connect plugin uses ServiceNow web services support for a query-only interface.


### Plugin information

-   **New plugins**

    The following plugin is new in Zurich:

    Live Connect \(com.glide.rest.sqlapiserver\): Unified installer for the ServiceNow ODBC and JDBC server‑side plugin. This plugin works with ServiceNow client‑side drivers to enable clients to query and retrieve data from a ServiceNow instance using ODBC and JDBC API standards. You can download and install the client‑side drivers on your client machines from the ServiceNow Store.


