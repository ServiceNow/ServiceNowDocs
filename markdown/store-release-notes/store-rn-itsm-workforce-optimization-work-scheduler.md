---
title: Work Scheduler for Workforce Optimization release notes
description: Version history for the ITSM Work Scheduler for Workforce Optimization application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-workforce-optimization-work-scheduler.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Work Scheduler for Workforce Optimization release notes

Version history for the ITSM Work Scheduler for Workforce Optimization application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.3.2 - March 2026**

    Fixed: Work Scheduler filter and show sidebar icon not closing after opening in Manager Workspace

-   **Version 3.3.0 - December 2025**

    Minor bug fixes.

-   **Version 3.2.7 - August 2025**

    Minor bug fixes.

-   **Version 3.2.2 - May 2025**

    Minor bug fixes.

-   **Version 3.2.1 - February 2025**

    Fixed: Matching criteria issue related to agents.

-   **Version 3.2.0 - November 2024**

    No Major feature changes. Contains minor changes and bug fixes.

-   **Version 3.1.4 - August 2024**

    Fixed accessibility defects in this release.

-   **Version 3.1.3 - May 2024**

    Fixed: WCAG bugs.

-   **Version 3.1.2 - February 2024**

    Fixed: Matching criteria bug.

-   **Version 3.1.1 - November 2023**
    -   New: Extension points feature
    -   Fixed:
        -   WCAG issue
            -   Foreground and background colors meets WCAG 2 AA minimum contrast ratio thresholds
            -   Elements that have scrollable content are accessible by keyboard
            -   The order of headings is semantically correct
            -   The content info landmark is at top level
        -   Axe tool testing
            -   Buttons should have discernible text
            -   Heading Level Should be increased by 1
            -   Form Elements should have labels
        -   A11y : Missing label for input elements
-   **Version 3.0.0 - August 2023**
    -   New:
        -   Migrate existing recommendation engine to Assignment workbench.
        -   Add timezone and availability matching criteria to recommend users.
        -   Add matching details in Work scheduler calendar contextual panel.
        -   Prevent the ability for user to use sort and filter when recommendations are on.
        -   Add "Work shift" details on the calendar contextual panel.
        -   Persist collapse of assignment groups in Work Scheduler calendar.
        -   Add matching criteria conditionally to recommendation matching rule.
        -   Clicking on Agent link will display user details in contextual side pane.
    -   Changed:
        -   Existing recommendation implementation was replaced with Assignment workbench framework to suggest users.
    -   Fixed:
        -   Security issues.
-   **Version 2.1.0 - August 2023**
    -   New:
        -   Create Teammembers section of contextual side panel for work calendar filters
        -   Move work scheduler header into side panel
        -   Move team member search and sorting of recommendations to above the now-calendar header
    -   Changed: UI changes for work scheduler page and filters contextual side panel
-   **Version 2.0.2 - April 2023**

    Fixed:

    -   UTC timezone users were unable to view the Shift calendar.
    -   Active span was not resizing.
    -   Display of work queue was empty.
-   **Version 2.0.0 - February 2023**
    -   New:
        -   Added new demo data
        -   Refresh recommendations when user clicks left/right arrow to move to the next item
-   **Version 1.1.0 - November 2022**
    -   New:
        -   Add ability to resize work item spans from the calendar directly without having to open the record first on the sidebar.
        -   Add ability to re-assign or move a work item span on the work scheduler calendar by performing drag and drop actions from the calendar grid.
        -   Add ability to resize work scheduler sidebar.
    -   Fixed:
        -   Fixed an issue that prevented the calendar to change the context date to the selected work item start date due to a bad handling of non default time formats set on the user's profile.
-   **Version 1.0.4 - August 2022**

    Plan your teams' work and assign work items such as incidents, problems, change requests, or interactions to them based on their skills and availability. View your teams' shifts and work assignments and assign or reassign the work items from a central location.​


**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

