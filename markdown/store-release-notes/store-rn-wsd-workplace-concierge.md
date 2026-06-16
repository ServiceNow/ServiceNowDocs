---
title: Workplace Concierge release notes
description: Version history for the Workplace Concierge application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-concierge.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Concierge release notes

Version history for the Workplace Concierge application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.6 - June 2026**

    Fixed: Workplace profiles were created while loading the presence-page, instead of when the employee saves the presence information

-   **Version 1.7.1 - May 2026**

    New: The introduction of new API end points to support artificial intelligence platforms

-   **Version 1.6.11 - April 2026**

    Increasing version number to align with the releases.

-   **Version 1.6.7 - March 2026**
    -   Changed: The first day of the week property is honored when setting routines.
    -   Fixed:
        -   The title, rather than the name, was displayed in the "Sit near" field on the Workplace Preferences page.
        -   In some cases, reservations were not displayed in the agenda view.
        -   An error was displayed related to Moment Timezone for several languages on the search and workplace pages.
-   **Version 1.6.0 - December 2025**
    -   Changed:
        -   The option to change my in-office plan got moved below the calendar in the mobile Workplace-experience
        -   Editing a reservation in the Workplace mobile experience now also display smart suggestions
    -   Fixed:
        -   No error message was displayed when there was no reservable module made available for the mobile Workplace-experience
        -   Corrected the value from "workplace\_experience" to "workplace experience" in the reservable module definition when Workplace Concierge is installed
        -   Performance enhancements when loading the Workplace-tab in NowMobile
        -   Security fixes
-   **Version 1.5.4 - September 2025**

    Fixed: The presence status was not displayed on the workplace page in certain timezones.

-   **Version 1.5.1 - August 2025**

    New: Employees can set their in-office days in the In-office preferences in the new Workplace experience on NowMobile.

-   **Version 1.4.2 - May 2025**
    -   New: Employees can reserve a workspace \(desk\) using the new mobile Workplace experience. They can reserve workspaces using personalized suggestions, view planned workspace reservations, or view the space on the map using the Workplace Location Directory experience on the employees' mobile.
    -   Fixed: An incorrect entry was added to the system logs when an employee created a reservation without a workplace profile.
-   **Version 1.3.1 - February 2025**

    Fixed: Improved support for translations.

-   **Version 1.3.0 - November 2024**
    -   Fixed:
        -   Creating a reservation for a specific date displayed the reservation over two days.
        -   When visiting another location, the employee was notified incorrectly about reserving a space on their remote day.
        -   The collaborator percentage was not updated when any collaborators change their routine.
        -   An incorrect insight was displayed on the dashboard when the employee set an exception to visit another location and created a reservation for that day.
        -   In some cases, the current date on the dashboard was incorrectly displayed.
        -   Security fixes
-   **Version 1.2.0 - August 2024**
    -   Fixed:
        -   An error was displayed in the presence dashboard for recurring reservations. This has been fixed.
        -   Remote exceptions were not cancelled when changing the routine. This has been fixed.
        -   Security fixes
-   **Version 1.1.3 - May 2024**
    -   New:
        -   Employees can make their workplace presence information private
        -   New presence dashboard with personalized information that highlights schedules and collaborators and makes exceptions on the spot
        -   Show personalized insights on collaboration opportunities on the presence dashboard
    -   Changed: Use suggestions to add collaborators
-   **Version 1.0.2 - February 2024**

    ServiceNow Workplace Concierge provides employees with real-time insights to optimize their on-site presence in the workplace with their co-workers to improve team collaboration and learning.


