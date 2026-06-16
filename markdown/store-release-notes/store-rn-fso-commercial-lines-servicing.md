---
title: Commercial Lines Servicing release notes
description: Version history for the Commercial Lines Servicing application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-commercial-lines-servicing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Commercial Lines Servicing release notes

Version history for the Commercial Lines Servicing application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - June 2026**

    New: Added child tables for indexing for Financial Case indexed source

-   **Version 2.6.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 2.5.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 2.3.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 2.2.1 - November 2024**

    Changed: ACL bypass via UX Screen Condition.

-   **Version 2.2.0 - May 2024**
    -   New: Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
    -   Changed: Modified configuration for localization support
    -   Removed: Deprecated sn\_bom\_policy\_b2b.requestor role and related UI actions
-   **Version 2.1.0 - February 2024**
    -   Fixed: Fixed security issue in portal page
    -   Changed:
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 1.5.3 - December 2023 \(Vancouver\)**

    Fixed: Update Commercial policy coverage info service portal widget to private.

-   **Version 1.4.4 - December 2023 \(Utah\)**

    Fixed: Update Commercial policy coverage info service portal widget to private.

-   **Version 1.2.3 - December 2023 \(Tokyo\)**

    Fixed: Update Commercial policy coverage info service portal widget to private.

-   **Version 1.4.1 - November 2023**

    Changed: Moved product model demo data from the 'sn\_bom\_b2b\_ins\_policy\_model' table to 'sn\_ent\_b2b\_ins\_policy\_model' table.

-   **Version 1.4.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added localization changes.
-   **Version 1.3.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 1.2.0 - November 2022**

    Fixed: Fixed dark theme issues

-   **Version 1.1.0 - August 2022**
    -   New: Added configuration for document signing
    -   Changed:
        -   Updated reject reason values to be shown based on stages
        -   Updated labels of service name and policy number
        -   Renamed label from Net premium field to Balance due
        -   Renamed label from Decline button to Cancel request
    -   Removed: Removed customer 360 page and moved to FSO Core
-   **Version 1.0.3 - March 2022**
    -   New:
        -   New service definition on Business Owners Service Case for Change coverage request
        -   New playbooks for service definition
        -   New configurable workspace landing page for Commercial Lines Processor

