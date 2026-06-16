---
title: SAP Ariba spoke release notes
description: Version history for the SAP Ariba spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sap-ariba.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SAP Ariba spoke release notes

Version history for the SAP Ariba spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.15.0 - June 2026**

    Security patch on non-glide ACLs

-   **Version 1.14.0 - March 2026**
    -   Added Cancel Requisition.
    -   Fixed: Remove unnecessary mandatory inputs from create and update requisition.
-   **Version 1.13.0 - February 2026**
    -   Added a sample agentic workflow
    -   Fixed:
        -   Added role masking for the AI Agents
        -   Security vulnerability for a system property
-   **Version 1.12.0 - December 2025**

    Added 2 actions and 10 new AI Agents

-   **Version 1.11.0 - November 2025**

    Added 5 more actions.

-   **Version 1.10.2 - July 2025**
    -   Fixed:
        -   Deprecated outdated sample subflow and actions.
        -   Deprecated "Create Event Line Items" action and replaced it with a new action by updating the datatype of Quantity and Amount fields to number.
-   **Version 1.10.0 - June 2025**

    Added 1 spoke action.

-   **Version 1.9.1 - January 2025**

    Fixed: Response Timestamp field missing in Look up Pending Messages ID CXML action.

-   **Version 1.9.0 - December 2024**

    Added 5 new spoke actions.

-   **Version 1.8.0 - October 2024**
    1.  Security updates on MID script includes
    2.  Added FieldID output field to Create Sourcing Event, Look up Supplier Bids, and Look up Upstream Supplier actions
    3.  Support more formats for Download Attachment from Supplier Bid action response
-   **Version 1.7.0 - September 2024**
    -   Incorporated the new Xanadu Zip step feature into the Spoke Actions to unzip the file directly within the ServiceNow platform
    -   Fixed Update Requisition Action to create/update new/existing requisition lines accordingly
    -   Created a sample outbound Subflow to show how to update the requisition and requisition lines
    -   Fixed size limits for both Create Item Attachments and Create Requisition Actions
-   **Version 1.6.1 - August 2024**
    -   Added 10 actions.
    -   Renamed the action category and group the associated actions to match with the corresponding connection and credential alias names as much as possible.
-   **Version 1.5.0 - June 2024**

    Added 8 actions.

-   **Version 1.4.1 - May 2024**

    Added 8 actions.

-   **Version 1.3.1 - April 2024**

    Added 12 actions, mostly REST based.

-   **Version 1.3.0 - March 2024**

    Added 14 new REST based actions.

-   **Version 1.2.0 - February 2024**

    Changed: Updated Spoke action labels and documentation to avoid confusion and emphasize the fact that the SAP's deprecation news of ITK has no impact on this spoke.

-   **Version 1.1.2 - December 2023**

    Fixed:

    -   Missing OOB 'report\_view' ACLs for platform tables owned by \[Business Area\].
    -   Multiple flows configured to run as System.
-   **Version 1.1.1 - October 2023**

    Fixed: Execute Ariba Export Action - Export Supplier Organizations \(CSV\) Sourcing event to download and unzip attachments.

-   **Version 1.1.0 - September 2023**
    -   Added authentication template
    -   Fixed: Get Ariba Additional fields Action: Add Metadata in the suffix and mark active field as false
-   **Version 1.0.7 - April 2023**

    Improved installation performance.

-   **Version 1.0.5 - June 2022**

    Fixed: Patch release of SAP Ariba Spoke. This version includes a fix for the inability to activate flows when actions have empty values for mandatory fields.

-   **Version 1.0.4 - February 2022**

    Fixed: Patch version of SAP Ariba Spoke for IntegrationHub. This version fixes icon issues within flows.

-   **Version 1.0.3 - November 2020**

    Patch release of the SAP Ariba spoke for IntegrationHub.

-   **Version 1.0.1 - September 2020**
    -   New:
        -   The SAP Ariba Spoke provides a list of actions that interact with SAP Ariba. It provides the foundation to interact with Ariba's SOAP and REST API, as well as ITK \(Integration Toolkit\).
        -   Given that SAP Ariba is a highly customizable system, SAP Ariba Spoke also showcases the design pattern that can support additional ITKs beyond what is out of the box.
        -   When both ServiceNow and SAP Ariba do procurement together, the possibilities are endless.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

