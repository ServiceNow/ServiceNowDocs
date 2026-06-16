---
title: Coupa Spoke release notes
description: Version history for the Integration Hub Coupa Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-coupa.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Coupa Spoke release notes

Version history for the Integration Hub Coupa Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.16.0 - June 2026**
    -   Security patch for non-glide ACLs
    -   Added 5 new actions
    -   Added primary address object fields to Update Supplier action
    -   Updated Get Supplier Fields \(Metadata\) action to have primary address object fields
    -   Updated Create Invoice action to support credit memo and price fields as number
    -   Added new Look up Product Catalogs Stream action and deprecated existing Look up Product Catalogs Stream action
-   **Version 4.15.0 - March 2026**
    -   Added 1 action.
    -   Added a Create Receipt action and deprecates existing Create Goods Receipt action.
-   **Version 4.14.0 - October 2025**

    Added 13 AI Agents.

-   **Version 4.13.0 - September 2025**

    Added required ACLs or Roles as per the AI Security Directive guidelines

-   **Version 4.12.0 - August 2025**

    Added 2 new Spoke Actions and updated 2 Spoke Actions

-   **Version 4.11.1 - June 2025**

    Added or improved 6 actions.

-   **Version 4.10.0 - May 2025**

    Added 7 conversational sample subflows.

-   **Version 4.9.1 - April 2025**
    -   New: Action: Look up Advanced Shipment Notices Stream by Purchase Order Line ID
    -   Fixed: Actions: Look Up Approvals Stream, Look up Contracts Stream
-   **Version 4.8.0 - March 2025**

    Created a sample conversational subflow.

-   **Version 4.7.0 - February 2025**
    -   Fixed:
        -   Look up Invoice action's line number mapping
        -   Added more output fields for Look up PO action
-   **Version 4.6.0 - January 2025**
    -   Added more input and output fields for:
        -   Look up Cost Centers Stream
        -   Look up Invoice Payment Details
        -   Look up Shipment Date
        -   Create Requisition
        -   Create Draft Requisition
        -   Update Requisition
        -   Update Invoice
-   **Version 4.5.0 - September 2024**
    -   Added 10 new Spoke Actions
    -   Changed 4 existing Actions with more input/output fields
    -   Fixed the data streaming Actions with upper limit restriction
-   **Version 4.4.0 - August 2024**

    Added or Updated 10 actions in total.

-   **Version 4.3.0 - June 2024**

    Added 13 actions.

-   **Version 4.2.0 - April 2024**

    Added 9 new actions.

-   **Version 4.1.3 - February 2024**

    Fixed: Unit Price in Coupa Requisition Line Details table to support decimal values.

-   **Version 4.1.2 - September 2023**
    -   Fixed:
        -   Fields data type mismatch found in the remote tables
        -   'licensable' field set to be true in plugin.xml
-   **Version 4.1.1 - April 2023**

    Improved installation performance.

-   **Version 4.1.0 - March 2023**

    Changed: Added Manufacture Part Number output field to Get PO Line action.

-   **Version 4.0.0 - August 2022**

    Changed: Made changes so that all actions use OAuth.

-   **Version 3.0.3 - March 2022**

    Patch release of Coupa Spoke for IntegrationHub. This version includes a fix within Close Purchase Order action for invalid PO ID.

-   **Version 3.0.2 - September 2021**

    Fixed: This version fixes an error observed when the correct receipt ID is provided.

-   **Version 3.0.1 - December 2020**

    Minor release of Coupa spoke for IntegrationHub. This release includes two new actions \(Look Up Item, Look Up Suppliers\) and support for the NOW mobile app.

-   **Version 2.0.0 - March 2020**
    -   New:
        -   Added generic error handling for unknown errors
        -   Added an Advanced Shipment Notice action to query From Date
        -   Added missing item attribute input on Create Requisition action
    -   Fixed: Included missing outputs on PO Line
-   **Version 1.0.1 - December 2019**

    Provides actions to automate approval, contract, inventory, invoice, catalog item, purchase order, requisition, supplier, and user management in Coupa.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

