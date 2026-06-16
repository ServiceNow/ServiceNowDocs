---
title: Workplace Space Management release notes
description: Version history for the Workplace Space Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-space-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Space Management release notes

Version history for the Workplace Space Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.20.1 - June 2026**
    -   New:
        -   Introducing the new &amp; improved Space Planning module in Workplace Central
            -   Enhanced Space Planning. Plan space, allocations, and moves directly on the floor map and stack plan. Surface and execute moves on single- or multi-user selection, view allocations by Department, Cost Center, Workplace Entity, or Neighborhood, and switch view-bys with a single default applied at load.
            -   Allocation workflows on the floor map. Allocate or remove space allocations for single and multi-space selections from a streamlined dialog, with allocation choices for Department, Cost Center, and Workplace Entity.
            -   Configurable KPIs and View-Bys. Administrators can configure which KPIs and View-By options appear on the space planning floor map, with persisted user preferences.
            -   Scenarios and Space Requests in Space Planning. Scenarios and Space Request tabs are now surfaced inside the Space Planning experience to keep planning context in one place.
            -   Space Management administration module. A new Administration module for Space Management is available in the navigator for quick access to admin actions.
            -   Move details on User Card. Move details now appear on the User Card when surfaced from Global Search, giving planners full move context without leaving the page.
    -   Changed:
        -   Unified record page experience. The Space Assist Request page has been migrated to the standard record page for a consistent experience.
        -   Accessibility compliance. Workplace Space Management now meets WCAG 2.2 AA standards, including 400% zoom and reflow support.
    -   Fixed:
        -   Local administrators can now view space plan details correctly on the My Tasks page.  \{PRB2014276\}
        -   Green confirmation tick marks now appear when changing the building or floor in a space plan.  \{PRB2001503\}
        -   The Space Assist Request draft form now displays entity types for a pre-filled form, not just the cost center field.  \{PRB1999753\}
-   **Version 1.19.3 - May 2026**

    Fixed: Drag and Drop bars in the Stack Plan for Scenario Planning was not working in the latest version of Chrome Browser. This has been fixed now.

-   **Version 1.19.1 - April 2026**

    Increasing version number to align with the releases.

-   **Version 1.19.0 - March 2026**
    -   New: Automated workplace location assignment for new hires during HR pre-boarding.
    -   Fixed:
        -   When using the building overview, the allocation profile was not populated while adding or changing allocation via bulk editing spaces on floor map.
        -   Security fixes
-   **Version 1.18.2 - December 2025**
    -   New:
        -   Select spaces on floor maps using multiple criteria for more precise and efficient space management using Space Filter on both Building Overview and Scenario Planning
        -   Assign, unassign, and move users between neighborhoods within buildings using the map-based admin tool.
        -   Generate direct links to spaces, floors for quick navigation and sharing from Building &amp; Scenario Planning View. Navigate to Map View in Workplace Central from Platform view for Space/ Floor/ building records
        -   Improved map-based admin tool with optimized marker placement and visibility of all assigned employee names on the map along with Space names.
        -   Ability to visualize Bare Map in the Workplace Central Map View \(as in the Map Studio\) and quickly print it
    -   Changed:
        -   Enhanced space allocation and neighborhood controls to prevent conflicts and improve access rules
            -   Global setting to control space access for users without assigned departments, cost centers, or workplace entities
            -   Users are granted access to a space if the spaces are part of at least one of the restricted neighborhoods assigned to that space
            -   Prevent automatic deactivation of active or future allocations when processing new space requests
    -   Fixed:
        -   Match the Neighborhood colors in Location Directory and Scenario Planning
        -   Error on the schedule planner on Workplace central due to Timezone/Timeformat
        -   Avatar of users are not coming in floor map of building overview and scenario planning
-   **Version 1.17.0 - August 2025**
    -   Changed:
        -   Use the new neighborhood tables, that are part of Workplace Core.
        -   The banner image for the workplace dashboard has been updated.
    -   Fixed:
        -   Handle allocation of spaces in a SC Plan when the Group by - dept, cc, Workplace entity are made inactive or deleted
        -   In scenario planning group by Workplace Entity, colours of workplace entities are now matching in stack plan and for floor map
        -   Support commas in Department names for the View By/ Group By to ensure proper functionality and spaces being highlighted
    -   Removed: Moved neighborhood related tables to the Workplace Core application.
