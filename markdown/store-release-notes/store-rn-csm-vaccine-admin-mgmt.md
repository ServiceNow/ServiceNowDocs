---
title: Vaccine Administration Management release notes
description: Version history for the Customer Service Management Vaccine Administration Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-vaccine-admin-mgmt.html
release: store
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Vaccine Administration Management release notes

Version history for the Customer Service Management Vaccine Administration Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.0.2 - February 2025**

    Fixed: Minor defects.

-   **Version 9.0.1 - January 2025**

    Fixed: Remediated an insecure API that gave users incorrect table access.

-   **Version 9.0.1 - December 2024**

    Fixed: Remediated an insecure API that gave users incorrect table access.

-   **Version 9.0.0 - May 2024**

    Changed: Migrated the old VAM dashboards to the next gen UI dashboard experience.

-   **Version 8.0.2 - January 2024**
    -   Fixed:
        -   An issue has been fixed which on rare occasions allowed for appoinments to be evicted from the sn\_vaccine\_sm\_schedule without being booked.
        -   An issue has been fixed where users who were not logged in were unable to self-report vaccination status and test results.
-   **Version 8.0.0 - August 2023**

    New: Minor changes to true up to Vancouver

-   **Version 6.2.1 - August 2022**

    New: Added configuration to VAM property to enable scoped cache

-   **Version 6.0.1 - September 2021**

    Changed: Support for scheduling multiple vaccines in a single appointment

-   **Version 5.2.2 - July 2021**

    -   New: Ability for end users and agents to book subsequent appointments, if the first vaccine dose was administered and scheduled outside Vaccine Administration Management
    -   Fixed: Performance fixes and translations for application strings
    **Note:** In version 5.2.2, Vaccine Administration Management has been moved from Customer Service Management to Healthcare and Life Sciences.

-   **Version 5.1.3 - June 2021**
    -   New:
        -   Providers can configure multiple vaccine methods, with different eligibility criteria that can be used to automatically assign the appropriate vaccine
        -   Users will be able to select their vaccine method, if they are eligible for multiple vaccines \(and the provider has enabled method choice\)
        -   Clinicians can select the vaccine method, when they register and schedule appointments on behalf of end users
    -   Changed: The 'Home' and 'Appointment List' pages, which are part of the Clinician Portal, include layout and navigation changes
    -   Fixed: WCAG issues for Citizen and Clinician Portals
-   **Version 5.0.2 - May 2021**
    -   New:
        -   Clinicians can register a user as well as book and reschedule appointments for them. The same functionality can be used to support a call center use case.
        -   The clinician portal has a location filter that needs to be selected prior to showing appointments.
        -   End users can select a different location for each of their appointments during first-time booking or rescheduling. Clinicians can also do the same while booking appointments on behalf of a user.
    -   Changed:
        -   No-show appointments are represented as a distinct, separate state
        -   Self-registration and clinician-assisted registration only support email addresses with less than 40 characters
        -   Usability changes for the clinician portal
    -   Fixed:
        -   Data accuracy on the Appointment Dashboard for no-show and cancelled appointments
        -   Text label issues
        -   Performance changes
-   **Version 4.2.3 - April 2021**
    -   Fixed:
        -   Appointments that are active beyond the scheduled time are automatically canceled
        -   Canceled appointments show incorrect UI actions
-   **Version 4.2.2 - April 2021**
    -   New: Appointment configuration diagnostic scripts
    -   Fixed:
        -   Accessibility issues on citizen and clinician portal
        -   Minor issues with appointment configuration and inventory management
        -   Performance changes for appointment booking
-   **Version 4.1.4 - April 2021**
    -   Fixed:
        -   Optimized performance and functionality for the end user appointment booking experience
        -   Address corner cases with appointment booking and inventory configuration
-   **Version 4.0.5 - March 2021**
    -   New:
        -   End users
            -   Choose their own time and date for appointment
            -   Independently book second appointment
        -   Provider admins
            -   Configure a weekly schedule by location, with day and time slot overrides
            -   Manage inventory by location, including automated and manual distribution and manual waste tracking
            -   Perform scheduling based on available inventory
            -   Cancel appointments over a date range
        -   Clinicians
            -   Update inventory after the vaccine is administered
            -   Capture that the patient has given verbal consent
            -   Capture that the patient has been provided vaccine information
    -   Changed:
        -   End users: Ability to change calendars from 7-day view to 1-day view
        -   Provider admins
            -   Reduce booking contention with randomization of time slots
            -   Availability of two appointment slot options of 10 minutes and 15 minutes
        -   Support for Quebec Patch 1
    -   Fixed:
        -   End users: Rebook expired and no-show appointments
        -   Clinicians: Fixed questionnaire bugs
-   **Version 3.0.3 - March 2021**
    -   Fixed:
        -   Support for changing appointment dates to 12-hour and 24-hour formats
        -   Security fix
-   **Version 3.0.2 - February 2021**
    -   New:
        -   Appointment dashboards
        -   Ability to temporarily stop service at a vaccine location
        -   Scheduling of a second vaccination appointment after the first appointment is complete
        -   Mobile-friendly clinician experience
        -   Accessibility improvements for the end user and clinician portals
    -   Changed:
        -   QR codes are now embedded within emails, instead of linking users to a portal
        -   Filtering options for the clinician portal
    -   Fixed: Performance improvements for scheduling appointments
-   **Version 2.0.0 - February 2021**
    -   -   New:
    -   Ability to self-register and sign up for vaccinations
    -   Use QR codes for appointment notifications and verifications
    -   New clinician portal with support for tablets
    -   The eligibility criteria for self-service appointment booking is enabled by default
-   Changed: Improved the user portal experience
-   Fixed: Performance optimizations for mass booking
-   **Version 1.0.1 - January 2021**

    The ServiceNow® Vaccine Administration Management application enables organizations, such as governments and healthcare providers, to create and manage vaccination programs. Vaccine recipients can visit a self-service portal to review and provide privacy consent, use the knowledge base or Virtual Agent to address common questions, and self-schedule their appointment after responding to an eligibility questionnaire. Providers can schedule appointments for groups of eligible recipients, notify citizens and patients, administer and record vaccinations, and manage vaccination tasks.


## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

