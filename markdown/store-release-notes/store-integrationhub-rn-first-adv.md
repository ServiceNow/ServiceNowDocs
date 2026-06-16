---
title: First Advantage spoke release notes
description: Version history for the Integration Hub First Advantage spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-first-adv.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# First Advantage spoke release notes

Version history for the Integration Hub First Advantage spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 1.8.0 - November 2025**

    Security patch: Improve sample webhook registry security.

-   **Version 1.7.0 - November 2024**

    Evaluated and modified Sandbox Access for Client-Callable Script Includes as false.

-   **Version 1.6.0 - May 2023**

    Added Authentication Template for easy 1-click setup.

-   **Version 1.5.5 - September 2022**

    Fixed: Patch version of First Advantage Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.5.4 - July 2022**

    Fixed: Patch release of First Advantage Spoke for IntegrationHub. This version includes a fix for ACL bypass with 'Accounts and Package Retrieval Util' Script Include.

-   **Version 1.5.3 - December 2021**

    Changed: Patch release of First Advantage Spoke for IntegrationHub. This version includes security-related changes.

-   **Version 1.5.2 - July 2021**

    Fixed: Patch Release of First Advantage Spoke for IntegrationHub. This version includes fixes for validation on null inputs, issues with Account ID within some actions.

-   **Version 1.2.0 - December 2020**
    -   Fixed:
        -   Spoke also supports multiple accounts and their associated packages
        -   Bug fixes
-   **Version 1.0.1 - April 2020**

    Fixed: User with fadv\_user role is unable to see the packages in Create First Advantage Case form.

-   **Version 1.0.0 - March 2020**
    -   The First Advantage spoke provides a list of actions that wraps around the primary REST APIs provided by First Advantage. In addition, the spoke provides two sample flows that demonstrate how to perform one-step and two-step screening processes.
    -   Most customers use a two-step screening process where ServiceNow kicks off the screening process in First Advantage. The First Advantage sends the invitation email to the candidate. The candidates fill their information and submit it to First Advantage. At the same time, ServiceNow keeps track of the invitation link in the Task table. When there's any status update on the screening in First Advantage, real-time updates are made in ServiceNow so that the HR Ops or candidates will have a 360-view of the latest progress.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