-   **Version 1.15.0 - May 2025**
    -   New: Support Scenario Planning using the Workplace Entity model aligned with organization's business hierarchy.
    -   Changed: Enhanced Move and Resize options for Scenario Planning stack changes.
    -   Fixed
        -   "Apply" button in Building Overview did not activate, blocking allocation updates.
        -   The data generation job for the Workplace Analytics Space Management report were not populating the "Utilization vs Capacity" table as expected.
        -   Legend selection was not functioning correctly in Map-based administration for certain View-by modes.
        -   Automated tasks for Space Assist requests were getting stuck in the "Work in Progress" state.
        -   Clipboard functionality was not working in Scenario Planning for specific Group-by modes.
        -   Time-bound allocation logic was not applied on the reservation search page in certain scenarios.
        -   The space recommendation conflict check logic did not account for allocation time effectiveness, resulting in inaccuracies.
        -   User assignment scheduled job continued to execute user assignment rules even when the neighborhood is inactive.
        -   New neighborhood assignments through Workplace Profile Location table were missing expected fields.
        -   Post-deployment, Space Assist requests default to "View-by: Cost Center" on the Floor Map tab, even when raised from the Workplace entity.
        -   Performance improvements.
        -   Security fixes.
-   **Version 1.14.0 - February 2025**
    -   Fixed:
        -   Conflict checks were performed only when a space assist request is opened in UIB, but they should also run during 'deploy' action to account for any allocation changes to the selected spaces.
        -   Schedule Plan did not support all date formats.
        -   Recommended spaces were not displayed as highlighted during the initial map load for space recommendation tasks.
        -   The 'Full Name' field in WSD Location tables was incorrectly calculated, showing all parent hierarchy values.
        -   On the Building Overview floor map, the "Remove Allocation" function removed the incorrect allocation type instead of the selected one.
        -   In Space Recommendation, raising a Space Assist request after deploying spaces does not update the execution table.
        -   In Space Assist requests, the execution table was not updating after deploying space options.
        -   In Scenario Planning, after selecting multiple spaces and performing the "Remove Allocation" action, the page became unresponsive.
        -   The selection of legend checkboxes did not function correctly when multiple allocations were configured for a single space.
        -   The right-side panel encountered issues in Building Overview and Scenario Planning when a single space had multiple allocations configured.
        -   The legend label tooltip with ellipsis was not displayed for workplace entities for spaces with multiple allocations in Scenario Planning and Building Overview.
        -   Building, floor, and space details were not displayed during user unassignment in Building Overview.
        -   In Building Overview, assigning or moving a user at the floor or area level did not recalculate the KPI on the Stack Plan tab.
        -   In Scenario Planning grouped by neighborhood, unassigning a user caused the neighborhood location assignment record to be removed instead of being deactivated.
        -   In Scenario Planning, previously selected values were not cleared when adding a new allocation or user assignment via floor map.
        -   Lasso selection of user assignments in map-based administration failed to function properly when the drawing intersects with username text.
        -   Performance improvements when loading building overview and scenario plans in Workplace Central workspace.
        -   Accessibility improvements implemented with improved page reflow, zoom and more.
        -   Security fixes.
-   **Version 1.13.0 - November 2024**
    -   New:
        -   The new schedule planner feature enables project owners to efficiently assign and manage employee assignments according to project timeframes.
        -   Through configuration, admins can now add more options to the "View By" dropdown, allowing them to color code plans and stacks by different data elements associated with the spaces, including custom fields.
        -   Admins can now configure the "View By" dropdown to remove or reorder options.
    -   Changed:
        -   Type-ahead support has been added for searching Departments, Cost Centers, Workplace Entities, and Neighborhoods when changing allocations using the floor map.
        -   The ability to access extra workplace location details within the Workplace Profile record.
    -   Fixed:
        -   Allocations made on the floor map tab were not reflecting in the stack plan tab.
        -   The "Assign to" dropdown option in the stack plan tab side panel was not refreshing.
        -   After applying the floor filter in the settings tab, other floors were still visible in the building map view.
        -   The space count and total capacity KPIs were showing double the actual records, and the default active spaces filter did not filter spaces in building view and scenario plan.
        -   The approver tab in scenario planning did not display the full list of approvers.
        -   In the Building Overview, the count of unassigned profiles for neighborhood grouping was not accurate.
        -   The "Reason for the Anomaly" field was editable when creating a new workplace profile location assignment record.
        -   Spaces were not allocated to a department in the floor map due to the Allocation Profile field being set to "None" during allocation change.
        -   Despite the scenario plan being in an approved state, users were able to resize and move the stack bars.
        -   Unable to create a space with the new space type classification.
        -   In space recommendations, the allocation logic rule for workplace entities should take into account the capacity of qualifying spaces instead of the number of space records.
        -   Performance improvements
        -   Accessibility improvements have been made. We have improved keyboard support, added IDs, alt text, contrast ratio, support for screen readers, and more.
        -   Security fixes.
