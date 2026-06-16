---
title: Individual Life Servicing release notes
description: Version history for the Individual Life Servicing application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-individual-life-servicing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Individual Life Servicing release notes

Version history for the Individual Life Servicing application on the ServiceNow Store.

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

    Changed: Prevent ACL bypass by updating the ACL scripted condition from GlideRecord to GlideRecordSecure.

-   **Version 2.2.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added new menus for Next experience dashboard
    -   Changed:
        -   Updated the reject reason options for underwriters
        -   Added PA viewer role to individual manager
        -   Added sn\_ins\_indiv\_life.line\_writer role to Policy Coverage and Beneficiary ACLs
        -   Modified configuration for localization support
-   **Version 2.1.0 - February 2024**
    -   Changed:
        -   Migrated the agent assist pages to UIB layout 3.0
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 1.2.2 - November 2023**

    Changed: Moved product model demo data from 'sn\_bom\_indiv\_policy\_model' table to 'sn\_ent\_indiv\_life\_ins\_policy\_model' table.

-   **Version 1.2.1 - August 2023**
    -   Fixed
        -   Hide 'New' list action on Individual life service cases when user navigates to the List view from the landing page.
        -   Hide 'New' list action on Individual life tasks lists.
        -   Updated landing page's case report filter condition to dynamic for the assignment group field.
-   **Version 1.2.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added localization changes.
-   **Version 1.1.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions
-   **Version 1.0.2 - November 2022**

    Changed: Updated headers/sub-header translated text on the landing page

-   **Version 1.0.1 - August 2022**

    Individual Life Servicing empowers carriers to change the dynamics of life insurance policy servicing. Eliminate tedious manual processes with end-to-end digitization of the servicing journey. Boost customer satisfaction, decrease turnaround time, and reduce costly back-and-forth emails and phone calls. Gain efficiency by automating and optimizing the seamless transfer of work across internal and external stakeholders. Carriers can prioritize policy servicing requests with intelligent business rules to accelerate resolution.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

