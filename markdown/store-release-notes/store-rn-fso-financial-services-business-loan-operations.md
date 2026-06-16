---
title: Financial Services Business Loan Operations release notes
description: Version history for the Financial Services Business Loan Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-business-loan-operations.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Business Loan Operations release notes

Version history for the Financial Services Business Loan Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.7.0 - April 2026**
    -   New: Added deposit service table as a source for AIS, enabling better data integration and insights.
    -   Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.
-   **Version 3.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 3.4.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 3.3.1 - February 2025**

    Fixed: Republish the playbook to fix the b2b relationship contributor not being able to access case after creation. 

-   **Version 3.3.0 - November 2024**

    New: Added scope flow executor role to subflows.

-   **Version 3.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed: Modified configuration for localization support
    -   Removed: Deprecated sn\_bom\_loan\_b2b.requestor role and related UI actions
-   **Version 3.1.0 - February 2024**
    -   Changed:
        -   Migrated the landing pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 2.3.2 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_loan\_account\_model' table to 'sn\_ent\_loan\_account\_model' table.

-   **Version 2.3.1 - August 2023**
    -   New
        -   Hide 'New' list action on loan service cases and loan tasks lists
        -   Updated landing page case report condition filter for assignment group field to dynamic
-   **Version 2.3.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added localization changes.
-   **Version 2.2.1 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI Actions for case
-   **Version 2.1.0 - November 2022**
    -   New: Added business location functionality
    -   Fixed: Fixed dark theme issues
-   **Version 2.0.0 - August 2022**
    -   New:
        -   Added configuration for document signing with integration to Document Template
        -   Added Document processor features
    -   Changed: Updated existing flows to support new document functionalities
    -   Removed: Financial document services application dependencies
-   **Version 1.1.2 - May 2021**

    Changed: Financial Services Core application dependency version has been updated

-   **Version 1.1.1 - March 2021**

    Changed: Moved plugin dependencies to Financial Services Operations Core

-   **Version \(1.1.0\) - December 2020**
    -   New:
        -   Manage loan service request for business customers
        -   Loan financial account types for business customers
        -   Dedicated agent workspace for loan agents
        -   Performance Analytics for insights into team's and business performance

**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

