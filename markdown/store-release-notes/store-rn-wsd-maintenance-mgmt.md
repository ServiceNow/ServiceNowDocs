---
title: Workplace Maintenance Management release notes
description: Version history for the Workplace Maintenance Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-maintenance-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Maintenance Management release notes

Version history for the Workplace Maintenance Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.11.0 - June 2026**

    Changed: Workplace cases now open the record-page in Workplace Central.

-   **Version 1.10.9 - April 2026**

    Increasing version number to align with the releases.

-   **Version 1.10.5 - March 2026**
    -   Fixed:
        -   Opening the Maintenance Request catalog item did not show the interactive floor map for all languages.
        -   Performance improvements when creating maintenance plans with a large set of items.
-   **Version 1.10.1 - December 2025**
    -   Fixed:
        -   Maintenance plan records are not getting filtered when searching for a keyword in copy schedule pop up
        -   Preventive maintenance cases do not open on the correct time
        -   Maintenance Plan issues: Last Completion Time shows prematurely on schedule edit, and generated maintenance cases are missing from the Overview page.
-   **Version 1.9.1 - September 2025**
    -   New: New AI Agent to optimize cleaning schedules and other other maintenance plans based on expected attendance.
    -   Fixed: Schedules could not be copied as the dropdown is showing as empty when clicking on it.
-   **Version 1.8.1 - August 2025**

    Fixed: Unable to copy an existing schedule to a new maintenance plan.

-   **Version 1.7.0 - May 2025**
    -   Changed: Workplace Maintenance Management dashboard list views have been relocated to the common page within Workplace Central.
    -   Fixed: Scheduling was generating duplicate records in Workplace Maintenance Management.
-   **Version 1.6.0 - February 2025**

    Fixed bug related to Submit a Maintenance Request record producer.

-   **Version 1.5.0 - November 2024**

    Fixed a few Accessibility and Security issues.

-   **Version 1.4.3 - August 2024**

    Fixed: Minor issues related to UI and plan records dates.

-   **Version 1.4.0 - May 2024**
    -   New:
        -   You can now publish maintenance plans that are saved in Draft state.
        -   Demo data has been added for maintenance cases and services.
    -   Fixed:
        -   The issue with case creation in cases of canceled maintenance plans has been fixed.
        -   A few maintenance cases did not appear in the calendar view for specific date formats. This has been fixed now.
        -   Maintenance cases were generated for maintenance plans with end dates that were past the due date. This has been fixed now.
-   **Version 1.3.1 - February 2024**
    -   New:
        -   Support for multiple case templates
        -   New table "Workplace Maint Plan Service Configurations" to store the service configurations
        -   New table Workplace Maintenance Plan Record
        -   Introduced Appsee Analytics user journey tracking New Maintenance Plan creation flow and Tracking a Maintenance Plan flow
    -   Changed: Scheduled job that generates cases picks the appropriate service configuration for a plan record
    -   Fixed:
        -   Time zone issues while generating plan records
        -   Time zone issues in the scheduled job that generates cases
    -   Removed: Deprecated table Workplace Maintenance Schedule Service \(Workplace Maint Plan Service Configurations table to be used in its place\). Fix script migrates records to the new table.
-   **Version 1.0.13 - November 2023**

    Fixed: Issues related to creation of maintenance plans and schedules.

-   **Version 1.0.10 - August 2023**

    Fixed: Security and Performance issues.

-   **Version 1.0.6 - May 2023**

    New: New Maintenance Management Dashboard to track preventive versus corrective maintenance case trends.

-   **Version 1.0.4 - March 2023**
    -   Fixed:
        -   UI fixes:
            -   My Plans widget name fixed.
            -   Calendar view auto refreshes when a new schedule or case is added.
            -   Formatting Alerts on the UI.
            -   Fixed the 'Page not found' error when clicking a maintenance plan link from schedule.
            -   Date validations.
            -   Filters and Settings in Maintenance Cases related list.
            -   Error Messages.
        -   Roles:
            -   The enterprise\_asset\_editor role was removed from sn\_wsd\_maintenance.writer role.
            -   The availability of the Maintenance Mgmt module in Workplace Central is driven by roles.
        -   Accessibility:
            -   Key board short cuts fixed.
        -   Security fixes: Some security fixes.
-   **Version 1.0.3 - February 2023**

    ServiceNow Workplace Maintenance Management enables workplace maintenance planners to plan for preventive maintenance for facilities assets \(chairs, etc.\) and soft services like house-keeping, etc. At the same time, there is a provision to capture corrective or reactive maintenance like spills or messes or other breaks. Provide visibility into the preventive v/s corrective cases and associated trend and enables better decision making.


