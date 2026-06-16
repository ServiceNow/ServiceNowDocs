---
title: Platform Analytics Workspace release notes
description: Version history for the Platform Analytics Workspace on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-sn-app-analytics-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Platform Analytics Workspace release notes

Version history for the Platform Analytics Workspace on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.4.0 - June 2026**
    -   Fixed:
        -   Hide the unsupported Sort by and Group by features from legacy data visualization library page
        -   Share dialog - no results returned when user doesn't have access to roles
        -   Visualization Designer configuration panel shows incorrect error message on application scope mismatch
        -   Scrolling issue with data visualizations in edit mode
        -   Dashboard sharing UI truncates long user group names with no option to view full name in Platform Analytics
        -   Cannot edit read-only data visualization after 'Unlink from dashboard' unless entire browser page is reloaded
        -   Core UI reports do not open from Data Visualization library page when Next Experience UI is turned off
        -   Tabs gets overridden \(visually\) while switching many times before API finishes it's request
        -   List navigation arrows missing in form view when opening records from List component in Data Visualization
        -   Copy link with Filters feature broken for legacy filters
        -   Distinguish widget level properties from visualization level properties for saved visualizations in config panel
        -   Single score widget is not auto-refreshed in the page
    -   Platform Analytics:
        -   Dashboard search function failing to match Keywords
        -   Guided Tour Does not populate route parameters for "default" dashboards, which breaks the functionality
        -   Drilldown View settings are missing in the dashboard visualization configuration.
        -   SVG images on dashboard are missing accessible text
-   **Version 7.4.1 - June 2026**
    -   Fixed:
        -   Platform Analytics
            -   When using a date/time filter, the "Today" predefined range incorrectly starts from the current hour instead of all of today.
            -   Visualization Designer configuration panel shows incorrect error message on application scope mismatch
            -   Scrolling issue with data visualizations in edit mode
            -   Dashboard sharing UI truncates long user group names with no option to view full name in Platform Analytics
            -   Cannot edit read-only data visualization after 'Unlink from dashboard' unless entire browser page is reloaded
            -   Core UI reports do not open from Data Visualization library page when Next Experience UI is turned off
            -   List navigation arrows missing in form view when opening records from List component in Data Visualization
            -   Copy link with Filters feature broken for legacy filters- Distinguish widget level properties from visualization level properties for saved visualizations in config panel
            -   Single score widget is not auto-refreshed in the page
            -   Guided Tour Does not populate route parameters for "default" dashboards, which breaks the functionality
            -   Visualizations do not load while switching tabs in browser zoom mode
        -   Service Operations Workspace: Dashboard does not load, upon re-selecting the same dashboard again
-   **Version 8.3.1 - May 2026**
    -   New: Allow to add the Now Assist Context Menu in the Platform Analytics dashboard to generate summaries and insights based on AI available skills
    -   Fixed:
        -   History entry and title are generated with an incorrect description when accessing dashboards
        -   Dashboard Statistics table contains negative data incorrectly
        -   Save button is enabled when new properties are added to component
        -   List parameters to be passed when drilling down on dashboards and visualization designer
        -   If v\_table property is not on then list will not show CoreUI reports but cards have the count
        -   Visualization Configuration: Data sources empty message is not translated
        -   "You have unsaved changes in Workspaces" indicator dot appears when opening a data visualization
        -   Hide inactive Core UI scheduled exports from the scheduled export library page
        -   "Not used in any dashboard" shows incorrect results
-   **Version 7.4.0 - May 2026**
    -   Fixed:
        -   Dashboard Statistic table shows negative data incorrectly
        -   History entry and title are generated with an incorrect description when accessing dashboards
        -   List params need to be passed when list is drilled down on dashboards and visualization designer
        -   Hovering issue in Subject Field while creating Scheduled Email in Platform Analytics
        -   Date filtering does not work for 'ON' operator in Date fields on the List visualizations of Platform Analytics
        -   Visualization Configuration: Data sources empty message is not translated
        -   Hide inactive classic scheduled exports from the scheduled export library page
        -   Collapse icon on top layout should be visible when there are no widgets on top layout
        -   "You have unsaved changes in Workspaces" indicator dot appears when opening a data visualization