-   **Version 1.12.0 - August 2024**
    -   New:
        -   Manage space allocations by setting start and end dates and receive advance notifications about allocation expiration.
        -   Department or Project representatives can now request space allocations with defined timeframes through space assist requests.
        -   New reservation configuration that incorporates the allocation duration when presenting available spaces.
        -   Create and visualize scenario plans spanning multiple buildings.
    -   Fixed:
        -   Unable to remove user records from the neighborhood user assignment list in Scenario Planning. This has been fixed.
        -   Discrepancies found in specific KPI calculations between stack plan and floor map right-side panels. This has been fixed.
        -   In the building view, selecting a floor after switching to the workplace entity level incorrectly displays building-level KPIs on the right-side panel instead of floor-level KPIs. This has been fixed.
        -   The complete list of buildings failed to load in the building list view within the Space Optimization module of Workplace Central. This has been fixed.
        -   Changes made to user assignments in scenario planning did not reflect in the building view after deploying the scenario. This has been fixed.
        -   Fixed an issue where space allocations were not updated after deploying cases from space requests.
        -   Security fixes.
-   **Version 1.11.1 - May 2024**
    -   New:
        -   View employee seat assignments on the floor map.
        -   Search for employees from user and workplace profile tables.
        -   Assign employees to spaces directly from the floor map.
        -   Manage neighborhood assignments via the stack plan within scenario planning.
    -   Changed: The neighborhood location data is now merged into the Workplace Profile Location Assignments table for efficient data management.
    -   Fixed:
        -   Workplace entity-based space recommendation options are being deployed without undergoing allocation conflict checks. This has been fixed now.
        -   Workplace user role holders encounter an empty workplace entity type dropdown while submitting space assist requests. This has been fixed now.
        -   Core admin users can select all neighborhoods in the "Browse by Neighborhood" path but can't view spaces if they lack neighborhood access, leading to inconsistency. Granted access to all spaces by excluding them from restricted neighborhood rules.
-   **Version 1.10.0 - February 2024**
    -   New:
        -   Any workplace profile anomalies are recorded when a user has a workplace profile assignment in a restricted neighborhood space.
        -   You can define space allocations by incorporating space ownership and tenancy alongside allocation percentages for greater granularity.
        -   You can assign a user without a workplace profile record into a neighborhood as an ad-hoc member.
        -   The updated Space Optimization and Occupancy dashboards now encompass multi-day reservation data and workplace entity filters.
    -   Fixed:
        -   Floor that contain a higher number of qualifying spaces are not given priority as the first option in the space recommendations.
        -   The reversed priority sequence of preferred location rules is impacting the precision of space recommendations.
        -   The protection policy of the non-SNC Script Includes has been changed, allowing for customizations by lifting read-only restrictions.
        -   Encountering error when attempting to update the Status field on a space.
        -   Security fixes.
-   **Version 1.9.1 - December 2023**

    Fixed: The protection policy status of the Script Include WSDSpaceRecommenderPopulateUtils has been changed, allowing for customizations by lifting read-only restrictions.

-   **Version 1.9.0 - November 2023**
    -   New:
        -   A customer hierarchy model is introduced to link your business hierarchy with spaces, offering you control over the space consumption logic based on the association. With this hierarchy, you can do the following:
            -   Create and manage hierarchical business structure utilizing the new workplace entities table, facilitating associations between locations and businesses.
            -   Support space consumption \(via hoteling and permanent workplace assignments\) management based on space allocations within the organizational hierarchy and accommodate space requests at entity levels.
            -   Offer data visualization options \(view-by\) on the floor map/stack plan for various hierarchy levels, enabling drill-down functionality.
            -   Space utilization dashboard in Workplace Central that supports data visualization using different workplace entity levels.
            -   Choose a workplace allocation type, that empowers customers to determine space association based on department, cost center, or workplace entity hierarchy.
        -   Introduced additional space classification fields - Space Function and Occupancy Status. You can now visualize the floor map and stack plan based on these criteria.
        -   You can now view, add, and remove neighbourhood-level user assignments through Workplace Central's map-based administration.
    -   Changed: You can now create or update workplace profile records with Allocation and Assignment type anomalies during scenario plan deployment and execution of move cases.
    -   Fixed:
        -   Earlier, the 'Proximity at' field in space recommendation rules displayed incorrect choices. This issue has been fixed.
        -   After upgrading WSD plugins to the latest versions, error messages were displayed when opening the stack plan. This issue has been fixed.
        -   In the scenario plan map view, when users performed a multi-select \(lasso or bulk selection\), the cursor did not indicate if the "Shift" key was pressed. This issue has been fixed.
        -   In the map-based space administration feature, the right-hand side panel did not display the assigned user list when selecting a space. This issue has been fixed.
        -   General accessibility improvements have been made, such as screen readers, headings, and confirmation message enactments are now supported during scenario planning and map-based space administration.
    -   Removed: The 'Department &amp; Cost Center' allocation type has been deprecated and will no longer be supported across space management features.
