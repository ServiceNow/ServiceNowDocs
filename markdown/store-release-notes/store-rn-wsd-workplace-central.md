---
title: Workplace Central release notes
description: Version history for the WSD Workplace Central application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-central.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Central release notes

Version history for the WSD Workplace Central application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.16.1 - June 2026**
    -   New:
        -   Introducing the new &amp; improved Space Planning module in Workplace Central
            -   Unified Navigation. The Space Planner has all the necessary tools in a single module in Space Planning &gt; Floor Maps, Stack Plan, Workplace Profiles, Spaces, Scenarios, Neighborhoods and Space Requests.
            -   Enhanced Space Planning. Plan space, allocations, and moves directly on the floor map and stack plan. Surface and execute moves on single- or multi-user selection, view allocations by Department, Cost Center, Workplace Entity, or Neighborhood, and switch view-bys with a single default applied at load.
            -   Allocation workflows on the floor map. Allocate or remove space allocations for single and multi-space selections from a streamlined dialog, with allocation choices for Department, Cost Center, and Workplace Entity.
            -   Configurable KPIs and View-Bys. Administrators can configure which KPIs and View-By options appear on the space planning floor map, with persisted user preferences.
            -   Scenarios and Space Requests in Space Planning. Scenarios and Space Request tabs are now surfaced inside the Space Planning experience to keep planning context in one place.
            -   Space Management administration module. A new Administration module for Space Management is available in the navigator for quick access to admin actions.
            -   Move details on User Card. Move details now appear on the User Card when surfaced from Global Search, giving planners full move context without leaving the page.
        -   Introducing Case Visualization
            -   List &amp; Calendar for cases. View and manage workplace cases on a new Calendar view in Workplace Central under Case Management module, with click-through to a side panel for quick case details and actions. Unified filters apply and retain across the Calendar and List View with ability to Group Cases on the Calendar View.
        -   Other enhancements
            -   Facility Asset management. Access and manage facility assets directly in Workplace Central through a new standard record page with all asset-related tabs.
            -   Workplace Central in Unified Navigation search. The Workplace Central application is now available from the Unified Navigation search context menu for faster access.
    -   Changed: Unified record page experience. Case Management, Space Management and Move Management custom record pages have been migrated to the standard record page experience.
    -   Fixed:
        -   The Maintenance Items tab no longer returns an empty list when the system property glide.invalid\_query.returns\_no\_rows is enabled.  \{PRB2022829\}
        -   Field selection under Maintenance Management in the Workplace Central workspace now behaves correctly.  \{PRB2000350\}
        -   Record creation from within Workplace Central workspace lists now works as expected \(Lease Management Module\).  \{PRB2019165\}
        -   Workspace notifications now load with accurate counts and navigate to the correct records when clicked.  \{PRB1932045\}
        -   Button order in the Workplace Central workspace for Cases is now consistent after the initial save.  \{PRB2007913\}
-   **Version 1.15.4 - March 2026**
    -   New:
        -   Workplace Core module
            -   New "Space Planning" module to view floor maps, spaces, Workplace Profiles, and neighborhoods.
            -   Assign/unassign users to seats from the floor map, individually or in bulk.
            -   View neighborhood assignments and seat/user KPI, and perform actions to manage allocations and assignments.
            -   Typeahead search for spaces and users and load floor map and highlights the user's location based on the selection.
    -   Changed: Enhanced the settings panel to configure floor map display preferences.
    -   Fixed: The maintenance items count should initially display the total inventory count.
-   **Version 1.15.1 - December 2025**
    -   New:
        -   Space Management module:
            -   Select spaces on floor maps using multiple criteria for more precise and efficient space management using Space Filter on both Building Overview and Scenario Planning
            -   Assign, unassign, and move users between neighborhoods within buildings using the map-based admin tool.
            -   Generate direct links to spaces, floors for quick navigation and sharing from Building &amp; Scenario Planning View
            -   Improved map-based admin tool with optimized marker placement and visibility of all assigned employee names on the map along with Space names.
            -   Ability to visualize Bare Map in the Workplace Central Map View \(as in the Map Studio\) and quickly print it
        -   Move Management module:
            -   Bulk Moves Experience Enhancements
                -   Better stepper expeerience
                -   Handle routing back to the same step where the user left off last and continue processing
                -   Data Conflicts/ Business Conflicts editing cues
        -   Workplace Dashboards Landing Page
            -   AI-powered Workplace Insights generated by Now Assist
    -   Fixed:
        -   Workplace case management:Mini Email composer not coming up when opening Case record using /record link in workspace
        -   Ability to change form view in record page \(Space\) in Edit Space from Building Overview
        -   After clicking on deploy button Initially modal is not loading on scenario plan
        -   Inactive user assignments showing up on the Map and not editable
        -   Workplace case management: Task printing option is missing in workplace central
