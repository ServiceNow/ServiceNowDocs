---
title: Service Graph Connector for VMware Workspace ONE UEM release notes
description: Version history for the Service Graph Connector for VMware Workspace ONE UEM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-vmware-workspace-one-uem.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for VMware Workspace ONE UEM release notes

Version history for the Service Graph Connector for VMware Workspace ONE UEM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.0 - March 2026**
    -   Fixed:
        -   Fixed RAM value handling from Workspace ONE to ensure accurate memory representation across all device types.
        -   Placeholder MAC address values from Workspace ONE aren't populated to avoid mismatches in the CMDB.
-   **Version 1.8.0 - August 2025**

    New: Onboards the connector to the common connection framework \(CCF\).

-   **Version 1.7.0 - December 2024**
    -   Fixed:
        -   Fixed the issue to create the correct number of software records per device
        -   Fixed the check to validate serial number for Android 12 devices
        -   Fix the issue on handling Manufacturer for devices
        -   Mapped UDID to serial number\(cmdb\_serial\_number\) with type as UUID
-   **Version 1.6.1 - April 2024**

    Fixed: The unique device identifier \(UDID\) is now used as an identifier for devices running Android 12 or later versions.

-   **Version 1.6.0 - December 2022**
    -   Fixed:
        -   Fix turn\_off\_software\_import option that prevented software import.
        -   Add condition on serial number mapping for Computer, Handheld Device, Printer and Media Player.
        -   Fix for test record loading 20 records taking a long time.
-   **Version 1.5.0 - June 2022**
    -   Fixed:
        -   Removed IP address mapping to NIC.
        -   Removed quick mode from flow designer actions call.
        -   Added pagination in Remove Software.
-   **Version 1.4.3 - February 2022**

    Removed: Delete removed Software.

-   **Version 1.3.2 - September 2021**
    -   New:
        -   Added support for Basic Authentication in addition to OAuth.
        -   Support for filtering out user's personal apps on their mobile devices from being tracked in the CMDB.
        -   Performance Improvements.
    -   Fixed:
        -   The last\_discovered field on all CIs now reflects the last scan date from the Workspace ONE UEM.
        -   Username from Workspace ONE UEM is used to lookup the ServiceNow user from the User table. The assigned\_to field in all hardware CIs will contain this user.
        -   Handheld device name field now contains the concatenation of MAC address and serial number. This avoids mapping multiple devices with the same name to a single CI that relies on name is the primary identifier.
-   **Version 1.1.1 - April 2021**
    -   New:
        -   Implemented the ability to connect to multiple instances of Workspace ONE UEM.
        -   Captured additional data in a Related List to the Hardware Configuration Item:
            -   User Name
            -   User Email
            -   Ownership Compliance Status
-   **Version 1.0.4 - February 2021**

    New: VMware Workspace ONE UEM performs: Mobile Device Management​ Windows and macOS end-user computer​ Hardware and Software Asset Mgmt


