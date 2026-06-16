---
title: Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes
description: Version history for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-ms-azure-iot.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes

Version history for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.1.0 - March 2026**

    New: Certified for Australia.

-   **Version 2.0.4 - August 2025**
    -   New:
        -   View the class mappings available for the Service Graph Connector using the new Class Mappings menu.
        -   Avoid OT entity update issues by using the new ire\_criterion\_attribute attribute on the OT Entity \[cmdb\_ot\_entity\] table.
        -   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
        -   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in ServiceNow automatically using the Site Map table.
-   **Version 2.0.2 - November 2024**

    Fixed: Updated with various bug fixes.

-   **Version 1.0.2 - February 2024**
    -   Import Microsoft Defender for IoT \(Azure\) sensors into the Network IDS \(NIDS\) class and take advantage of NIDS metadata assignment capabilities.
    -   OT devices detected by sensors with validated NIDS records will be imported and assigned the metadata on the NIDS record automatically.
    -   When the Industrial Process Manager is also installed, sites can be assigned to detected OT devices so that you can restrict access to users on a per-site basis.
    -   Support for importing OT-specific attributes, including zone and Purdue Model, to define the different levels of critical infrastructure.
    -   Data from additional sources like ServiceNow Discovery and Microsoft SCCM can be updated in the multisource CMDB.
    -   Sensors located on IT networks \(for example, in data centers\) can be designated as IT and appropriate configuration item records and relationships can be created.
    -   Certified for Washington DC
-   **Version 1.0.1 - August 2022**

    Integrate Microsoft Defender for IoT with the ServiceNow Operational Technology Manager application to import devices, connections and sensor appliances.


