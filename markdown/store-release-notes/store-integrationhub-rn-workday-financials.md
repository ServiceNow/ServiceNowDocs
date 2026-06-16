---
title: Workday Financials spoke release notes
description: Version history for the Workday Financials Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-workday-financials.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Workday Financials spoke release notes

Version history for the Workday Financials Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - June 2026**

    Security patch on non-glide ACLs

-   **Version 2.1.1 - May 2026**

    Fixed: Deprecated and updated Create Supplier Invoice Action to support 45.2 Workday API

-   **Version 2.1.0 - August 2025**

    Added 27 actions.

-   **Version 2.0.2 - September 2023**
    -   Fixed:
        -   Missing 'report\_view' ACLs on a all tables.
        -   Flows configured to run as System.
-   **Version 2.0.1 - August 2023**
    -   Added OAuth support on all SOAP actions
    -   Verified the Spoke with v39 Workday public APIs
    -   Fixed duplicate items found in Create Supplier Invoice action
    -   Fixed the static file attachment name issue
-   **Version 1.3.1 - September 2022**

    Patch version of Workday Financials Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.3.0 - December 2021**

    Fixed: Patch release of Workday Financials Spoke for IntegrationHub. This version adds a fix to duplicated content in the GLIDE-INF folder.

-   **Version 1.2.8 - November 2021**

    Fixed: Patch release of Workday Financials Spoke for IntegrationHub. This version includes fixes for URLs containing hard-coded tenant names and security-related changes.

-   **Version 1.2.3 -August 2021**

    Fixed: KMF and security patches.

-   **Version 1.2.2 -April 2021**

    Fixed: The Workday Financials Spoke has been built by BristleCone Inc in the past and now has a couple of Patch fixes in this version.

-   **Version 1.1.0 - September 2020**
    -   New:
        -   The Workday Financials spoke provides a list of actions that wraps around the primary SOAP APIs and some REST API provided by Workday Financials. In addition, this spoke provides one sample flow and a webhook inbound flow that demonstrate how to perform:
            -   Constant sync data such as account sets, business units, cost centers, etc from Workday Financial to ServiceNow.
            -   Bi-directionally synchronize purchase order lifecycle between ServiceNow and Workday Financial.
            -   Workday Financials is the gospel of truth for the core Financial and Spend Management information. ServiceNow, as the System of Engagement and Action, needs the latest and greatest foundational Financial data to perform the subsequent actions, such as real-time create and update Purhcase Orders between ServiceNow and Workday Financials. Once ServiceNow has the foundational Financial data in place, customers can leverage the ServiceNow platform and its spokes to create more complex workflows beyond imagination.

