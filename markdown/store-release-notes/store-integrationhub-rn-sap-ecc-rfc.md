---
title: SAP ECC RFC spoke release notes
description: Version history for the SAP ECC RFC Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sap-ecc-rfc.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SAP ECC RFC spoke release notes

Version history for the SAP ECC RFC Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.10.0 - June 2026**
    -   Security patch for non-glide ACLs
    -   Added Swift Code in Vendor Bank Details field for create/update vendor action
-   **Version 2.9.4 - April 2026**

    Fixed: Updated MID Server JAR file and SapConnector Class to avoid Name, Version, and Filename conflicts

-   **Version 2.9.3 - March 2026**

    Enhanced: Look up Purchase Orders and Purchase Order Lines - Additional Input Fields Added for the action to support Full Pull

-   **Version 2.9.2 - February 2026**

    Fixed: Cancel Invoice action intermittently returns a blank output in the dynamic object field.

-   **Version 2.9.1 - December 2025**

    Security enhancement: Made the UI label of sn\_sap\_ecc\_rfc\_spo\_sap\_rfc\_list table read-only

-   **Version 2.8.0 - August 2025**

    Added: Enhanced and productized SNC load balancing

-   **Version 2.7.2 - March 2025**

    Security patch update.

-   **Version 2.7.1 - January 2025**

    Fixed: Added IT\_ACCOUNT\_GROUP object to Look up vendor action.

-   **Version 2.7.0 - December 2024**

    Added more fields for the Create Vendor and Update Vendor spoke actions.

-   **Version 2.6.0 - October 2024**

    Added more output fields for Create Non-PO Invoice and Create Invoice actions.

-   **Version 2.5.0 - September 2024**

    Incorporated tax object for Create Invoice and Create Non Purchase Order Invoice actions.

-   **Version 2.4.1 - June 2024**

    Fixed: Missing OOB 'report\_view' ACLs for platform tables.

-   **Version 2.4.0 - May 2024**

    Added 2 more actions.

-   **Version 2.3.1 - April 2024**
    -   Added 5 new actions
    -   Added SNC connection support
-   **Version 2.2.0 - February 2024**

    Changed: Updated sapConnector.jar and added a common ECC-agent.jar to support multi-threading with other ServiceNow's SAP integration products that reside on the same MID Server.

-   **Version 2.1.0 - November 2023**

    New: Added 6 new actions.

-   **Version 2.0.4 - September 2023**
    -   Fixed:
        -   JCO's RFC / BAPI function returning an array inside an array issue.
        -   Script includes dependency for PSM app.
-   **Version 2.0.2 - July 2023**

    Fixed to handle bank account numbers that exceed 16 characters.

-   **Version 2.0.1 - June 2023**
    -   Fixed "Look up Operations" action
    -   Updated to support load balancing environment
    -   Added ACL role check for actions with sensitive data
-   **Version 2.0.0 - May 2023**
    -   Redesigned 5 existing actions
    -   Added 5 new actions
-   **Version 1.5.1 - April 2023**

    Improved installation performance.

-   **Version 1.5.0 - December 2022**
    -   Added the new enqueue-luw action-dequeue Action for HR module user provisioning use case
    -   Added load balancing logon group connection alias for customer who uses clustering server setup
-   **Version 1.4.0 - February 2022**
    -   New: Added 2 new actions
        -   Create Transfer Order and Line Items
        -   Look up Transfer Order and Line Items
-   **Version 1.3.0 - August 2021**
    -   Execute RFC action now supports tabular structure for create and update operations
    -   User can now create, look up, and update most of the operations that can be called by BAPIs
-   **Version 1.2.1 - June 2021**

    This is a patch release of SAP ECC RFC Spoke for IntegrationHub. This release includes a fix for additional fields in the payload for Create Goods Receipt Action.

-   **Version 1.2.0 - May 2021**
    -   Added new actions:
        -   Look up Customer Info
        -   Look up Bill Detail by ID
        -   Look up Bill Details
        -   Look up Inventory of Parts
        -   Create Sales Order
        -   Update Sales Order
        -   Look up Sales Orders
        -   Look up Sales Order
        -   Look up Payments
        -   Look up Outstanding Balance
        -   Create Sales Order and Look up Status
-   **Version 1.0.1 - September 2020**

    New: The SAP ECC RFC Spoke provides a list of actions that interact with SAP standard BAPIs. It provides the foundation to synchronize ServiceNow and SAP ECC, such as create PO, update PO, create a journal entry, create invoices, create goods receipts, and so on.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

