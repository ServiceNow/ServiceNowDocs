---
title: Intelligent Servicing for Fraud release notes
description: Version history for the Financial Services Operations Intelligent Servicing for Fraud on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-intelligent-servicing-fraud.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Intelligent Servicing for Fraud release notes

Version history for the Financial Services Operations Intelligent Servicing for Fraud on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 2.6.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 2.4.0 - August 2025**
    -   New: As part of this release, Deny ACLs were introduced on the existing tables. These Deny ACLs will restrict access for unauthenticated users on CRUD operations.
    -   Fixed: Restrict Access to relevant service definition to external user roles
-   **Version 2.3.2 - February 2025**

    Fixed: Republish the playbook to fix the b2b relationship contributor not being able to access case after creation.

-   **Version 2.3.1 - November 2024**
    -   New: Added scope flow executor role to subflows
    -   Changed: FraudCaseAjax has been made as Sandbox enabled as false
-   **Version 2.2.3 - August 2024**
    -   Changed: Replaced usage of 'image' with 'illustration component' in fraud score component
    -   Removed: Removed header component from existing landing pages
-   **Version 2.2.2 - June 2024**

    Fixed 'Recover fund task' generation issue.

-   **Version 2.2.0 - May 2024**
    -   New: Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
    -   Changed: Modified configuration for localization support
-   **Version 2.1.0 - February 2024**
    -   Changed:
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 1.1.2 - November 2023**
    -   Changed:
        -   Updated card\_provider field choice table from 'sn\_bom\_card\_model' to 'sn\_ent\_card\_service\_model' table
        -   Moved product model demo data to new model tables created in the Expanded Model and Asset Classes application.
    -   Fixed: Added list\_edit ACL for fraud\_suspected field in sn\_bom\_fraud\_transaction, for users with roles sn\_bom\_fraud.agent\_connector, sn\_bom\_fraud.contributor, sn\_bom\_fraud.agent.
-   **Version 1.1.1 - August 2023**

    Fixed: Updated 'Customer liability' field with currency code in card fraud policy outcome subflow.

-   **Version 1.1.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added localization changes.
-   **Version 1.1.0 - February 2023**

    Intelligent Servicing for Fraud automates work so that cases are resolved at lower cost and the fraud window is simultaneously closed. Provides capabilities to create, analyze, investigate and dispose fraud alerts and complaints for financial institutions, providing transparency and ease for middle and back-office teams. With these capabilities, financial institutions can reduce or avoid the direct and indirect cost of fraud such as reputational damage and regulatory exposure.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