-   **Version 6.1.1 - May 2026**
    -   New: List visualization enhancements: Pagination support; consistent configuration, header, and exporting capabilities\(dependent on Yokohama Patch 13\).
    -   Fixed:
        -   Widget based settings are not working as expected with saved visualizations
        -   Only supported List export format options are available from export dropdown
-   **Version 8.1.3 - April 2026**
    -   New:
        -   Ability to specify which list view to drill down to from the Chart Interaction section of data visualizations.
        -   Ability to pass filter parameters via URL for the Platform Analytics inline dashboards
    -   Fixed:
        -   Dashboard widgets repositioned after upgrading
        -   "Schedule" option on Platform Analytics within workspaces throws "The page you are looking for could not be found" message.
        -   Widget-based settings not working as expected in saved visualizations.
-   **Version 7.2.10 - April 2026**
    -   New:
        -   Ability to specify which list view to drill down to from the Chart Interaction section of data visualizations.
        -   Ability to pass filter parameters via URL for the Platform Analytics inline dashboards \(dependent on Zurich Patch 8\).
    -   Fixed:
        -   Hide the unsupported 'Sort By' and 'Group by' features from the Data visualization library.
        -   Cmd+Click not opening CSM Dashboard widget's drill down in its own primary workspace tab.
        -   "Schedule" option on Platform Analytics within workspaces throws "The page you are looking for could not be found" message.
        -   Widget-based settings not working as expected in saved visualizations.
        -   Dashboard header is missing when migrating the dashboard through banner.
        -   Platform Analytics - Scheduled exports UI has several usability issues.
-   **Version 6.0.20 - April 2026**

    Fixed: Platform Analytics Scheduled exports library page has several usability issues

-   **Version 8.1.0 - March 2026**
    -   New: Added navigation buttons from the Dashboard, Visualization, and Filter designer pages back to the Platform Analytics libraries.
    -   Fixed:
        -   Error while updating the Scheduled export.
        -   Scheduled exports UI has several usability issues.
        -   Navigating back to dashboard after updating a record does not show the latest changes.
        -   The drill down is not working for Time series visualizations when group by is applied after migration.
        -   Dashboard export to pdf does not export pivot table.
-   **Version 7.2.4 - March 2026**
    -   Fixed:
        -   ACLs are now configured correctly for Par-scheduler and scheduler\_admin
        -   Adding a data visualization from a dashboard now assigns ownership to the logged-in user instead of the dashboard owner
        -   Updating a Scheduled Export no longer produces an error
        -   Typing the name of a new data visualization quickly no longer drops the final trailing space
        -   Drilldown in Platform Analytics library visualizations with unusually long URLs no longer returns a "414 Request-URI Too Large" error
        -   Navigating back to a dashboard after updating a record now reflects the latest changes
        -   A chart element highlighted via "Act as filter" no longer persists its selected state when editing and saving non-data properties in edit mode
        -   Drilldown on Time Series visualizations now works correctly when a group-by is applied after migration
-   **Version 6.0.19 - March 2026**
    -   Fixed:
        -   "Some of the changes you made to the widget are lost" banner no longer appears in Dashboard Edit mode
        -   Filters applied in the Data Visualization widget now carry over to the list view
        -   Clicking "View all" on a Simple List visualization now generates the correct query
        -   Drilldown in Platform Analytics library visualizations with unusually long URLs no longer returns a "414 Request-URI Too Large" error
        -   Navigating back to a dashboard after updating a record now reflects the latest changes
        -   Drilldown on Time Series visualizations now works correctly when a group-by is applied after migration
        -   Redundant properties such as 'noDebounce' and 'propLabel' are no longer added to widget props when saving a dashboard
-   **Version 7.2.3 - February 2026**
    -   Fixed:
        -   Clicking on widgets in edit mode shows a blue banner that says "You lost your changes"
        -   Platform Analytics Dashboards - Unable to Copy Dashboard Link with Filter
        -   Add to Dashboard is not enabled in a data visualization of List type if a Group By is configured
        -   Data source and filters reset when changing a data visualization to or from a List in the Visualization Designer
        -   The card "Updated in the last 30 days" in the Dashboard library page is returning incorrect records
        -   Applied Quick access filter is getting displayed as an unavailable option
