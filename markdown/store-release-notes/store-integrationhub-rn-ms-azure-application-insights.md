---
title: Microsoft Azure Application Insights spoke release notes
description: Version history for the Integration Hub Microsoft Azure Application Insights spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-azure-application-insights.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Application Insights spoke release notes

Version history for the Integration Hub Microsoft Azure Application Insights spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   New connection and credential alias Microsoft Azure Application Insights \(sn\_ms\_appin\_spoke.Microsoft\_Azure\_Application\_Insights\)
        -   Authentication Template for easy spoke setup
        -   New actions that make use of new connection and credential alias
            -   Event Management: Look up Event \(look\_up\_event\),Look up Events by Type \(look\_up\_events\_by\_type\),Look up OData Metadata \(look\_up\_odata\_metadata\)
            -   Metric Management: Look up Metric \(look\_up\_metric\),Look up Metric Metadata \(look\_up\_metric\_metadata\),Look up Metrics \(look\_up\_metrics\)
            -   Query Management: Execute Query \(execute\_query\),Look up Query \(look\_up\_query\)
    -   Removed:
        -   Deprecated old credential alias Azure\_Application\_Insights \(sn\_ms\_appin\_spoke.Azure\_Application\_Insights\)
        -   Deprecated actions that make use of old credential alias
            -   Event Management: Get By Type \(Deprecated\) \(get\_by\_type\),Get Event \(Deprecated\) \(get\_event\),Get Odata Metadata \(Deprecated\) \(get\_odata\_metadata\)
            -   Metric Management: Get Metadata \(Deprecated\) \(get\_metadata\),Get Metrics \(Deprecated\) \(get\),Get Multiple \(Deprecated\) \(get\_multiple\)
            -   Query Management: Execute Query \(Deprecated\) \(execute\),Get Query \(Deprecated\) \(get\_query\)
-   **Version 1.0.3 - May 2023**

    Changed: Spoke name.

-   **Version 1.0.2 - September 2022**

    Fixed: Patch version of Azure Application Insights Spoke for IntegrationHub. This version includes a fix to improve the installation performance of the spoke.&lt;

-   **Version 1.0.1 - October 2020**

    Provides actions to retrieve events and metrics, and run queries with Azure Application Insights


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

