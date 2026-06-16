---
title: Service Graph Connector for Microsoft SCCM release notes
description: Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Microsoft SCCM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-microsoft-sccm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Microsoft SCCM release notes

Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Microsoft SCCM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.8.3 - June 2026**

    Fixed the issue with creating connections.

-   **Version 3.8.1 - February 2026**
    -   Fixed:
        -   Fixed the last run datetime value for the SG-SCCM Computer Identity data source.
        -   Fixed the SQL in the SG-SCCM Computer Identity data source to handle unknown TimeKey column errors.
        -   Fixed the SCCMMultiDataSourceUtil script to handle subqueries.
-   **Version 3.8.0 - December 2025**
    -   Fixed:
        -   Fixed the issue with SQL query for the Computer Identity data source.
        -   Mapped discovery source for samp\_sw\_usage.
-   **Version 3.7.0 - September 2025**

    New: Added support for SCCM airgap scenario. An airgap is a security measure that involves isolating a computer or network to prevent it from establishing an external connection. In SG-SCCM, a solution is developed to pull data for a highly secure zone via PowerShell and process it through SG-SCCM.

-   **Version 3.6.0 - November 2024**

    New: Onboarded connector to SGC Central.

-   **Version 3.4.2 - March 2024**
    -   Fixed:
        -   The Last Scanned field is now populated in the Software Installation \[cmdb\_sam\_sw\_install\] table for the SG-SCCM Software AI data source
        -   Menus intended for admin users in the application navigator will no longer appear for non-admin users
        -   Fixed encoded URLs during the creation of data sources
        -   Updated the SQL query for the v\_GS\_CCM\_RECENTLY\_USED\_APPSSCCM table to improve the performance
        -   The serial numbers in the Serial Number \[cmdb\_serial\_number\] table now use the Cleanse Serial Number RTE transform operation
-   **Version 3.4.0 - September 2023**
    -   New:
        -   Support for the common connection framework
        -   Implemented the cleanse serial number operation for serial numbers
    -   Fixed: Tuned the SQL query in the SG-SCCM Software data source for the last used software
-   **Version 3.3.0 - March 2023**
    -   Fixed:
        -   Removed dots from field names so they are equivalent to the path. Dots in the field names prevented them from appearing on the user interface.
        -   Fixed issue updating SG-SCCM SAMP SW USAGE record for certain products.
        -   Fixed issue aggregating usage time when multiple records exist with the same combination of filename and related fields.
        -   Removed hard-coded value to provide flexibility to run software usage for a given month.
-   **Version 3.2.1 - May 2022**
    -   Change:
        -   Use Raw value of Publisher, Display Name, and Version for Software Source Native key instead of cleansed value
        -   Move the left navigation items of SCCM to the Integration Commons Service Graph Connectors navigation menu
-   **Version 3.0.6 - January 2022**
    -   Fixed: When a user runs the "Test Load 20 Records" and a MID server is used, the last run date time is set. Steps added to the Guided Setup that users need to clear the last run date time to force a full import on the first run.
    -   Note: Upgrade of existing 2.x version to 3.x will work as is but changes to credential and connections will require going through guided setup again.
-   **Version 3.0.4 - December 2021**
    -   New: Support for connecting with multiple SCCM instance using new/updated guided setup process
    -   Note: Upgrade of existing 2.x version to 3.x will work as-is, but changes to credential and connections will require going through guided setup again.
-   **Version 2.5.0 - September 2021**

    New: Added support for Computer Identity: Asset Tag, Assigned On, DNS Domain and Organizational Unit \(OU\)

-   **Version 2.4.2 - August 2021**

    Changed: Software titles incorrectly removed from CMDB when title contained escaped characters \(e.g. "&amp;amp"\).

-   **Version 2.4.1 - July 2021**

    Changed: Implemented a new data source to populate cmdb\_ci\_computer.last\_discovered with LastHWScan from SCCM to reflect the last time SCCM scanned the computer.

-   **Version 2.3.1 - May 2021**
    -   New:
        -   Remove licensing restrictions.
        -   Support Subscription Software rules for "last used" usage model.
        -   Populate source\_recency\_timestamps from source data.
    -   Fixed: Updated handling of removed software to take into account multiple computer identity records for a single computer CI in the CMDB.
-   **Version 2.1.6 - March 2021**

    Fixed: Software installation records were incorrect under certain circumstances.

-   **Version 2.1.1 - September 2020**
    -   The Microsoft SCCM integration is a one direction import of SCCM data into the ServiceNow Configuration Management Database \(CMDB\).
    -   Scheduled imports bring relevant SCCM data into the ServiceNow instance from an SQL Server database and map the data to the appropriate tables in the CMDB. You can configure either a full or incremental data import. The import is achieved using a JDBC connection via the MID Server. The integration keeps the ServiceNow CMDB synchronized with the SCCM SQL Server database, so that only relevant data is imported from the SCCM database to the CMDB. The SCCM database is considered an authoritative source and is not written to.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

