---
title: Service Graph Connector for Infoblox release notes
description: Version history for the Service Graph Connector for Infoblox on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-service-graph-connector-infoblox.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Service Graph Connector for Infoblox release notes

Version history for the Service Graph Connector for Infoblox on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.0 - March 2026**
    -   New:
        -   Implemented life cycle management for all IPAM tables.
        -   Redesigned the Managed Network table to import Infoblox network view data instead of duplicating the Subnet table.
        -   Added new fields:
            -   Added the ip\_version field to the cmdb\_ci\_allocated\_ip\_address, cmdb\_ci\_ip\_pool, and cmdb\_ci\_ip\_network\_subnet tables for IPv4/IPv6 tracking.
            -   Added the subnet reference field to the cmdb\_ci\_allocated\_ip\_address table linking directly to the cmdb\_ci\_ip\_network\_subnet table.
        -   Updated table labels for consistency and to differentiate managed entities from discovered IP pools and network subnets:
            -   The IP Pool table is renamed to Managed IP Pool.
            -   The IP Network Subnet table is renamed to Managed IP Network Subnet.
        -   Infoblox extensible attributes are ingested into the cmdb\_key\_value table for all IPAM tables.
        -   Added the sn\_infoblox\_integ.default\_get\_ip\_address system property to set the global default for the Get IP Address option when importing networks.
        -   Updated all Source Native Keys \(SNKs\) to include Managed Network as part of the key for accurate CI identification.
    -   Fixed:
        -   Removed the relationship between Subnet and Allocated IP Address and replaced it with a direct reference field.
        -   Updated the upgrade process to mark CIs from version 1.4 and earlier as retired \(operational\_status=6\) instead of deleting them.
        -   Fixed the data duplication issue.
-   **Version 1.4.0 - August 2025**

    New: Added multi-instance support.

-   **Version 1.3.1 - June 2025**
    -   New:
        -   Implemented parallel loading for better performance.
        -   Added support to set up import schedules for IP address, subnet, and network data sources independently.
        -   Added support for IPv6.
-   **Version 1.2.0 - September 2024**
    -   Fixed:
        -   The network view property wasn't saving properly
        -   The connection name in the "Confirm connection creation" message \(SGC Central\)
-   **Version 1.1.1 - March 2024**
    -   Fixed:
        -   Updated the ACLs for the tables of Service Graph Connector for Infoblox
        -   Menus intended for admin users in the application navigator will no longer appear for non-admin users
        -   Fixed connection issues
        -   Fixed the issue with the "Test Load 20 Records" related link loading all data for the SG-Infoblox IP Address data source
-   **Version 1.1.0 - August 2023**
    -   New:
        -   Added support for IPv6
        -   Added ability to import CNAME as DNS Alias
-   **Version 1.0.0 - May 2023**

    Service Graph Connector for Infoblox imports subnets and IP addresses from Infoblox to the ServiceNow CMDB quickly, seamlessly, and securely. The connector is built on the Infoblox IPAM module. This integration is part of ServiceNow-developed Service Graph Connectors. The Plug-and-play Service Graph Connectors simplify setup and facilitate quick integration with Infoblox.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

