---
title: Employee Profile release notes
description: Version history for the Employee Profile application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-employee-profile.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Employee Profile release notes

Version history for the Employee Profile application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.1 - June 2026 \(Australia\)**

    Updated to support the latest version of the dependent apps.

-   **Version 13.6.8 - June 2026 \(Zurich\)**

    Updated to support the latest version of the dependent apps.

-   **Version 14.0.0 - June 2026 \(Australia\)**

    Updated to support the latest version of the dependent apps.

-   **Version 13.6.7 - June 2026 \(Zurich\)**

    Updated to support the latest version of the dependent apps.

-   **Version 13.6.6 - May 2026**

    Added the RCA and fixed the defects.

-   **Version 13.6.3 - March 2026**

    Fixed issues with accessing Employee Profile from the portal.

-   **Version 13.5.2 - February 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 13.5.1 - January 2026**

    Fixed Employee Profile access issues.

-   **Version 13.5.0 - December 2025**

    Updated to support the latest version of the dependent app.

-   **Version 13.3.2 - September 2025**

    \[Security Bug Fix\] Resolved ACL Bypass in ep\_UtilsSNC caused by GlideRecord Usage.

-   **Version 13.3.1 - August 2025**

    Updated to support the latest version of the dependent apps.

-   **Version 13.1.3 - June 2025**
    -   Resolved the following bugs:
        -   Users were unable to encrypt attachments with the sn\_employee.admin role after upgrading to Xanadu.
        -   Users faced tablet responsiveness malfunction on the appointment booking pages when the dynamic window is pinned.
-   **Version 13.1.2 - May 2025**
    -   Implemented the profile summary API as part of the HR persona framework. Resolved the bug in logging a warning message instead of an error message if the solution record is not present, while fetching similar employee profiles.
    -   Get topic level security in My Favorites widget and Conversational LLM support to resolve tasks and approvals in Employee Center.
-   **Version 13.0.2 - February 2025**
    -   Fixed bugs that impacted the user interface, including:
        -   Removing duplicate menu items from drop-down lists.
        -   Removing duplicate user profiles caused by generating profiles based on system users, then installing HR core.
-   **Version 12.1.1 - November 2024**

    Fixed user interface, accessibility, and security issues.

-   **Version 12.0.2 - August 2024**

    Addition of Employment History, Education and Training, and Languages Spoken, related tables under employee profile. New Profession tab is added under employee profile for visibility of user's professional profile on Employee Center.

-   **Version 11.0.3 - May 2024**

    Improved configuration to allow the employee profile to be configured differently for different portals.

-   **Version 10.0.1 - February 2024**

    Define dotted-line reporting relationships between employees and managers in the Organization Chart and the My Team section in the Employee Profile. \(Requires Employee Center Pro\).

-   **Version 9.0.1 - November 2023**

    Enabled admins to configure which fields to display in employee profile header Added widget overview section for quick navigation to specific widgets on an employee profile tab Enabled admins to add multiple instances of the Profile Overview widget to the Employee Profile UI across tabs.

-   **Version 8.0.2 - August 2023**

    Skills profile was added as an extension of the employee profile.

-   **Version 7.0.6 - May 2023**

    Changed:

    -   Admins can easily organize additional work-related details by configuring different tabs on the Employee Profile page and widgets on each tab.
    -   Admins can configure the visibility of widgets on each tab to different user groups including employee, manager, or everyone by user criteria.
    -   Admins can specify which widgets an employee can personalize for their public profile.
    -   Employees can personalize their public profile by specifying visibility of widgets to self, manager, or everyone.
-   **Version 4.0.2 - May 2022**

    New:

    -   Actions, such as connecting via emails and calls, can be configured on the employee profile page.
    -   MS Teams: added presence indicator
    -   Built-in image editor \(rotate, zoom in/out, flip, focus\) for the  profile picture and background banner.
    -   HRSD customers: The HR widgets are available by default on the employee profile.
-   **Version 3.0.5 - February 2022**
    -   New:
        -   An updated Employee Profile table that includes bio, preferred pronoun and more.
        -   A configurable employee profile UI that lets employees view profile and work related information.
        -   Employee Profile UI configuration that lets admins easily organize the information on the profile page.
        -   AI/ML similar user data model based on employee profile that is used to drive content recommendations.

