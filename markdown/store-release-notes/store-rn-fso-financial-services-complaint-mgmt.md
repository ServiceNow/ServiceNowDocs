---
title: Financial Services Complaint Management release notes
description: Version history for the Financial Services Complaint Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-complaint-mgmt.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Complaint Management release notes

Version history for the Financial Services Complaint Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - April 2026**
    -   New: Added deposit service table as a source for AIS, enabling better data integration and insights.
    -   Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.
-   **Version 2.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 2.4.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 2.3.1 - February 2025**

     Fixed: Republish the playbook to fix the b2b relationship contributor not being able to access case after creation. 

-   **Version 2.3.0 - November 2024**

    New: Added scope flow executor role to subflows.

-   **Version 2.2.1 - August 2024**

    New: Added ACLs for Response template.

-   **Version 2.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed: Modified configuration for localization support
    -   Removed: Deprecated sn\_bom\_compl.requestor role and related UI actions
-   **Version 2.1.0 - February 2024**
    -   Changed:
        -   Migrated the landing pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 1.5.1 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_deposit\_account\_model' table to 'sn\_ent\_deposit\_account\_model' table and 'sn\_bom\_loan\_account\_model' to 'sn\_ent\_loan\_account\_model'.

-   **Version 1.5.0 - May 2023**
    -   New:
        -   Added UX page properties for the Agent Assist on Voltron record page.
        -   Added localization changes.
    -   Changed: Fixed data issue in the landing page - SLA Breached section.
-   **Version 1.4.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 1.3.0 - November 2022**
    -   New: Added business location functionality
    -   Fixed: Fixed dark theme issues
-   **Version 1.2.0 - August 2022**
    -   New: Added insurance viewer roles to complaint viewer role
    -   Changed: Changed reference qualifier to include Insurance Policies
-   **Version 1.1.1 - May 2022**
    -   Fixed: Account and contact fields are not mandatory when the customer field is populated
    -   Changed: Renamed service catalog to 'File a complaint'

**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

