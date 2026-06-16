---
title: Workplace Core release notes
description: Version history for the Workplace Service Delivery Workplace Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-safety-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Core release notes

Version history for the Workplace Service Delivery Workplace Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.28.1 - June 2026**
    -   Fixed:
        -   Long space names could overlap in the user card
        -   Reservations that re-triggered an approval were stuck in awaiting approval
        -   The assignment ratio when editing neighborhoods could be incorrect
        -   The assignment ratio was incorrect for neighborhoods without spaces in Workplace Central
        -   The tooltip to go back after opening the Floor Plan tab was incorrect
        -   In some cases, users or spaces remain pre-selected on load
        -   The map print option was not available for users with the Space Planner role
        -   Several usability enhancements with user assignment and space allocation controls
        -   Performance enhancements
        -   Security fixes
-   **Version 2.27.1 - May 2026**

    Changed: Enhanced API end points to support artificial intelligence platforms

-   **Version 2.26.3 - April 2026**

    Increasing version number to align with the releases.

-   **Version 2.26.1 - March 2026**
    -   New: Manage neighborhoods in Workplace Central
    -   Fixed:
        -   Performance enhancements when loading the interactive floor map using 'Find the space on a floor map' in a record producer.
        -   Security fixes
-   **Version 2.25.0 - January 2026**
    -   New:
        -   Core Business Suite for Workplace Services:
            -   As part of the admin setup, we have simplified the process for customers to create new spaces or edit existing ones using bulk upload capabilities.
-   **Version 2.24.6 - December 2025**
    -   New: Added the ability to edit the content and style of space, user, and neighborhood detail cards on Location Directory and Kiosk.
    -   Fixed:
        -   An error was generated when loading the page using a specific named views.
        -   Email scripts used for cases could enter infinite loops when specific data configurations exist.
        -   Performance enhancements
        -   Security fixes
-   **Version 2.23.2 - August 2025**
    -   New: Introduced the neighborhood tables to Workplace Core from Workplace Space Management. Migrated existing neighborhoods and their configurations to the new tables.
    -   Fixed: Security fixes
-   **Version 2.22.0 - May 2025**

    Security fixes.

-   **Version 2.21.0 - February 2025**
    -   Fixed:
        -   Using typeahead on reservation search page for a building could generate a warning message in the logs
        -   Improved support for translations
        -   Accessibility improvements implemented
        -   Security fixes
-   **Version 2.20.0 - November 2024**
    -   Fixed:
        -   Blocking a location could show an error message, preventing the record from being created.
        -   Security fixes
-   **Version 2.19.0 - August 2024**
    -   Fixed:
        -   Auto numbering field could create empty numbers when creating cases in bulk. This has been fixed.
        -   The approval menu item on the WS-portal shows a blank dropdown when using 'EC Theme' theme. This has been fixed.
    -   Removed: The Workplace Service portal has been deprecated. Customers who have downloaded the 2.18.1 or any older version will continue to have the service portal, and can continue to use it. Customers who have downloaded 2.19.0 or newer version of the app will NOT have the service portal.
-   **Version 2.18.1 - May 2024**
    -   New:
        -   Enabling reservations based on reservation and occupancy data through Location Directory maps
        -   Changes to Location Directory maps - Legend, Accessibility mode
        -   Changes to Space Details Card - Reservation button, Occupancy tag
-   **Version 2.17.0 - February 2024**
    -   Changed: The Workplace Manager Dashboard can now be accessed from the Workplace Central workspace. Customers who have installed 2.16.1 or earlier versions of the app can still access the old version of the dashboard. Customers installing the app for the first time from 2.17.0 version onwards can access the dashboard in Workplace Central only.
    -   Fixed:
        -   Clicking the view task-link in the email used on mobile opens the new task form.
        -   Requesting a Workplace service activity did not trigger the approval after adding a custom field used in the process.
        -   Improved translations for labels used between Knowledge Base and Location Directory.
        -   General translation improvements.
    -   Removed: The Workplace dashboard has been deprecated. Customers who have downloaded the 2.15.0 or any older version will continue to have the dashboard and can continue to use it. Customers who have download 2.16.1 or newer version of the app will NOT have the dashboard.
