---
title: Shift Planning release notes
description: Version history for the Shift Planning application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-shift-planning.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Shift Planning release notes

Version history for the Shift Planning application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.0 - June 2026**
    -   Added Shifts, Shift Swap, Schedule Adherence, and Time Off Requests tab routes in CSM workspace
    -   Added Schedule and Scheduling Adherence lists in CSM workspace Lists navigation
    -   Added Team Schedule nav item for CSM/FSM Workspace with Shift Planning Manager applicability
    -   Implemented manager role for supervisors to access schedule capabilities
    -   Fixed minor defects
-   **Version 7.0.0 - March 2026**
    -   Manage location‑based holiday calendars to improve workforce scheduling by mapping holidays to specific regions, enabling managers to plan shifts with accuracy, and reducing manual adjustments.
    -   Fixed minor defects
-   **Version 6.10.2 - December 2025**

    Minor bug fixes.

-   **Version 6.9.0 - August 2025**

    Minor bug fixes.

-   **Version 6.8.0 - May 2025**
    -   Enables agents to sign up for shifts
    -   Enables managers and agents to get shift signup notifications
    -   New table "Agent Schedule Attribute" enables managers to track agent location and view agent personal event details
-   **Version 6.7.1 - November 2024**

    No Major feature changes. Contains minor changes and bug fixes.

-   **Version 6.6.1 - August 2024**
    -   New:
        -   Added ability to synch WFO calendars with Outlook calendar
        -   Added ability to for managers and agents to create recurring meeting and training events
    -   Fixed a few accessibility issues
-   **Version 6.4.3 - May 2024**

    Fixed: WCAG bugs.

-   **Version 6.3.1 - February 2024**
    -   Changed: Modify existing L1 schedules module
    -   Fixed: Shift swap modal button bug
-   **Version 6.2.1 - November 2023**
    -   New:
        -   Upgraded shifts and schedules to page layout 3.0
        -   Generating demo data changes for Monthly Schedules
    -   Fixed: Accessibility issues
-   **Version 6.1.4 - September 2023**
    -   Fixed:
        -   On-call time off not getting displayed up on the proposed cover agent calendar
        -   Leave request description of others was visible to all shift planning users
        -   Save Buttons was not getting enabled while editing meeting and training
-   **Version 6.1.2 - August 2023**
    -   New: Inclusion/Exclusion Criteria Applicable Groups
    -   Changed: Bug fixes
-   **Version 5.4.5 - May 2023**

    Changed: Forecast historical volumes along with forecasts so that users can compare the patterns.

-   **Version 5.4.4 - April 2023**

    Fixed: UTC timezone users are unable to view the Shift Calendar, which has been fixed in this version.

-   **Version 5.4.3 - March 2023**
    -   Fixed: Fixed the following minor issues where:
        -   The location filter was not working
        -   The Requested-Save Shift to a Schedule was not working
        -   There was an issue with On-Call OOTB flag during San Diego to Utah release upgrade
-   **Version 5.4.1 - February 2023**

    New: added custom event types in team calendar of manager workspace.

-   **Version 5.3.0 - November 2022**
    -   New:
        -   Agent shift signup feature
        -   To enable the agents to sign up for shifts, you must setthe sn\_shift\_planning.enable\_agent\_signup property to true.
    -   Changed: The following label changes to the filters for schedules are automatically made:
        -   State is renamed to Schedule plan state.
        -   Dates is renamed to Schedule plan dates.
-   **Version 5.1.7 - November 2022**
    -   Fixed:
        -   Fixed issue where new shift not searchable
        -   Show overlapping requests of only agents managed by logged in user
-   **Version 5.1.4 - September 2022**
    -   Fixed:
        -   Fixed issue where Shift Calendar fails when there are inactive groups.
        -   Fixed issue where Agent belonging to multiple groups is shown multiple times under schedule creation flow.
-   **Version 5.2.3 - August 2022**
    -   New:
        -   Ability to select timezones for work shifts and on-call shifts.
        -   Managers can assign schedule plans to groups.
        -   Use pagination on the shifts and team calendar.
        -   Use pagination to scroll through your agent's shifts and schedules.
    -   Fixed: Enable localization support.
-   **Version 5.1.2 - May 2022**
    -   New:
        -   Filtering, search, and pagination capability for schedule plans, work shifts, and on-call shifts.
        -   Agents and managers communicate with each other for approvals using the Compose field in the approval form.
        -   Enable localization support.
-   **Version 5.0.0 - March 2022**

    New: Initial Store release for San Diego

-   **Version 4.0.9 - February 2022**

    Shift planning allows managers and supervisors to configure workforce scheduling.


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

