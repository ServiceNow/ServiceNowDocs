---
title: Oracle HCM Cloud spoke release notes
description: Version history for the Oracle HCM Cloud spoke integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-oracle-hcm-cloud-spoke.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Oracle HCM Cloud spoke release notes

Version history for the Oracle HCM Cloud spoke integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.5.0 - June 2026**

    Security patch for non-glide ACLs

-   **Version 4.4.0 - April 2026**
    -   Fixed: Added role masking to the OOTB AI Agents
    -   Added a sample AI Agent Workflow
-   **Version 4.3.1 - March 2026**

    Security fix on a system property vulnerability.

-   **Version 4.3.0 - December 2025**

    Added 10 new AI Agents

-   **Version 4.2.0 - August 2025**
    -   Fixed: "Look up benefits enrollment specialist" Agent returns a 500 from the subflow when there are no user benefits
    -   Added:
        -   Absence Reason in Request time off action
        -   LegalEmployerName in Look Up Workers Stream data stream output
        -   Actions to retrieve absence reason and absence type
-   **Version 4.1.1 - January 2025**

    Fixed: Status output from Get Oracle Cloud HCM Object metadata action.

-   **Version 4.1.0 - November 2024**

    Added/updated 5 actions.

-   **Version 4.0.1 - December 2023**

    Fixed:

    -   Unable to add multiple query parameters in the input of Look up Workers Stream action.
    -   Missing OOB 'report\_view' ACLs for Multiple Table.
    -   Omit if the Empty check box is not checked for the Authorization header in Look up Atom Feeds Employees Newhire Stream action due to which JWT is working but basic auth is not working.
-   **Version 4.0.0 - November 2023**

    Added: 7 new actions, authentication template, and OAuth JWT grant type.

-   **Version 3.3.0 - May 2023**

    Improved installation performance.

-   **Version 3.2.2 - November 2022**

    Patch release of Oracle HCM Cloud Spoke for IntegrationHub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 3.2.1 - March 2022**

    New: Fields at actions 'Look up Workers Stream' and 'Look up Active And Inactive Workers Stream'.

-   **Version 3.2.0 - February 2022**
    -   New: Added two new actions
        -   Look up Payslip
        -   Look up Legislative Data Group
-   **Version 2.5.0 - November 2021**
    -   New: This version adds a new action 'Look up Organization Payment Method'
    -   Changed:
        -   Changes to citizenship status
        -   Performance improvements to Total Rewards
    -   Fixed: Fixes to Time-Off Balance and filtering inactive workers.
-   **Version 2.4.0 - October 2021**
    -   New:
        -   Added four new actions.
        -   Added a remote table.
    -   Changed: Updated the "Look up Workers Stream" action.
-   **Version 2.1.0 - July 2021**

    Added the "Look up Total Rewards" action and updated the "Look up Payroll" action.

-   **Version 1.0.2 - May 2021**
    -   More actions are added:
        -   Look up Record Details
        -   Look up Benefit Enrollments
        -   Look up Individual Compensation
        -   Look up Atom Feeds for
            -   Employees Assignments
            -   Employees Newhire
            -   Employees Termination
            -   Locations
            -   Organizations
        -   Look up Departments
        -   Look up Employee Assignments
        -   Look up Holiday Calendar
        -   Look up Locations
        -   Look up Workers
        -   Look up External Bank Accounts
        -   Look up Payroll
        -   Look up Payroll Elements
    -   Two sample remote tables:
        -   Holiday calendar
        -   New positions
-   **Version 1.0.0 - October 2020**
    -   Highlights of the Oracle HCM spoke: Actions
        -   Look up Positions
        -   Look up Jobs
        -   Look up Employees
        -   Look up Atom Feeds Employee Update
        -   Look up Atom Feeds Jobs
        -   Look up Atom Feeds Positions