-   **Version 2.16.2 - January 2024**

    Security fixes.

-   **Version 2.16.1 - November 2023**
    -   New:
        -   The following workplace profile enhancements have been added:
            -   A new table is introduced to consolidate multiple workplace profiles created for an employee.
            -   You can now set one workplace profile as Primary for an employee.
    -   Changed:
        -   A fix script is added to support and facilitate the migration of an employee's multiple workplace profiles to the new m2m table for existing customers.
        -   It is now allowed to create or update workplace profile records with Allocation and Assignment type anomalies.
    -   Fixed:
        -   Earlier, the Workplace Manager Dashboard did not display any data during impersonation. This issue has been fixed.
        -   Implemented optimizations and fixes to enhance page load performance.
-   **Version 2.15.0 - August 2023**

    New: The application got renamed from Workplace Safety Management to Workplace Core. There are no changes in functionality.

-   **Version 2.14.1 - May 2023**
    -   New: Use alphabetical or apply a custom sorting to the location, floor, area, and neighborhood selectors in the Location Directory.
    -   Fixed:
        -   Earlier, the capacity ratio was not pushed down from floor to space level. This has been fixed.
        -   Earlier, generating QR codes from space type set the description to undefined. This has been fixed.
        -   Earlier, when using Mappedin maps, it was not possible to click on the horizontal cards. This has been fixed.
-   **Version 2.13.2 - March 2023**

    The release notes of the related plugins can be viewed on the respective plugin's release notes.

-   **Version 2.13.1 - February 2023**
    -   Changed
        -   Default email templates are updated to match the next experience content and style guidelines. The new templates are installed beside the old ones in cases the old ones already exist on the instance.
        -   Updated, where possible, the BRs to fetch location-related information using getValue instead of getRefRecord.
    -   Removed: Workplace Service Items cannot be added through the related list on the Rooms-table.
-   **Version 2.12.1 - November 2022**

    Changed: Added performance optimizations while loading the location directory.

-   **Version 2.11.1 - August 2022**

    Fixed: Workplace Services, Workplace Service Items, and Service Item sub category were not marked for translation.

-   **Version 2.10.3 - July 2022**

    Fixed: The DXF floor map will now load without any issues when requesting a space using the record producer.

-   **Version 2.10.1 - May 2022**
    -   New
        -   Make the Locations table structure available in the Workplace Safety Management Location tables.
            -   Migrate existing location types to the Workplace location tables.
            -   For new entries in the Workplace tables, the location type is automatically set based on the configuration.
    -   Changed: To improve translations, a 'Title' field is introduced on the request forms and on other pages \(e.g. in the floor picker searching for availability\).
    -   Fixed: Earlier, employees were not always assigned with the workplace user role when using client role assignments. This has been fixed now.
-   **Version 2.9.2 - February 2022**
    -   New
        -   A new Approval definitions module is available to configure custom approval flows for reservations.
            -   You can manage and set various approvers, prioritizations, and multi-step approvals.
            -   You can define approvers for workplace cases and reservations.
    -   Changed: The existing Approval Options in Workplace Case Management are migrated as Performer Criteria in Workplace Safety Management.
    -   Fixed
        -   The ACLs from different Workplace Service Delivery applications will no longer affect the normal template users who access template records.
        -   The space import will no longer fail if an end point or start point is not defined in a dxf entity.
-   **Version 2.8.1 - December 2021**
    -   New: A new module is introduced to enable users to generate and print QR codes for spaces.
-   **Version 2.7.5 - October 2021**
    -   New: Additional support has been added to support all the 22 languages that are currently available across the ServiceNow AI Platform.
