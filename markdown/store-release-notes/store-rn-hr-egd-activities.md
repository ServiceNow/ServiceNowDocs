---
title: Career Conversations release notes
description: Version history for the Career Conversations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-egd-activities.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Career Conversations release notes

Version history for the Career Conversations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.10.0 - June 2026**
    -   Tested WCAG 2.2AA and 400% zoom/reflow support in core UI
    -   Reviewed Non-Glide Cobalt Raven ACLs
    -   Tested TinyMCE v8 Library Upgrade
-   **Version 3.9.0 - March 2026**
    1.  Enhanced the Outlook scheduling feature for a user to view available time slots for the whole 24 hour window for all days in a week
    2.  The look of the 'Plan conversation' button to trigger the Growth conversation preparation AI agent was updated to the AI gradient theme
    3.  A decision table was introduced to map credentials for different types of permissions \(delegated/application\) that are used for scheduling Outlook meetings from the Conversations app
-   **Version 3.8.0 - December 2025**
    -   The scheduling experience for conversation series in the TD Conversations app has been improved. Previously, updating the date of an individual conversation would shift all upcoming discussions in the series. With this enhancement:
        -   The start date of the series is now captured during series creation.
        -   Subsequent discussions are scheduled strictly based on the selected cadence and the original start date.
        -   Updating the date of a single conversation no longer alters future discussions in the series.
    -   These changes provide more predictable scheduling and greater flexibility when managing conversation series.
-   **Version 3.6.3 - October 2025**

    'Plan conversation' button on the Career Conversations homepage was updated to invoke the agent 'Growth conversation preparation AI agent' instead of agentic workflow, 'Help plan growth conversations'.

-   **Version 3.6.2 - September 2025**

    Updates to 'Edit conversation' and addition of 'Edit series' option

-   **Version 3.5.2 - May 2025**
    -   Changed:
        -   Coral Theming changes
        -   API's for Persona Assistant for Conversations
-   **Version 3.4.0 - February 2025**
    -   Fixed:
        -   Accessibility issues
        -   Review skills modal padding issues
        -   Fixed console errors in Conversations when TD Core is not installed in the instance
        -   Browser compliance issues
-   **Version 3.3.0 - November 2024**
    -   Surfaced developing skills in employee career conversations
    -   Surfaced skill activity insights in the validation flow
-   **Version 3.2.0 - August 2024**
    -   Fixed:
        -   Improved scope security
        -   Various usability defects
-   **Version 3.1.2 - May 2024**
    -   New: Goals are included in the conversation details side panel when the "Employee Goals" application is installed
    -   Changed:
        -   Employees can now initiate conversations with their managers
        -   Mentees can now initiate conversations with their mentors
    -   Fixed: Various issues related to user experience
-   **Version 3.0.3 - February 2024**
    -   New
        -   Added support for mentoring conversations
        -   Added support for Outlook/Exchange integration to create conversation meetings
        -   Added support for Suggested talking points widget for Growth Plan Check-ins
-   **Version 2.0.2 - January 2024**

    Added fixes for empty ACLs.

-   **Version 2.0.1 - November 2023**
    -   New:
        -   Quarterly patch containing fixes only.
        -   Reference the linked documentation for more details on features, configurations, and other setup instructions.
-   **Version 2.0.0 - September 2023**

    EGD Activities provides managers and employees with tools to enable employee growth and development. Activities includes EGD Discussions, a tool to help guide managers and employees prepare for and have more frequent manager/employee growth conversations.

-   **Version 1.0.4 - August 2023**
    -   New
        -   Initial release of Employee Growth &amp; Development functionality.
        -   Contains Conversations application
        -   Reference the linked documentation for more details on features, configurations, and other setup instructions.

