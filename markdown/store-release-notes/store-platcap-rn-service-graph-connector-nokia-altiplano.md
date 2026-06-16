---
title: Service Graph Connector for NOKIA Altiplano release notes
description: Version history for the Service Graph Connector for NOKIA Altiplano application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-nokia-altiplano.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for NOKIA Altiplano release notes

Version history for the Service Graph Connector for NOKIA Altiplano application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.1 - June 2026**

    The Service Graph Connector \(SGC\) for Nokia Altiplano integrates with Nokia Altiplano through the SGC to fetch physical network data. It discovers and stores physical inventory information for the access network, including OLTs, ONUs, and their hardware hierarchy — slots, cards, subslots, and physical ports — in the CMDB.

-   **Version 1.2.1 - December 2025**

    New: A new granular admin role, tsom\_visibility\_admin, has been added to TSOM Core. Users with this role will have the ability to operate the Nokia Altiplano application functionality.

-   **Version 1.1.2 - August 2025**
    1.  New:
        1.  Support Discovery of Logical entities- Logical Interfaces, Logical Connections
        2.  Support Filtering conditions to enable discovery using IP Address/range and/or OLT Name.
    2.  Changed
        1.  System property to allow discovery of only OLT or both OLT and ONU.
        2.  Using the common ETL framework for discovery rather than the custom ETL for Altiplano.
        3.  Updated the logic to handle multi instance support.
-   **Version 1.0.1 - February 2025**

    Service Graph Connector for Nokia Altiplano provides Integration with Nokia Altiplano via SGC to fetch Physical Network data. It allows a mechanism via Physical Inventory Information of the the Access Network, including OLT, ONU and their underlying hierarchy of physical elements \(Slots, Cards, Sub-Slot and Physical Ports\) to be discovered and stored in CMDB.


