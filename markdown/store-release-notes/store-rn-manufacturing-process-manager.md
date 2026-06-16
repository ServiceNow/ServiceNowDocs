---
title: Industrial Process Manager release notes
description: Version history for the Industrial Process Manager application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-manufacturing-process-manager.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Operational Technology release notes, ServiceNow Store release notes]
---

# Industrial Process Manager release notes

Version history for the Industrial Process Manager application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.0 - June 2026**

    New: Certified for Australia Patch 3

-   **Version 3.1.0 - March 2026**
    -   New:
        -   View all OT devices and unmapped OT devices in separate tabs during equipment model entity mapping
        -   AMAZING 2.0 supports discovered subnets to uniquely identify OT devices in copy-paste networks
        -   Automatically generate a location hierarchy for an equipment model entity in the Industrial Workspace
-   **Version 3.0.0 - December 2025**

    Changed: Minor Platform enhancement.

-   **Version 2.0.12 - August 2025**
    -   New:
        -   Filter out Not in use and Retired equipment model entities in the Industrial Workspace using the Operational Status field value for a site.
        -   In the Equipment Model Manager on the Industrial Workspace, favorite child equipment model entities using the Favorite icon.
        -   Use the Processing Order field to assign values to an equipment model entity that determines their functional importance in a Site.
        -   The Daily Activity tab displays the list of previous day's activities on the OT devices. The activities range from adding an OT device to changes in the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.
    -   Changed:
        -   The Not in use value was added as an option for the Operational Status field in an equipment model entity site record in the Industrial Workspace.
        -   The All OT Devices by Managed Network list was added to the Industrial Process Manager module on the ServiceNow AI Platform.
        -   In the Equipment Model Manager on the Industrial Workspace, the Favorite icon was added to favorite child equipment model entities in your system.
        -   When you use the search function to find an equipment model entity, the list expands to show and highlight the search entity.
-   **Version 2.0.11 - May 2025**

    New: Updated with various bug fixes.

-   **Version 2.0.10 - February 2025**
    -   New:
        -   Better organize your OT device data by capturing the mapped equipment model entity for an OT device.
        -   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.
-   **Version 2.0.7 - November 2024**

    Fixed: Updated with various bug fixes.

-   **Version 2.0.5 - September 2024**
    -   New:
        -   Add Operational Technology \(OT\) devices to an equipment model entity by using the IP address
        -   Change the Entity name and Parent fields of an equipment model entity to keep your equipment model entity information up to date after you create it
        -   Automatically installed with Operational Technology Incident Management and Operational Technology Change Management
        -   Certified for Xanadu
-   **Version 2.0.4 - August 2024**
    -   Add Operational Technology \(OT\) devices to an equipment model entity by using the IP address
    -   Change the Entity name and Parent fields of an equipment model entity to keep your equipment model entity information up to date after you create it
    -   Automatically installed with Operational Technology Incident Management and Operational Technology Change Management
    -   Certified for Xanadu
-   **Version 2.0.2 - February 2024**
    -   Certified for Washington DC
    -   Improved site level access control to use User Criteria to define read or write level user access to equipment model entity sites. With the additional assignment of OT viewer \(cmdb\_ot\_viewer\) or OT Editor \(cmdb\_ot\_editor\) roles, users will also have either view or edit access to OT devices in the sites assigned accordingly.
    -   On upgrade to version 1.0.12 of ISA Equipment Model, existing Site User records will be migrated to an improved access control model using User Criteria to preserve the same access permissions. For each site with ISA Entity Site User records:
        -   For users with viewer access:
            -   A new User Criteria record will be created and named Read User Criteria for &lt;site name&gt; Site \[System Generated\]
            -   A new User Group with all Site Users from this site will be created and named Read Group for &lt;site name&gt; Site \[System Generated\]
            -   A new record in the new Equipment Model Entity View Access table \(isa\_entity\_m2m\_user\_criteria\_can\_view\) will be created with the User Criteria and User Group just created as described above.
        -   For users with editor access:
            -   A new User Criteria record will be created and named Edit User Criteria for &lt;site name&gt; Site \[System Generated\]
            -   A new User Group with all Site Users from this site will be created and named Edit Group for &lt;site name&gt; Site \[System Generated\]
            -   A new record in the new Equipment Model Entity Edit Access table \(isa\_entity\_m2m\_user\_criteria\_can\_edit\) will be created with the User Criteria and User Group just created as described above.
    -   Removed the Site User application menu and Site Users related list on the Equipment Model Entity record for a site
    -   Set all Site User \(isa\_entity\_site\_user\) records to inactive
    -   Added application menu items for both
        -   Site User - Can Read
        -   Site User - Can Edit
    -   Added related lists on the Equipment Model Entity record for a site for both
        -   Can Read Equipment Models
        -   Can Edit Equipment Models
-   **Version 2.0.1 - August 2023**

    -   Certified for Vancouver
    -   Renamed to Industrial Process Manager
    -   Simplification to the template used by the service graph connector ETL
    -   The Manufacturing Workspace was renamed to Industrial Workspace
    -   The Manufacturing application menu item was renamed to Industrial Workspace Admin on the Platform.
    For uploading ISA Equipment Models through the Service Graph Connector:

    -   Removed Read-only protection policy for the ISAEquipmentModelConstants script include
    -   ISA admin can assign a template to any site at any time, regardless of whether a template has already been assigned.
    -   New role cmdb\_ot\_isa\_viewer\_all added to enable a user view only access to all Equipment Model Entity records. This role is included in cmdb\_ot\_admin role
    -   New template provided for import
-   **Version 1.0.9 - February 2023**

    New: Equipment Model Entity Schedules

-   **Version 1.0.8 - August 2022**
    -   Changed:
        -   Dependency change
        -   Certified for Tokyo
    -   New: Automatically Map Across Zone-based IP Network Groups \(AMAZING\), which maps OT assets by subnet to accelerate production process mapping
-   **Version 1.0.7 - March 2022**

    New: Enabled automatic updates of equipment model entity upstream and downstream relationships in the Equipment Model Manager workspace

-   **Version 1.0.6 - February 2022**

    New: Certified for San Diego

-   **Version 1.0.4 - November 2021**

    Changed: Dependency changes


**Parent Topic:**[ServiceNow Store - Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-manufacturing-highlights.md)

