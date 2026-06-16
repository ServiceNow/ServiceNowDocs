---
title: Financial Services Business Deposit Operations release notes
description: Version history for the Financial Services Business Deposit Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-business-deposit-ops.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Business Deposit Operations release notes

Version history for the Financial Services Business Deposit Operations application on the ServiceNow Store.

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

    Fixed : Republish the playbook to fix the b2b relationship contributor not being able to access case after creation.

-   **Version 3.3.0 - November 2024**
    -   New: Added scope flow executor role to subflows
    -   Fixed: ACL bypass with UX screen condition security fix
-   **Version 3.2.2 - September 2024**

    Fixed: FSO Remote Lookup was not working on Voltron. Added event mapping for remote lookup to work on Votron.

-   **Version 3.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed: Modified configuration for localization support
    -   Removed: Deprecated sn\_bom\_deposit\_b2c.requestor role and related UI actions
-   **Version 3.1.0 - February 2024**
    -   Changed:
        -   Migrated landing pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
-   **Version 2.4.2 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_deposit\_account\_model' table to 'sn\_ent\_deposit\_account\_model' table.

-   **Version 2.4.1 - August 2023**
    -   New
        -   Added localization changes
    -   Fixed
        -   Updated landing page's case report filter condition to dynamic for the assignment group field.
-   **Version 2.4.0 - May 2023**
    -   New:
        -   Added UX page properties for the Agent Assist on Voltron record page.
        -   Added localization changes.
    -   Fixed: Fixed data issue for 'other's customer cases' option in Agent Assist.
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
    -   Changed: Updated Flows and Process automation designer to use Document Processor actions and activity definitions for document verification
    -   Fixed: Added icon for all catalog items
    -   Removed:
        -   Removed inbound/outbound document creation actions and activity definitions for flows and Process automation
        -   Removed Financial Services Document Management plugin dependency

