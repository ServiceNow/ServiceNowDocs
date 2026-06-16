---
title: Zero Copy Connectors release notes
description: Version history for the Zero Copy Connectors application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-zero-copy-connectors.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Workflow Data Fabric release notes, ServiceNow Store release notes]
---

# Zero Copy Connectors release notes

Version history for the Zero Copy Connectors application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - May 2026**

    Changes in this release: New subscription profiles are now included.

-   **Version 1.0.4 - May 2026**

    Access data from multiple external sources using Zero Copy Connectors, without copying or duplicating data to your instance.

-   **Version 3.1.0 - April 2026**
    -   Two subscription tiers introduced: ZCC - Primary and ZCC - Advanced.
    -   ZCC - Primary includes all Primary connectors — production-grade, fully supported connectors built and maintained by ServiceNow.
    -   ZCC - Advanced includes all Primary and Community connectors.
-   **Version 3.0.3 - March 2026**
    -   Auth support via OAuth framework \(Snowflake, Oracle, Databricks\)
    -   New connector in Primary which is currently under Preview
        -   Cloudera \(Impala\)
    -   Moved from Community to Primary which is currently under Preview
        -   Iceberg
    -   Delta Lake enhancements \(continued to be in Community\)
    -   Compatible with Australia release
-   **Version 2.1.0 - January 2026**
    -   Support for new primary connectors - Amazon S3, Teradata Connector
    -   JDBC connection pool support for all primary JDBC connectors
    -   Addressed minor bugs to improve the overall product
    -   Zurich Patch 4 and higher
-   **Version 2.0.0 - August 2025**

    Zero Copy Connectors are part of the Workflow Data Fabric. They let the ServiceNow AI Platform access data from external sources directly, without copying any data to the instance. Zero copy connections provide a significant advantage to organizations working with large datasets by ensuring real-time, consistent data access, reducing latency, and improving overall system performance.


**Parent Topic:**[ServiceNow Store - Workflow Data Fabric release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-workflow-data-fabric-highlights.md)

