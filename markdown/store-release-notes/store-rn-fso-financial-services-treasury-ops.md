---
title: Financial Services Treasury Operations release notes
description: Version history for the Financial Services Treasury Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-treasury-ops.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Treasury Operations release notes

Version history for the Financial Services Treasury Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.7.0 - April 2026**
    -   New: Added deposit service table as a source for AIS, enabling better data integration and insights.
    -   Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.
-   **Version 3.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 3.4.1 - August 2025**

    Changed: Updated the translation changes for Q4.

-   **Version 3.3.1 - February 2025**

    Fixed: Republish the playbook to fix the b2b relationship contributor not being able to access case after creation.

-   **Version 3.3.0 - November 2024**

    New: Added scope flow executor role to subflows.

-   **Version 3.2.1 - August 2024**

    Fixed: Fixed security defect with adding of report\_view ACL for tables sn\_bom\_treasury\_service\_financial\_account,sn\_bom\_treasury\_service\_use.

-   **Version 3.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed: Modified configuration for localization support
-   **Version 3.1.0 - February 2024**
    -   Changed:
        -   Migrated the landing pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 2.3.2 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_service\_model' table to 'sn\_ent\_financial\_services\_model' table.

-   **Version 2.3.1 - May 2023**

    New: Added localization changes.

-   **Version 2.3.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 2.2.0 - November 2022**
    -   New: Add business location functionality
    -   Fixed: Fixed dark theme issues
-   **Version 2.1.0 - August 2022**

    New: Added configuration for document signing with integration to Document Template

-   **Version 2.0.0 - May 2022**
    -   New:
        -   Security-related additions
        -   Added decision table for defining document rules
    -   Changed: Updated Flows and Process automation designer to use "Document Processor" actions and activity definitions for document verification
    -   Removed:
        -   Removed outbound document creation actions and activity definitions for flows and Process automation
        -   Removed "Financial Services Document Management" plugin dependency
-   **Version 1.0.1 - August 2021**

    Financial Services Treasury Operations enables financial institutions to onboard and perform due diligence of treasury services. Conditional forms and workflow streamline agents’ work during the application creation, review, and approval stages, eliminating vulnerabilities related to missing information, human error, and delay.