-   **Version 1.14.5 - September 2025**

    Fixed: In some cases, when creating a new maintenance plan, the schedule page took a long time to open or it did not open at all.

-   **Version 1.14.0 - August 2025**
    -   New: Ability to efficiently create and manage bulk move requests by uploading a spreadsheet containing essential move details such as employee information, current locations, and new location
    -   Fixed:
        -   Not all departments/cost centers/Neighborhoods/Workplace Entities were loaded when applying allocations using map-based space management.
        -   The label "Use following filter to select spaces \(maximum 20000 spaces\)" did not support translations.
        -   The label "Go back to stack plan" did not support translations.
-   **Version 1.12.2 - May 2025**
    -   New: Support Scenario Planning using the Workplace Entity model aligned with organization's business hierarchy.
    -   Changed: Certain dashboard lists have been moved to a dedicated list page in Workplace Central.
    -   Fixed:
        -   The '+' icon and space names were not appearing for all eligible unassigned spaces on the Map based Space Administration.
        -   Translation fixes.
-   **Version 1.10.3 - February 2025**
    -   New:
        -   Added Indoor Mapping for Kiosk configuration module
        -   Ability to print maps for map based administration
    -   Fixed:
        -   The side context form filter did not show locations corresponding to the selected floor when a new floor was selected.
        -   In Scenario Planning grouped by neighborhood, the user assignment action was available even for spaces not associated with any neighborhood.
        -   Scenario Planning allowed stack bars to be moved to different floors using the floor dropdown, despite the state being approved.
-   **Version 1.9.0 - November 2024**
    -   New: Introduced the "Schedule Planner" module, allowing project owners to schedule employee assignments.
    -   Fixed:
        -   The selected Building and Floor were not populated when clicking a bar in the stack plan on the scenario planning.
        -   The option to disable the display of title and marker for a place type was ignored in the scenario planning map component.
        -   The header was missing in the confirmation dialog when moving users via the floor map.
        -   Accessibility improvements have been made. We have improved support for screen readers, alt text, contrast ratio,and more.
        -   Performance improvements.
        -   Translation fixes.
-   **Version 1.8.2 - August 2024**
    -   New: Create and visualize scenario plans spanning multiple buildings.
    -   Fixed:
        -   Accessibility improvements.
        -   General performance improvements.
-   **Version 1.7.1 - May 2024**
    -   New:
        -   View employee seat assignments on the floor map.
        -   Search for an employee from the user and workplace profile table.
        -   Assign employees to spaces directly on the floor map.
        -   Trigger employee relocations within and between buildings directly from the floor map.
        -   Access employee information with move and assignment actions on map cards in the side panel.
        -   Manage neighborhood assignments via the stack plan within scenario planning.
    -   Changed: The Execution plan is now divided into two tabs, capturing both user and space-related changes within the scenario plan.
    -   Fixed:
        -   Workplace entity-based space recommendation options are being deployed without undergoing allocation conflict checks. This has been fixed now.
        -   The Deploy button remains enabled after deploying a selected space option. This has been fixed now.
        -   The contextual side panel displays empty fields until the floor is loaded when accessing the Floor map section in map-based administration. This has been fixed now.
        -   Performed general performance improvements of the Scenario Planning Save, Send for Approval, and Publish actions.
        -   Performed general translation improvements.
-   **Version 1.6.0 - February 2024**
    -   Changed: In the Occupancy dashboard, added a new filter "Workplace Entity"
    -   Fixed:
        -   Unable to remove the neighborhood allocations using Map-based space administration view.
        -   The Stack Plan KPIs aren't updating following the assignment of users to neighborhoods.
        -   Confirmation message appears for the allocation change even when there are no allocations present.
        -   The data doesn't refresh promptly upon changing the view options in the stack plan, even after the loading symbol disappears.
        -   Unable to change view-by options while the scenario is in the awaiting approval state.
        -   Accessibility improvements have been made. Added ID's, updated labels, improved color contrast ratio, and more.
        -   General translation improvements in Move Scheduler.
        -   General performance changes when loading the building page.
