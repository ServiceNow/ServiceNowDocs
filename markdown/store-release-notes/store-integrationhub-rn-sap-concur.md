---
title: SAP Concur spoke release notes
description: Version history for the SAP Concur spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-sap-concur.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# SAP Concur spoke release notes

Version history for the SAP Concur spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.2 - April 2026**

    Updated the condition from 'co' to 'eq' in the SapConcurUtil Script Include to increase precision for the Look up Users Stream result set

-   **Version 2.3.1 - February 2026**
    -   Added a sample agentic workflow
    -   Deprecated the old Get User Details and Look up Users Data actions
    -   Fixed: Added role masking for the existing AI Agents
-   **Version 2.2.0 - December 2025**

    Added 10 new AI Agents

-   **Version 2.1.2 - August 2024**

    Fixed: Request payload of Look up Users Stream action getting appended with an additional array in Xanadu instances.

-   **Version 2.1.1 - November 2023**

    Fixed: Missing OOB 'report\_view' ACLs on multiple tables.

-   **Version 2.1.0 - September 2023**

    Added authentication template.

-   **Version 1.0.5 - June 2023**
    -   New: Pre-built integration with SAP Concur allows employees to sync, view, track, send back, and fulfill requests from external business applications into Employee Center Pro. This plugin provides a configurable omnichannel experience from Employee Center Pro and actionable notifications in Virtual Agent in Microsoft Teams. Approvers are able to:
        -   View expense reports.
        -   View line items for expense reports.
        -   View itemizations.
        -   View Comments on an expense report.
        -   View Attachments for a report and/or for a line item.
        -   Approve or send back expense report with comments.
-   **Version 2.0.0 - May 2023**
    -   Added 5 actions that are related to employee experience and environmental-sustainability-governance use cases
    -   Added new authentication templates that are related to these 5 actions
-   **Version 1.0.1 - April 2023**

    Improved installation performance.

-   **Version 1.0.0 - February 2021**

    The Concur spoke provides a list of actions that wraps around the primary REST APIs provided by Concur. In addition, this spoke provides one sample flow on syncrhonizing a list of last modified expense report from Concur to ServiceNow. It also provides a remote table sample to view the list of expense report on demand from Concur in ServiceNow without persisting any data in ServiceNow.


