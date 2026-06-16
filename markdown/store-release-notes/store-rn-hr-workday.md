---
title: HR Service Delivery Integration with Workday release notes
description: Version history for the HR Service Delivery Integration with Workday on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-workday.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# HR Service Delivery Integration with Workday release notes

Version history for the HR Service Delivery Integration with Workday on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.6.2 - June 2026**

    Fixed: A job tracker was not created for Pull To-Do's

-   **Version 3.6.1 - April 2026**

    Fixed: Termination details in ServiceNow are now updated or removed when a termination or resignation is withdrawn or rescinded in Workday.

-   **Version 3.6.0 - February 2026**
    -   New:
        -   Sync employee termination information from Workday into the HR Service Delivery integration with Workday App.
        -   Update personal details within ServiceNow and sync those changes to Workday.
-   **Version 3.4.11 - December 2025**

    Minor fixes.

-   **Version 3.4.1 - August 2025**
    -   Problem: During the storecertificationIT test, the RUN AS field in a scheduled job trigger referenced a user not present by default in the instance, causing execution failure.
        -   New: Introduced validation to ensure RUN AS users are present in the instance before execution.
        -   Changed: Updated the trigger configuration to reference a valid default user.
        -   Fixed: Corrected the invalid user reference in the transformation logic to prevent execution failure.
        -   Removed: Eliminated dependency on non-default users for scheduled job execution.
    -   Problem:The primary field on future worker job records was being overwritten during transformation, triggering unintended user updates before the official start date.
        -   New: Added logic to safeguard future-dated job records from premature updates.
        -   Changed: Modified the transformation flow to respect start-date constraints on primary field updates.
        -   Fixed: Resolved the issue causing early updates by correcting the transformation behavior.
        -   Removed: Removed the faulty logic that allowed overwriting of future worker job data.
-   **Version 3.4.0 - May 2025**

    Minor bug fixes.

-   **Version 3.3.6 - February 2025**
    -   The delivered integrations between ServiceNow HR Service Delivery and Workday HR application include the following experiences:
        -   Employee synchronization  Pull to-dos 
    -   New Functionality:
        -   Improve the HR Service Delivery Integration with Workday sub-flow in the workday HR spoke to provide agent's ability to retrieve employees' professional profile details from Workday.
    -   Below are the high level features added: 
        -   Importing and updating physician profile-related data from Workday into ServiceNow. 
        -   Enabling detailed physician information from Workday to be viewed and used within ServiceNow.
-   **Version 3.1.2 - June 2024**
    -   The delivered integrations between ServiceNow HR Service Delivery and Workday HR application include the following experiences:
        -   Employee synchronization
        -   Pull to-dos
-   **Version 3.1.1 - February 2024**

    Minor fixes.

-   **Version 3.1.0 - November 2023**

    New: Integrate HR Service Delivery Integration with Workday with localization tools.

-   **Version 3.0.0 - August 2023**
    -   New:
        -   Enabled Workday OAuth 2.0
        -   Enabled Approval workflows:
            -   Time Off Request
            -   Leave of Absence
            -   Time Sheet
            -   Compensation Change
            -   Job Requisition;
            -   Correct Time Off
            -   Termination
            -   Spend authorization / expense
            -   Change Job
-   **Version 2.0.6 - October 2022**

    Fixed: Includes fix for Workday Rescind employee

-   **Version 2.0.5 - August 2022**

    Fixed: Fixed the issue to reflect correct To-dos status in ServiceNow, when the user selects 'save for later' in Workday and completes the approval.

-   **Version 2.0.4 - February 2022**

    Fixed: Add system property to store exclude contingent worker type to be pulled in Get Worker Service

-   **Version 2.0.3 - October 2021**
    -   Fixed:
        -   Call get worker service via dynamic flow from get workers subflow
        -   Remove look up worker action from HRSD Workday app and change the reference to Look up workers and employment info action in workday HR Spoke
        -   Import sets are not passed from Get worker to Get Worker service Flow
-   **Version 2.0.2 - August 2021**
    -   Fixed:
        -   Handle parsing exceptions whenever WD is sending invalid characters.
        -   Utilize the page count configured via system property
        -   Country wasn't getting transformed correctly
        -   Log incorrect details in Job tracker for future workers
        -   Remove incorrect ACL on syslog\_app\_scope
        -   Fix for Rome issue for Get Locations Service flow. Script include call not working in inline script
-   **Version 2.0.1 - May 2021**

    New: Added dependency to Enterprise Service Management Integrations Framework 3.2.0

-   **Version 2.0.0 - April 2021**

    New: Pull tasks from Workday and display as todos in ServiceNow Employee Service Center.

-   **Version 1.0.3 - January 2021**

    This integration with Workday pulls and syncs employee profiles from Workday into ServiceNow HR Service Delivery on a scheduled basis.


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