-   **Version 1.8.0 - August 2023**
    -   New:
        -   Make field edits for single or multiple spaces using interactive floor map and witness real-time updates for seamless and efficient space management.
        -   Modify space allocations and reassign neighborhoods with the convenience of the interactive floor map.
    -   Changed: The "View-By" selection for building view has been relocated within the Map Settings.
    -   Fixed:
        -   Granular ACL improvements with reporting to prevent unauthorize access to sensitive column data.
        -   Previously, users with the scenario reader role were able to access scenario plans in Draft status through direct URLs. This issue has now been resolved.
        -   Earlier, the recommended space list displayed an option to add a 'New' space, which was incorrect. This issue has been addressed and fixed.
        -   In catalog requests, the space type selection field was not displaying any values. This issue has been resolved, and the field now shows the appropriate options.
        -   Changing the allocation type in the space allocation related list was not clearing the previous department or cost center values. Field values are now properly cleared when changing the allocation type.
-   **Version 1.7.1 - May 2023**
    -   New:
        -   Ability to configure space request approval and deployment process.
        -   New Space Optimization dashboard to track capacity and utilisation of meeting rooms, desks, etc.
    -   Changed: Updated recommended space options review and selection.
    -   Fixed:
        -   Earlier, the ability to push cost centre and department allocations down into the lower space hierarchy levels \(Push-down\) worked only for Workspace/Desk space types. This has been fixed now.
        -   Earlier, Save button was not disabled immediately after the Continue saving progress bar is 100% in stack plan. This has been fixed now.
        -   User message info improvements while configuring neighborhood spaces and assignments.
-   **Version 1.6.1 - February 2023**
    -   New:
        -   Create open and restricted neighborhoods and assign employees to them. Allow employees to reserve a space in eligible neighborhoods or let them search, browse or navigate using the location directory.
        -   You can now configure the business criteria that will enable the workplace system to provide the best available seating options to the departments raising space demands.
        -   You can now configure approvals and approve scenarios for space plan deployment.
    -   Changed:
        -   the 'Scenario mode' has now been separated from other "View-by" options to make the interaction more intuitive.
        -   The clipboard has been moved to the bottom of the stack plan panel to improve the user experience.
    -   Fixed:
        -   Scenario owners were able to edit scenario plans that were in the Approved or Awaiting approval states. This has been fixed now.
        -   Department/Cost Center values in the higher location hierarchy levels were inherited \(Push-down\) only by the spaces of Workspace/desk space types. This has been fixed now.
-   **Version 1.5.0 - December 2022**
    -   Changed: A stack plan's saving process will now be performed asynchronously. You can view the same via a new progress bar.
    -   Fixed: Earlier, the stack plan saving process that involved extensive allocation changes would get interrupted. This has been fixed now.
-   **Version 1.4.1 - November 2022**
    -   New:
        -   Space Optimization module in Workplace Central workspace provides an ability to assess the current space allocations and determine the best possible seating arrangements for the teams.
        -   Space planners can build strategic scenario plans to identify where they have excess capacity and reallocate or offload them easily via interactive stack plans.
        -   Space planners can easily visualize scenarios with the help of floor maps and make allocation/user assignment changes as part of their space planning.
        -   Perform employee space assignment and department space allocation changes in live data by deploying scenarios.
        -   Configurable BOMA type field allows space planners to classify spaces as per BOMA standard.
    -   Fixed:
        -   Earlier, when a location was marked for delete, the state of the location was not changed to "Retired" even after the deletion job executed. This has been fixed now.
        -   Earlier, user was able to set Planned start and end date range for a space outside of its parent location date range. This has been fixed now.
-   **Version 1.3.2 - August 2022**
-   **Version 1.2.2 - May 2022**
    -   New:
        -   You can now manage a space's lifecycle by capturing the status across the location hierarchy.
        -   You can track a space's status changes for space activation/retirement.
        -   You can control the availability of space by modifying the space's status.
-   **Version 1.1.11 - February 2022**
    -   Fixed: It is now possible to assign a room to an employee in the workplace profile.
-   **Version 1.1.8 - December 2021**
    -   Fixed: The background colour of the completed-value in the "Push down" state field was hardcoded.
-   **Version 1.1.5 - October 2021**
    -   New: Additional support has been added to support all the 22 languages that are currently available across the ServiceNow AI Platform.
-   **Version 1.1.1 - September 2021**
    -   Changed:
        -   More context to Push-down option – added a tooltip to this Push-down action button
        -   Updated content for Measurement details and units
        -   Content Label change for type "Both" to "Cost center and department"
    -   Fixed:
        -   Reason for anomaly color contrast is not legible and the Recalculate button has a lot of padding
        -   Fixed Recalculate button keyboard accessibility

