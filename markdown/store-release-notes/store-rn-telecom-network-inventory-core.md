---
title: Network Inventory Core release notes
description: Version history for the Network Inventory Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-network-inventory-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Network Inventory Core release notes

Version history for the Network Inventory Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.2 - June 2026**
    -   This release strengthens data center and physical inventory management, hardens platform security, and improves overall reliability.
    -   New &amp; Improved Capabilities  - Rack &amp; slot management — Card placement now supports multi-slot cards, and the slot picker automatically hides occupied slots, making it faster and more accurate to  position equipment in racks.  - Slot span validation — Added validation so rack and template slot spans are always correctly defined, preventing incomplete or empty slot-span configurations.  - Smarter hierarchy naming — Cards in the hierarchy tree are now named from their model, with an automatic fallback to the template name when no model name is available,  giving clearer and more consistent naming.  - Network interface form layout — Network Interface and Network Interface Model records now surface additional relevant fields directly in the Network Inventory view for  quicker editing.
    -   Security &amp; Reliability  - Expanded access control coverage across core inventory tables to fully support secure query-range operations.  - Hardened data access by enforcing security-aware record queries throughout core logic.  - Replaced broad query handling with system- and user-scoped secure queries to close potential data-exposure gaps.  - Improved query reliability by resolving entities dynamically by table rather than relying on fixed identifiers.
-   **Version 6.0.1 - March 2026**

    This release contains same feature set as before without new or changes.

-   **Version 5.1.0 - December 2025**

    No Changes.

-   **Version 5.0.0 - August 2025**

    CI classes supporting facility classes.

-   **Version 4.0.1 - February 2025**

    No additional changes.

-   **Version 3.1.1 - November 2024**
    -   New: Enabled Deny ACL \(effective from Yokohama release onwards\)
    -   Fixed:
        -   IRE for TMF 639 API
        -   Slot span field applicability conditions
        -   Slot/interface naming execution defect with Enterprise product model
-   **Version 3.0.1 - August 2024**
    -   New:
        -   Data model to capture bearable weight and bearable weight units are added to inventory models
        -   Data model to capture assigned electric power is added Equipment Holder class
        -   Cable to strand model relationship
        -   Cable Template
    -   Changed: Inventory models are moved to the Enterprise product model. New installations will have the latest data model while upgrades will have both new and legacy inventory data model
    -   Fixed: Interconnect facility for classes which are child to Telco Equipment Class
    -   Removed: Deprecated legacy inventory product models
-   **Version 2.0.0 - February 2024**
    -   New:
        -   Channelization and Strand Management
        -   Decommission of CI
        -   Revision and opertaionlization of an operational CI
    -   Changed: Design and Assign flows
-   **Version 1.4.7 - January 2024**
    -   Fixed:
        -   Misconfiguration of table/field ACLs within the 'com.app-ni-core' plugin has been resolved
        -   "Add Card" use case failure due to the service offering being present has been resolved.
-   **Version 1.4.2 - September 2023**

    Fixes.

-   **Version 1.4.1 - August 2023**
    -   New:
        -   Enablement of Attribute Pack
        -   Number Management
        -   TNI HAM Integration
        -   TMF-639 Patch
    -   Changed: Enable record producer for change.
    -   Fixed: Equipment Holder data model change.
    -   Removed: Related Party.
-   **Version 1.3.5 - March 2023**

    Fixed: Added additional validations to ensure the cross-impact of TNI Workspace and SOW Workspace.

-   **Version 1.3.3 - February 2023**
    -   Changed:
        -   Updated business logic to work with a broader network inventory data model.
        -   Integrated OMT-TNI to initiate change requests for the order tasks of Order Management for Telecommunications and Media application.
        -   Define a catalog of inventory functions and subflows to execute the network inventory design and assign activities via user-defined flows/subflows.
-   **Version 1.1.1 - August 2022**
    -   New:
        -   Data Model to create and store Metadata, Template and Network Inventory data.
        -   Support custom name patterns for Slots and Interfaces
        -   Auto creation of Slots and Interface for Equipment and Card Templates based on Model Relationship
        -   Support for TMF639- POST, DELETE and GET
        -   Support for Template API to create resources and relationships via Template

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