-   **Version 2.7.2 - September 2021**
    -   New
        -   All the workplace services provided by ServiceNow can now be accessed from the Employee Center – A single unified portal for multi-department service delivery.
        -   Workplace contents are now classified as quick links, sections, and widgets under the Workplace main menu for both desktop and mobile experiences
-   **Version 2.6.1 - June 2021**
    -   New
        -   As a workspace manager, you can identify duplicate space names on a floor of a building. You can view the list of duplicate spaces created on that floor and make changes if required.
-   **Version 2.5.3 - March 2021**
    -   New:
        -   You can now configure new space types in Space Type Configurations.
        -   You can block a workplace location for a specific period. The workplace location will be unavailable for reservation during this period.
    -   Changed:
        -   In the Workplace Service Delivery - Suite, from Workplace Safety Management\[workplace-safety-management\] version 2.5.3, the Space type \(space\_type\) choice field is depreciated. After the upgrade, Space types are configured in the Space Type Configuration menu option. The Space type \(space\_type\) field is migrated as Space type \(location\_type\) field in the Space table \[sn\_wsd\_core\_space\]. Customers having customization on the depreciated Space type \(space\_type\) field are advised to manually migrate their flow to use the new Space type \(location\_type\) field. A new fix script, 'Populate Location Type from Space Type' is introduced to execute the scheduled job - 'Populate location\_type from space\_type' on the Space table \[sn\_wsd\_core\_space\] to migrate the depreciated Space type \(space\_type\) field value to the new Space type \(location\_type\) field. The Workplace Service portal home page text is changed.
-   **Version 2.3.3 - January 2021**
    -   New:
        -   Employees can now schedule their arrival for future dates as well.
        -   Multiple time zones are now handled efficiently while scheduling an arrival. A setting is added to automatically display the selected building's time zone when scheduling an arrival.
        -   It is now possible to cancel a single reservation from a multiple-day reservation.
        -   Two new properties are added to display only available buildings, floors, areas, and spaces while requesting reservations for multiple days and for a single day reservation. The property can be turned on/off.
-   **Version 2.3.3 - December 2020**
    -   New:
        -   Employees can now schedule their arrival for future dates as well.
        -   Multiple time zones are now handled efficiently while scheduling an arrival. A setting is added to automatically display the selected building's time zone when scheduling an arrival.
        -   It is now possible to cancel a single reservation from a multiple-day reservation.
        -   Two new properties are added to display only available buildings, floors, areas, and spaces while requesting reservations for multiple days and for a single day reservation. The property can be turned on/off.
-   **Version 2.2.4 - November 2020**
    -   Changed:
        -   From Workplace Safety Management \(sn\_wsd\_core\) version 2.1, all updates, and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal from Workplace Safety Management \(sn\_wsd\_core\) version 2.1.
        -   The Workplace Case Management Dashboard, Reservation Management Dashboard, and the Visitor Reception Dashboard are now accessible from the Workplace Safety Management application.
        -   The appearance of the Workplace Service Portal/Service Portal My request page is changed from the Paris release.
        -   The reservation check-in time duration has been modified. A reservation must now be checked in within 30 minutes from the reservation start time, otherwise, the reservation is canceled.
        -   The mobile web interface has been improved in the Now Mobile app.
        -   The Workplace Services Catalog can also be accessed from the Now Mobile app homepage.
-   **Version 2.0.3 - October 2020**
    -   New:
        -   A Workplace services portal with all the workplace service delivery related features
        -   Knowledge management to create and manage Knowledge articles for workplace services
        -   Check in and check out a reservation
    -   Changed: Restrict employees from making shift based reservation if they are not part of that shift
-   **Version 2.0.0 - September 2020**
    -   No updates from v1.4.3 to v2.0.0
