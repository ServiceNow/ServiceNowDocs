---
title: Jack Henry jXchange Spoke release notes
description: Version history for the Jack Henry jXchange Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-jha.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Jack Henry jXchange Spoke release notes

Version history for the Jack Henry jXchange Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - August 2025**

    New: As part of this release, Deny ACLs have been added to existing tables to restrict unauthenticated users from performing CRUD operations.

-   **Version 2.0.2 - November 2024**

    Fixed: Added a fix script to remove snc\_internal role from the ACLs.

-   **Version 2.0.1 - May 2024**

    Changed: Added admin and user roles to the Remote Table ACLs.

-   **Version 2.0.0 - May 2023**
    -   Changed: Renamed application to Jack Henry jXchange Spoke
    -   Fixed:
        -   Fixed error in "Look up Financial Transactions Stream" action when passing Start Date
        -   Fixed error displayed when testing action "Look up Financial Account by Account Details"
-   **Version 1.0.4 - September 2022**

    Patch release of JHA Spoke for Integration Hub. This version adds fixes for XML Injection in outbound web service calls in flow actions, and execution with unnecessary privileges in flow actions.

-   **Version 1.0.2 - August 2022**

    Jack Henry Associates \(JHA\) SilverLake System provides seamless financial services to financial institutions of all sizes. The JHA spoke provides a list of actions that wraps around primary APIs provided by JHA. Although this spoke provides a few sample generic actions to look up and update records such as customer information, deposit accounts, and loan accounts, customers can expand the spoke to support almost any records available in JHA. Dynamic introspection allows customers to preview what fields are available in each record conveniently in Flow Designer.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

