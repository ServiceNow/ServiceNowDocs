---
title: SAP S4 HANA RFC spoke release notes
description: Version history for the SAP S4 HANA RFC Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sap-s4-hana-rfc.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SAP S4 HANA RFC spoke release notes

Version history for the SAP S4 HANA RFC Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 2.6.1 - May 2026**

    Enhanced to support batching and pagination for Look up PO and PO Lines action. Updated Jco file associate to this enhancement.

-   **Version 2.5.1 - April 2026**

    Updated the MID Server JAR file and SapConnector Class to avoid Name, Version, and Filename conflicts.

-   **Version 2.5.0 - August 2025**

    Added: Enhanced and productized SNC load balancing.

-   **Version 2.4.3 - January 2025**
    -   Fixed:
        -   Added IT\_ACCOUNT\_GROUP object to Look up Vendor action.
        -   Look up material by Plants is not working as expected\(Getting error in full pull\)
-   **Version 2.4.1 - December 2024**

    Removed extra mandatory role at the action level, which can be managed at the ACL level.

-   **Version 2.4.0 - October 2024**
    1.  Security update on MID script includes
    2.  Fixed connMap for Look up Materials by Plant action
-   **Version 2.3.1 - July 2024**

    Fixed: Script Includes for Look up Inventory of Parts, Look up Payment status for Invoice, and Look up Payments actions.

-   **Version 2.3.0 - May 2024**

    Added 2 actions.

-   **Version 2.2.0 - April 2024**
    -   Added 5 actions
    -   Added SNC Connection feature
-   **Version 2.0.2 - February 2024**
    -   Fixed:
        -   Dynamic template error for Create Table Field Object action.
        -   Look up RFC Table Field Input Metadata action.
-   **Version 2.0.1 - December 2023**

    Fixed: Missing OOB 'report\_view' ACLs for multiple tables.

-   **Version 2.0.0 - November 2023**

    New: Added 6 new actions.

-   **Version 1.4.0 - June 2023**
    -   Redesigned 5 existing actions
    -   Added 5 new actions
-   **Version 1.3.1 - April 2023**

    Improved installation performance.

-   **Version 1.3.0 - August 2022**

    New: Added another Execute RFC action that can also support tabular schema.

-   **Version 1.2.0 - May 2022**

    New: Added Create Transfer Order and Line Items action.

-   **Version 1.1.0 - February 2022**
    -   New: Added 11 new actions and 1 sample outbound flow
        -   Look up Customer Info
        -   Look up Bill Details by ID
        -   Look up Inventory Parts
        -   Create Sales Order
        -   Update Sales Order
        -   Look up Sales Order
        -   Look up Sales Orders
        -   Look up Payments
        -   Look up Outstanding Balance
        -   Look up Transfer Order and Line Items
        -   Sample flow to create a sales order
-   **Version 1.0.3 - September 2021**

    Changed: Updated SapConnector jar.

-   **Version 1.0.2 - June 2021**

    This is a patch release of SAP S/4 HANA RFC Spoke for IntegrationHub. This release includes a fix for additional fields in the payload for Create Goods Receipt Action.

-   **Version 1.0.0 - February 2021**
    -   New:
        -   The SAP S/4 HANA RFC spoke provides a list of actions that interact with SAP standard BAPIs. It provides the foundation to synchronize ServiceNow and SAP S/4 HANA, such as create PO, update PO, create a journal entry, create invoices, create goods receipts, and so on.
        -   Given that SAP S/4 HANA is a highly customizable system, SAP S/4 HANA RFC Spoke also showcases the design pattern that can support custom BAPIs and more standard BAPIs beyond what is out of the box
        -   When both ServiceNow and SAP S/4 HANA do financial operations together, the possibilities are endless.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