-   **Version 1.4.3 - August 2020**
    -   New:
        -   Workplace managers can add a space to a shift ahead of time and allocate spaces to users.
        -   Workplace managers can use the same schedule for multiple shifts. In previous release versions, workplace managers needed to create a schedule for each shift.
        -   Workplace managers can close down a building, which will cancel all future reservations and disallow new reservations from being made until the building is reopened.
        -   Localization for features from the August 6 release.
-   **Version 1.4.0 - August 2020**
    -   New:
        -   Use the floor map upload to update existing records in Space Administration Tables, including the following changes:
            -   Preview updates before committing changes
            -   Changes are logged from any upload events
        -   Localization for features from the July 23 release
-   **Version 1.3.2 - July 2020**
    -   New:
        -   Workplace manager experience
            -   The workplace team can use the Workplace Manager Dashboard to:
                -   Review pending workplace requests
                -   Analyze available capacity for today \(spaces and areas\)
                -   Monitor today's arrival entries
                -   Review the trend of unassigned cleaning tasks
                -   Analyze space utilization using today's reservations by shifts
        -   Bulk assignment of workspaces
            -   Use shifts to create space reservations for multiple employees at once
            -   Assign spaces at a department level by adding employees from a specific department to a shift
            -   Make reservations for employees in bulk with a single click
        -   Auto-assignment of workspaces
            -   Employees' designated workspaces are automatically reserved for them based on the workplace user profile definitions
            -   Workplace location details of the employee are auto-populated on the self-service reservation forms
            -   Employees can select just the date, time, and/or shift on the reservation forms and a workspace will be auto-assigned to them
-   **Version 1.2.2 - July 2020**
    -   New:
        -   Additional roles
            -   Shift owner: Has visibility into details and workspace reservations for the shifts they own
            -   Workplace user: Employee who accesses the self-service for reservations
        -   Reserve an area: Define capacity for an area of a floor to facilitate area reservations for employees. Employees can work from any available space from that area when they return to office. You can also use this feature to define and manage capacity for other workspaces, such as neighborhoods.
        -   Campus-level shifts: If a shift applies to all the buildings, floors, and spaces in a campus, you can associate a shift directly to the campus.
        -   Schedule arrivals: Define arrival times at various locations of your workplace. Employees can schedule their arrival to these locations at one of the defined times so you can avoid large gatherings or long waiting lines.
        -   Floor plans
            -   Added a legend on the map to indicate the availability of the workspaces on each floor
            -   Hover the cursor over a booked space to see who the reservation is for
-   **Version 1.1.4 - June 2020**
    -   New:
        -   Floor maps feature
            -   Upload a floor map into ServiceNow. Only the AutoCAD .dxf format is supported.
            -   Populate Space Administration tables by uploading floor maps
            -   Render floor maps inside Workplace Safety Management
            -   Show reservable vs. non-reservable spaces on floor maps
            -   Show all definable locations on a floor map \(for example, campus, building, floor, areas, spaces\)
        -   Employee self-reservations for workspaces
            -   Make single or multi-day workspace reservations
-   **Version 1.1.1 - June 2020**
    -   New:
        -   4 new record producers are available for workplace managers:
            -   Add a Shift: Create a shift from the portal.
            -   Add a Task: Create ad-hoc and scheduled tasks from the portal. One task can be created per record producer submission.
            -   Reserve a space: Reserve a space for employees who are allocated to a shift.
            -   Add a planned task definition: Create planned tasks definitions without needing to go to the platform view.
    -   Changed:
        -   Updated workplace manager dashboard: Provides a capacity view and a workplace tasks view, based on site.
-   **Version 1.0.9 - May 2020**
    -   With the Workplace Core application, quickly configure sanitized and socially distanced workspaces for the return of employees. With department leaders, workplace service managers can reserve available workspaces for employees in shifts. Workspaces can be scheduled for disinfection before and after these shifts. With reports and dashboards, workplace managers can view how much of the available workspaces have been reserved. Workplace managers also have a real-time view of all cleaning task statuses, including a full audit trail history.

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