-   **Version 6.0.18 - February 2026**

    Fixed: Clicking on widgets in edit mode shows a blue banner that says "You lost your changes"

-   **Version 7.2.2 - January 2026**
    -   Fixed:
        -   Dashboard view count does not increase after viewing the dashboard
        -   Default heading levels in the dashboard component often cause an illogical heading structure
        -   “Unlink from library” visualization in the dashboard still updates when the original is modified
        -   SharedContext property is being saved in the dashboard layout
        -   Platform Analytics Dashboard – Image component configuration panel is missing the upload button/flow
        -   Data visualization of type List does not show default columns in the Presentation tab
        -   Data visualization – Drill-down reports are not working
        -   Admin is no longer able to edit fields in Scheduled Email of Reports \(sysauto\_report\) in Zurich
-   **Version 7.2.0 - December 2025**
    -   New: Ability to group elements in the dashboards and define a background color and border on the component
    -   Fixed:
        -   User with viz\_admin role can't read records from par\_visualization\_configuration
        -   Unable to switch tabs on Platform Analytics dashboard after opening the Dashboard info panel
        -   Dashboard widgets move to different positions after saving the dashboard
-   **Version 7.1.3 - November 2025**
    -   Fixed:
        -   When a visualization has "Apply as Filter" selected, updating the Platform Analytics plugin version causes the filter to stop working
        -   Platform Analytics Dashboard tab gets overwritten when a tab is marked as favorite
        -   Dashboard tabs are cloning over other Dashboard tabs
        -   Navigation to UI16 record from List component includes undefined view parameter
-   **Version 6.0.16 - November 2025**

    Fixed:

    -   Confirm button "You made changes to a saved element" needs to be clicked 2 times
    -   When a visualization has "Apply as Filter" selected, updating the Platform Analytics plugin version causes the filter to stop working
    -   Platform Analytics Dashboard tab gets overwritten when a tab is marked as favorite
    -   Dashboard tabs are cloning over other Dashboard tabs
    -   Disabling chart interaction doesn't work in data visualization library
    -   Drilldown using special characters doesn't work when Next Experience UI is off
    -   Navigation to UI16 record from List component includes undefined view parameter
-   **Version 3.1.1 - July 2024**

    Fixed: Scheduled export form allows to configure only hours information in the interval dates.

-   **Version 4.2.2 - May 2024**

    New: Support passing filters information from UI Builder pages into Technical dashboards using the globalFilters property.

-   **Version 3.1.0 - March 2024**
    -   Fixed:
        -   Analytics Center - KPIs tab gives incorrect results on search
        -   Filters cannot be configured on dashboard tabs
        -   The default dashboard on the UI Builder configuration panel is not respected
-   **Version 3.0.6 - September 2023**
    -   Fixed:
        -   Saved visualization changes are not stored on the dashboard
        -   On the List component, fixed filters are not being applied
        -   Scheduling visualization export list does not show records
        -   The title is displayed on the drill down list from visualizations
-   **Version 3.0.3 - August 2023**

    Fixed: Support for cascading filters at the tab level- Scoped application notification available in the dashboard's edit mode- Scrollbars hidden when data visualizations are loading on dashboard- Translation available for Dashboard share and Add new element modals.

-   **Version 2.1.1 - March 2023**
    -   Fixed:
        -   Pagination controls for the Dashboard overview tab
        -   The top section above the tabs has a maximum height
        -   The headers and controller actions on Dashboard editing are available also when Next Experience UI is disabled.
        -   Redirection from Indicator scorecard and Simple list elements from the Dashboard
-   **Version 2.1.0 - February 2023**
    -   Fixed:
        -   Fixed the internationalization of the Analytics Center tabs
        -   Improved the redirection to Dashboards tab in Analytics Center
-   **Version 1.0.12 - September 2022**

    Fixed: Analytics Q&amp;A result page should be full page width and hide the image on Analytics Center

-   **Version 1.0.11 - August 2022**

    With the Platform Analytics Workspace, you have a central location for analytics on workspaces. Users can view all the workspace dashboards and data visualizations that they have access to. They can create new dashboards and data visualizations and delve into key performance indicators. Privileged users can make what they and others create available for others to include in their workspaces.


