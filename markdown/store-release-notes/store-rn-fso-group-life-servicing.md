---
title: Group Life Servicing release notes
description: Version history for the Group Life Servicing on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-group-life-servicing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Group Life Servicing release notes

Version history for the Group Life Servicing on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.7.0 - June 2026**

    New: Added child tables for indexing for Financial Case indexed source

-   **Version 2.6.0 - April 2026**
    -   New:
        -   Introduced new processor rejection flow, allowing users to handle processor rejection scenarios more efficiently.
        -   Added new utility classes and support files to enhance the playbook and group life workflows.
        -   Added shadow DOM-piercing strategies for more robust field interactions in automated flows.
    -   Updated:
        -   Enhanced the logic for clicking tabs and buttons in the playbook, ensuring compatibility with different browsers and CI environments.
        -   Updated the process for marking steps complete and submitting applications, adding explicit waits and strategies to handle page refreshes and loading states.
-   **Version 2.5.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 2.3.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 2.2.1 - November 2024**

    Changed: Prevent ACL bypass by updating the ACL scripted condition from Gliderecord to GlideRecordSecure.

-   **Version 2.2.0 - May 2024**
    -   New: Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
    -   Changed: Modified configuration for localization support
-   **Version 2.1.0 - February 2024**
    -   Fixed: Fixed security issue in portal page
    -   Changed:
        -   Migrated the agent assist page to UIB layout 3.0
        -   Modified configuration for localization support
        -   Upgraded snc-app-parent version to 5.1.0.16
-   **Version 1.3.3 - December 2023 \(Vancouver\)**

    Fixed: Updated Group life policy coverage info service portal widget to private.

-   **Version 1.2.4 - December 2023 \(Utah\)**

    Fixed: Updated Group life policy coverage info service portal widget to private.

-   **Version 1.0.4 - December 2023 \(Tokyo\)**

    Fixed: Updated Group life policy coverage info service portal widget to private.

-   **Version 1.2.1 - November 2023**

    Changed: Moved product model demo data to new model tables created in the Expanded Model and Asset Classes application.

-   **Version 1.2.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added localization changes.
-   **Version 1.1.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 1.0.1 - November 2022**

    Fixed: Fixed dark theme issues

-   **Version 1.0.0 - August 2022**

    Group Life Servicing empowers carriers to change the dynamics of group life and disability insurance policy servicing. Carriers can be agile and responsive to customers across the servicing journey with a unified workflow and frictionless exchange of data between carriers, benefits administrators, and employers. Eliminate tedious manual processes and reduce costly back-and-forth emails and phone calls with end-to-end digitization. Boost customer satisfaction, and decrease turnaround time by automating and optimizing the seamless transfer of work across internal and external stakeholders.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