-   **Version 1.5.0 - November 2023**
    -   New:
        -   The following dashboards have now been migrated to the Workplace Central workspace. A new tab - Workplace Dashboards is introduced from where you can access the dashboards:
            -   1. Reservation Mgmt Dashboard
            -   2. Workplace Case Dashboard
            -   3. Workplace Manager Dashboard
            -   4. Visitor Reception Dashboard
            -   5. Synchronization Health Dashboard
        -   You can now manage your reservations and reservation-related actions using the new Event Planner in the Workplace Central plugin. The Event Planner enables you to:
            -   View reservations using a schedule view.
            -   Optimize space reservations by manually changing the start date and time, or location.
            -   Manage reservations quickly and easily on behalf of employees.
        -   A new customer hierarchy model has been introduced so that you can associate a business hierarchy with spaces. The hierarchy provides you with the following:
            -   Data visualization options \(view-by\) on the floor map/stack plan for various hierarchy levels, are also enabled with a drill-down functionality.
            -   A space utilization dashboard that supports data visualization using different workplace entity levels.
        -   Additional space classification fields - 'Space Function' and 'Occupancy Status', have been introduced. This floor map and stack plan can be visualized based on these criteria using the View by option.
        -   You can now view, add, and remove neighborhood-level user assignments through map-based administration.
    -   Fixed:
        -   Earlier, issues were encountered while changing the floor from the floor map in Tokyo instances. This issue has been fixed.
        -   After upgrading WSD plugins to the latest versions, error messages were displayed when opening the Stack plan. This issue has been fixed.
        -   Earlier, the KPIs in the right-hand panel of the floor map and the stack plan were occasionally not refreshed while scenario planning. This issue has been fixed.
        -   Earlier, the settings filter in the map-based space admin floor map was intermittently not performing as expected. This issue has been resolved.
        -   General accessibility improvements have been made in map-based administration and scenario plan features. Screen readers, keyboard shortcuts, tooltips, headings, labels, and more are now supported.
-   **Version 1.4.0 - August 2023**
    -   New:
        -   An Occupancy Dashboard is now available. You can view the dashboard only if the Workplace Connectors application is installed.
        -   Track move cases and associated tasks seamlessly with the new Move management module.
            -   Utilize the Move Scheduler, a visual move planning tool, to group move cases into projects. Create an organized and logical plan for implementing bulk moves in your workplace.;
        -   Edit fields and make allocation changes for single or multiple spaces using an interactive floor map. Witness real-time updates for seamless and efficient space management.
    -   Changed:
        -   The "View-By" selection for building view has been relocated within the stack plan Settings.
        -   Improvements have been made with respect to the management of app dependencies, resulting in improved overall functionality and compatibility between applications.
    -   Fixed:
        -   Previously, the "Go to stack plan" link in the floor plan tab with an empty state was not functioning correctly, failing to navigate to the stack plan. This issue has been resolved.
        -   The links to the scenario plan in the Related scenario plan tab were not working as intended in the past. This issue has been fixed.
        -   Earlier, making changes to the "View-By" option resulted in multiple map loads with incorrect view-by modes. This issue has been resolved.
        -   Earlier, modifying space allocation resulted in inconsistent color code updates in the scenario plan. This issue has been fixed.
        -   Previously, after making user assignment or assignment type changes to spaces in the scenario plan, the space icons were not loading immediately. This issue has been resolved.
        -   General accessibility improvements have been made in scenario planning feature. Screen readers, tooltips, headings, labels, and more are now supported.
-   **Version 1.3.0 - May 2023**

    New: A new module 'Dashboards' is added to the left-hand side. Using this module, a workplace manager can view all the 3 new dashboards related to Space Optimization, Maintenance, and Lease Administration.

-   **Version 1.2.3 - March 2023**

    Fixed: Issues switching between 'Edit scenario' and 'View scenario' modes.

-   **Version 1.2.1 - February 2023**
    -   New
        -   Create open and restricted neighborhoods and assign employees to them. Visualize spaces using the stack plan or floor map and manage space assignments through the floor map.
        -   A workplace lease administration application to track all workplace lease contracts AND assets, services, locations that are part of the contract.
        -   Create preventive maintenance plans for enterprise assets and workplace locations. The latter can be used to do maintenance planning for soft services like house-keeping.
        -   View preventive maintenance cases, as an outcome of preventive maintenance planning, in the overview tab. The overview tab is a focus area for maintenance planners and maximize the information in one viewport.
        -   Assess preventive v/s corrective maintenance cases for the current month in the personalized landing page for maintenance planners.
-   **Version 1.1.0 - December 2022**

    Changed: A Stack plan saving process will now be performed asynchronously. You can track the same via a new progress bar.

-   **Version 1.0.3 - November 2022**

    Workplace Central provides a unified experience for workplace managers and other key personas such as space planners and maintenance managers to strategize, plan, optimize and maintain the workplaces more efficiently.


**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)

