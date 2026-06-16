---
title: Qualtrics spoke release notes
description: Version history for the Integration Hub Qualtrics spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-qualtrics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Qualtrics spoke release notes

Version history for the Integration Hub Qualtrics spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 1.3.0 - November 2025**

    Security update: Improved system scoping privilege for better sample subflow security.

-   **Version 1.2.4 - December 2023**

    Fixed: Look up Mailing list Action: Error: Parameter skipToken should not be empty.","errorCode":"QVAL\_5.

-   **Version 1.2.3 - June 2023**
    -   Fixed: Marked the deprecated ""Look up Contacts by Email"" action to inactive.
-   **Version 1.2.2 - September 2022**

    Patch version of Qualtrics Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.2.1 - July 2022**

    New: Patch release of Qualtrics Spoke for IntegrationHub. This version includes a fix for ACL bypass with 'Webhook Callback URL Generator' Script Include.

-   **Version 1.2.0 - May 2022**
    -   New:
        -   Added partner-id and X-API-Token header parameters for traceability
        -   Webhook subscription management actions
        -   Sample inbound webhook subflow
        -   Sample Remote Table
-   **Version 1.1.1 - November 2021**
    -   New:
        -   Added a sample outbound flow to upsert customer contact from ServiceNow to Qualtrics
        -   Added a sample flow to route to different subflows based on Qualtric's CSAT and Customer Value Score
    -   Changed: Updated Look up Contacts by Email action to include segment membership, which provides CSAT and Customer Value Score from Qualtrics
-   **Version 1.0.0 - October 2020**

    Provides actions to automate the management of Qualtrics.


