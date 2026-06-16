---
title: Financial Services Operations release notes
description: Version history for the Financial Services Operations Financial Services Payment Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-payment-operations.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Operations release notes

Version history for the Financial Services Operations Financial Services Payment Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 2.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 2.4.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 2.3.0 - November 2024**

    New: Added scope flow executor role to subflows.

-   **Version 2.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed: Modified configuration for localization support
    -   Removed: Deprecated sn\_bom\_payment.requestor role and related UI actions
-   **Version 2.1.0 - February 2024**
    -   Changed:
        -   Migrated the landing pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 1.5.3 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_deposit\_account\_model' table to 'sn\_ent\_deposit\_account\_model' table.

-   **Version 1.5.2 - August 2023**
    -   Fixed
        -   Hide 'New' list action on payment inquiry &amp; payment claim lists
        -   Updated landing page case report filter condition for assignment group field to dynamic
    -   Removed
        -   Removed claim viewer role from write ACLs on payment claim task
-   **Version 1.5.1 - May 2023**

    New: Added localization changes.

-   **Version 1.5.0 - February 2023**
    -   New: Added KMF encryption for account fields.
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 1.4.0 - November 2022**
    -   New: Add business location functionality
    -   Fixed: Fixed dark theme issues
-   **Version 1.3.0 - August 2022**

    New: Added configuration for document signing with integration to Document Template

-   **Version 1.1.1 - May 2021**

    Changed: Financial Services Core application dependency version has been updated

-   **Version 1.1.0 - March 2021**
    -   New:
        -   Added support for multiple transactions on Payment Inquiries, Claims, and Debit Approvals
        -   Added support for payments made to/from businesses
        -   Added business error categories and subcategories
        -   Added Debit Instructions related list to Claims
        -   Added support for Service Definitions
-   **Version 1.0.4 - September 2020**

    Provides capabilities to consolidate requests for a Payment Operations team and route them through workflows to the appropriate middle and back office teams.


