---
title: Service Graph Connector for Microsoft Intune release notes
description: Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Microsoft Intune on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-ms-intune.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Microsoft Intune release notes

Version history for the ServiceNow AI Platform capabilities Service Graph Connector for Microsoft Intune on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.8.1 - March 2026**

    New: Added retry logic for reports data source when sending requests to trigger reports.

-   **Version 2.7.1 - October 2025**
    -   New: Improved user experience during SG-Intune setup by providing the option to select advanced or regular data sources.
    -   Fixed:
        -   Fixed the software removal logic to remove the operating system software.
        -   Mapped Network Adaptor for Computer and Device.
-   **Version 2.3.1 - March 2024**
    -   Fixed:
        -   SG - Intune Computer data source was not updating the discovery source in the Network Adapter \[cmdb\_ci\_network\_adapter\] table
        -   SG-Intune Software data source was updating the most recent discovery of computers to the scheduled import time
-   **Version 2.3.0 - September 2023**
    -   New:
        -   Upgraded Microsoft Intune APIs to v1.0
        -   Added the support for government Intune APIs
        -   Supported the new connection framework
    -   Fixed:
        -   Fixed the software removal logic when the connection failed
        -   Fixed the empty Data loader issue for multi-instance connection
-   **Version 2.2.1 - March 2023**
    -   New:
        -   Updated Intune by bringing attributes for devices - lastSyncDateTime, azureADRegistered, managedDeviceOwnerType, isSupervised, userPrincipalName,isEncrypted,managementAgent
        -   Mapped IP address with wiredIPv4Addresses device attribute
        -   For any discovered software applications that were deleted later in the Microsoft Intune application, the Service Graph connector automatically deletes the corresponding records in CMDB
-   **Version 2.1.2 - April 2022**

    Fixed: Data source load issue affecting Quebec family release.

-   **Version 2.1.1 - February 2022**

    New: Multi-instance support.

-   **Version 2.0.0 - April 2021**

    New: Introduced the use of Intune batch API to improve performance of data imports.

-   **Version 1.1.1 - November 2020**
    -   New:
        -   Support for MID Server in Guided Setup
        -   Contextual help for Guided Setup
    -   A number of fixes.

