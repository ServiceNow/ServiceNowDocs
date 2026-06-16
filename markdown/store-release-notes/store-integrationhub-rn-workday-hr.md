---
title: Workday HR spoke release notes
description: Version history for the Integration Hub Workday HR Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-workday-hr.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Workday HR spoke release notes

Version history for the Integration Hub Workday HR Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.12.2 - June 2026**
    -   Security patch on non-glide ACLs
    -   Fixed Hire Employee and Contract Contingent Worke for v45.2 Workday API compatibility
    -   Fixed "Look Up Skills" Action to support '&amp;' in the Skill Name in Report Query
-   **Version 2.11.1 - May 2026**

    Added a sample WQL construction Flow

-   **Version 2.10.0 - April 2026**

    Added 6 new WQL related actions and 1 sample flow.

-   **Version 2.9.0 - February 2026**
    -   Added:
        -   A sample Agentic workflow
        -   Added 5 new actions
    -   Fixed: Added role masking to the existing AI Agents
-   **Version 2.8.0 - January 2026**

    Added 1 action: Look up Using WQL

-   **Version 2.7.0 - December 2025**

    Added 1 new action and 15 new AI Agents

-   **Version 2.6.1 - July 2025**
    -   Fixed:
        -   Terminated field in action Look up Workers and Employment info with correct value.
        -   Converted any date\(mm/dd/yyyy, dd/mm/yyyy\) format to default workday date format\(yyyy/mm/dd\).
-   **Version 2.6.0 - March 2025**

    Added 4 new actions.

-   **Version 2.5.2 - January 2025**
    -   Fixed:
        -   Output for Look up Holiday Calendars and Get My Tax Withholding Info US actions.
        -   Log with warning message for Look up Location and Look up Job Posting Datastream actions; similar to Update My Address and Update Custom Object related actions.
        -   Added SOAP versioning for Manage Employee Skills action.
        -   Error handling for Look up Employee Skills action.
-   **Version 2.5.0 - December 2024**

    Added 1 new spoke action.

-   **Version 2.4.0 - November 2024**
    -   Added: 3 actions.
    -   Fixed:
        -   Look up Worker Profile action's primary phone number and email as false.
        -   Passing calendar WID as an array for Look up Holiday Calendars of an Employee action.
-   **Version 2.3.0 - July 2024**

    Enhanced Hire Employee action to support more business subprocesses OOB.

-   **Version 2.2.2 - May 2024**

    In this version, Look Up Workers action is modified to exclude or include pill data.

-   **Version 2.2.1 - March 2024**

    Fixed: Look up Workers and Employment Info action throws active = false for all the employees.

-   **Version 2.2.0 - February 2024**
    -   Added 3 new actions and 1 more webhook.
    -   Changed: Add more input fields to the Create Job Requisition action.
    -   Fixed: Change "Job Requisition WID" output variable field with "Job Requisition ID" from Update Job Requisition Action.
-   **Version 2.1.1 - December 2023**

    Fixed: Look up Workers action compatibility with the Washington instance.

-   **Version 2.1.0 - September 2023**
    -   Fixed:
        -   Missing 'report\_view' ACLs on a all tables
        -   Flows configured to run as System
    -   Added 6 new actions
-   **Version 2.0.0 - August 2023**
    -   Added OAuth support for all the SOAP based actions
    -   Added actions to look up in-progress approval requests, approve, and reject the requests
-   **Version 1.6.14 - January 2023**

    Patch release of Workday HR Spoke for Integration Hub. This version includes a fix to update connection details.

-   **Version 1.6.12 - October 2022**

    Fixed: Patch release of Workday HR Spoke for Integration Hub. This version adds a fix to improve the installation performance and the "Hire\_Rescinded" tag in the "Look up Workers and Employment Info" action.

-   **Version 1.6.10 - August 2022**

    Fixed: This is a patch release and has fixes related to the connection details table.

-   **Version 1.6.9 - May 2022**

    New: This is a patch release and has updated actions to support Workday v36.0 APIs.

-   **Version 1.6.2 - November 2021**

    Fixed: This is a patch release for Workday HCM with fixes.

-   **Version 1.6.0 - September 2021**
    -   New:
        -   10 new actions \(Hire Employee, Create Position, Edit Position, Close Position, Look up Positions, Change Job, Set Hiring Restrictions, Edit Hiring Restrictions, Look up Workers and Employment Info, Worker Time Off and Leave of Absence Request, Contract Contingent Worker\)
        -   New webhooks for Deactivate User and Leave of Absence
-   **Version 1.5.0 - June 2021**
    -   New:
        -   Look up Total Rewards Using Report
        -   Get Reference WID
        -   Look up Payslip
-   **Version 1.3.0 - April 2021**
    -   Fixed:
        -   Security fixes
        -   New Look up Paylsip action: Returns the payslip info of an employee
        -   New Look up Custom Report action: Generic action that is capable of retrieving data of custom reports which has doesn’t pro
-   **Version 1.1.2 - November 2020**

    Patch release of Workday HR spoke for IntegrationHub.

-   **Version 1.1.0 - September 2020**

    Fixed: Bug fixes of the Workday HR Spoke for IntegrationHub.

-   **Version 1.0.3 - August 2020**
    -   The Workday HR spoke provides a list of actions that wraps around the primary SOAP APIs and some REST APIs provided by Workday. In addition, this spoke provides one sample flows, one webhook inbound flow, and several remote tables that demonstrate how to perform:
        -   Bi-directional sync employee lifecycle between ServiceNow and Workday.
        -   View Workday's employee info, time-off request, time-off balance, etc. on demand in ServiceNow without storing any data in ServiceNow.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

