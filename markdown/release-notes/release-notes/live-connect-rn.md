---
title: Live Connect release notes
description: Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-31"
reading_time_minutes: 4
keywords: [Live Connect, SQL API, ODBC, JDBC, OAuth, analytics, Live Connect, SQL API, ODBC, JDBC, OAuth, analytics, Live Connect, SQL API, ODBC, JDBC, OAuth, analytics]
---

# Live Connect release notes

Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.

## About Live Connect

-   Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Access data using read-only operations to avoid unintended changes to your ServiceNow records. Allow access only to the desired tables.
-   Integrate standard BI platforms such as Power BI, DBvisualizer, and other ODBC or JDBC-compatible tools directly with your ServiceNow data.
-   Merge your ServiceNow data with external datasets in your analytical platforms for comprehensive analysis.
-   Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

For more information, see [Access your ServiceNow data using Live Connect](https://www.servicenow.com/docs/r/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.html).

**Important:** Live Connect is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

## Activation and other requirements

-   **Activation information**

    Live Connect is a ServiceNow feature that is available with the activation of Live Connect plugin \(com.glide.rest.sqlapiserver\). The ServiceNow instance requires RaptorDB Professional entitlement to activate the Live Connect server-side plugin.

    The Live Connect client drivers are freely available for download by anyone with a valid account to the ServiceNow Store. However, the Live Connect client would not be able to connect to the ServiceNow instance until the server-side plugin is enabled. For more information, see .

-   **Upgrade information**

    ServiceNow provided customers with a free SOAP-based ODBC client. If you have an active RaptorDB Professional entitlement, you can migrate to the REST-based Live Connect client by completing the required configuration on both the server and client sides. For more information, see .

-   **Browser requirements**

    Live Connect is a backend connectivity layer with no browser-specific requirements. Browser compatibility depends on the third-party client tools used to connect to Live Connect.

-   **Additional requirements**

    You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the Live Connect queries. You can download the ODBC and JDBC drivers from ServiceNow Store.


## Accessibility and localization

-   **Accessibility information**
    -   Live Connect is a backend connectivity layer with no direct user interface.
    -   Accessibility of query results depends on the third-party client tools used to connect to Live Connect.
-   **Localization information**

    Live Connect operates independently of language settings. Data returned through Live Connect reflects the language settings of the queried tables.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## September 2026

Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.

### What's new

-   ****

    The ServiceNow Store Live Connect enables you to access your ServiceNow instance data through ODBC and JDBC drivers. Using Live Connect, you can directly access your instance data from third-party BI tools and other data analysis applications without exporting or replicating your data. The ServiceNow Live Connect plugin uses ServiceNow web services support for a query-only interface.

-   ****

    Connect third-party ODBC and JDBC clients to ServiceNow using OAuth credentials to meet FedRamp compliance requirements and enable secure multi-factor authentication workflows. OAuth provides modern, encrypted authentication aligned with security standards and reduces credential exposure in transit.

-   **Pyramid Analytics integration**

    Use Pyramid Analytics as your analytics layer for ServiceNow operational data with native SQL connectivity through JDBC drivers. Build interactive dashboards and reports without data duplication and leverage advanced analytics capabilities on live data.


### What's changed

-   **Product name updated from SQL API to Live Connect**

    The product name was updated from SQL API to Live Connect throughout the user interface, including all menus, forms, configuration pages, and labels.


### Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Live Connect \(com.glide.rest.sqlapiserver\): Unified installer for the ServiceNow ODBC and JDBC server‑side plugin. This plugin works with ServiceNow client‑side drivers to enable clients to query and retrieve data from a ServiceNow instance using ODBC and JDBC API standards. You can download and install the client‑side drivers on your client machines from the ServiceNow Store.


## Australia

Live Connect enables RaptorDB Professional users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. Live Connect is only available with RaptorDB Professional.

### What's new

The following features are new in this release.

### What's changed

The following UI changes are in this release.

