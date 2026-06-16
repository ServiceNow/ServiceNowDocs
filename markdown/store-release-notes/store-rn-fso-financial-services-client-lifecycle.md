---
title: Financial Services Client Lifecycle release notes
description: Version history for the Financial Services Client Lifecycle application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-client-lifecycle.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Client Lifecycle release notes

Version history for the Financial Services Client Lifecycle application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.7.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 3.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 3.4.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 3.3.0 - November 2024**

    New: Added scope flow executor role to subflows.

-   **Version 3.2.1 - August 2024**

    Fixed label in the playbook activity.

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
-   **Version 2.3.1 - May 2023**
    -   New: Added localization changes.
    -   Removed: Removed snc\_internal role from ACLs.
-   **Version 2.3.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 2.2.0 - November 2022**
    -   New: Added business location functionality
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
-   **Version 1.0.3 - August 2021**

    Financial Services Client Lifecycle enables financial institutions to shorten their time-to-revenue for new accounts and respond to other events that affect KYC over time. With an intelligent workflow that includes rulesets, playbooks, and agent workspaces, each team member can contribute to an efficient, consistent, and compliant process.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

