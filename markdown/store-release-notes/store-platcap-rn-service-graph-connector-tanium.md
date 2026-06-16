---
title: Service Graph Connector for Tanium release notes
description: Version history for the Service Graph Connector for Tanium integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-tanium.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Tanium release notes

Version history for the Service Graph Connector for Tanium integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.8.2 - November 2025**
    -   Fixed:
        -   Fixed the issue with the usage data source when reclamation rules are set.
        -   Fixed the issue with creating a relationship between the server and the VM for Azure server.
-   **Version 1.8.0 - May 2025**
    -   New:
        -   Introduced support for creating a relationship between a server discovered by the SGC for Tanium and a VM discovered by any other discovery source.
        -   Introduced the buffer\_days\_from\_last\_scan\_for\_hardware parameter to add buffer days on the last scan date before removing the software records.
    -   Fixed:
        -   Fixed the software removal logic for multi-connections.
        -   Cleansed the serial number for the computer CI for the SGC for Tanium.
        -   Fixed the error on the SG-Tanium Hardware and Software data source that occurred after an upgrade to version 1.7.
-   **Version 1.7.0 - November 2024**

    New: The 'Last Scanned' date is now populated in the Software Installation \[cmdb\_sam\_sw\_install\] table.

-   **Version 1.6.0 - June 2024**

    Fixed: Improved software removal performance.

-   **Version 1.5.1 - March 2024**
    -   Fixed:
        -   Appended the connection alias ID in the Computer source native key to resolve scenarios involving multiple instances
        -   Menus intended for admin users in the application navigator will no longer appear for non-admin users
        -   Implemented a workaround in the SGTaniumDataSourceUtil script include to address the Lambda error that occurred during ETL transformations
        -   Addressed the HTTP 502 error during the import of hardware and software data
        -   Corrected the plugin name in the script for removing uninstalled software instances from "com.snc.samp" to "com.snc.sams"
        -   Fixed the problem with the data loader script when configuring multiple instances
-   **Version 1.5.0 - June 2023**
    -   Fixed:
        -   Issues related to software installation where the software apps were removed but not updated until the SG-Tanium Hardware and Software data source runs.
        -   Disabled theSG-Tanium Applications data source to improve performance.
    -   Removed: SG-Tanium SN Remove Software data source and the Tanium Removed Software \[sn\_tanium\_integ\_tanium\_removed\_software\] staging table as the behavior is already configured in the SG-Tanium Hardware and Software data source.
-   **Version 1.4.0 - March 2023**
    -   Fixed: Added support to handle empty responses from Tanium when there are additional data pages to be retrieved.
    -   New:
        -   Pull TCP and Running process data
        -   Support application dependency mapping
        -   Pagination for Application Datasource
-   **Version 1.3.1 - June 2022**
    -   Fixed:
        -   Tanium accepts token credentials for single and multi-instance.
        -   Fixed the mapping for Hardware and Software data source.
-   **Version 1.3.0 - May 2022**

    New: Added multi-instance support.

-   **Version 1.1.2 - December 2021**

    This integration imports data from Tanium Asset into ServiceNow Service Graph. Use the integration to sync your Tanium Asset data to the ServiceNow Configuration Management Database \(CMDB\). This integration uses Tanium Asset views and allows for periodic data synchronization from Tanium. This is the recommended method to bring data from Tanium Asset to CMDB with support for bringing software usage data as well.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

