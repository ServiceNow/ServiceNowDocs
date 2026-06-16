---
title: Platform Analytics release notes
description: Version history for the Platform Analytics application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-sn-app-analytics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Platform Analytics release notes

Version history for the Platform Analytics application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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
            -   Copy link with Filters feature broken for legacy filters
            -   Distinguish widget level properties from visualization level properties for saved visualizations in config panel
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
-   **Version 8.1.3 - April 2026**
    -   New:
        -   Ability to specify which list view to drill down to from the Chart Interaction section of data visualizations.
        -   Ability to pass filter parameters via URL for the Platform Analytics inline dashboards
    -   Fixed:
        -   Dashboard widgets repositioned after upgrading
        -   "Schedule" option on Platform Analytics within workspaces throws "The page you are looking for could not be found" message.
        -   Widget-based settings not working as expected in saved visualizations.
-   **Version 6.0.19 - March 2026**
    -   Fixed:
        -   "Some of the changes you made to the widget are lost" banner no longer appears in Dashboard Edit mode
        -   Filters applied in the Data Visualization widget now carry over to the list view
        -   Clicking "View all" on a Simple List visualization now generates the correct query
        -   Drilldown in Platform Analytics library visualizations with unusually long URLs no longer returns a "414 Request-URI Too Large" error
        -   Navigating back to a dashboard after updating a record now reflects the latest changes
        -   Drilldown on Time Series visualizations now works correctly when a group-by is applied after migration
        -   Redundant properties such as 'noDebounce' and 'propLabel' are no longer added to widget props when saving a dashboard
-   **Version 6.0.18 - February 2026**

    Fixed: Clicking on widgets in edit mode shows a blue banner that says "You lost your changes"

-   **Version 6.0.17 - January 2026**
    -   Fixed:
        -   Data Visualization drill-down reports not working
        -   Default heading levels in dashboard components often cause illogical heading structures
        -   “Unlink from library” visualizations in dashboards still update when the original is modified
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
-   **Version 6.0.15 - September 2025**
    -   Fixed:
        -   Issue with Export in Platform Analytics Dashboard
        -   Hide technical dashboards in scheduled export while selecting dashboards from the modal
        -   Platform Analytics Dashboard: The toolbar disappears when trying to edit Rich Text Component content in full screen
-   **Version 7.1.1 - August 2025**
    -   New: Enables dividers capability for the Platform Analytics dashboards
    -   Fixed:
        -   Scheduled export for Analytics list shows PPT as attachment, even though File type is selected as PDF by default
        -   Dashboard dispatches 'stats' call 2 times when dashboard has table based visualizations in it
        -   When clicking on a visualisation, the query segment needs to include also the data source filter.
        -   Disabling chart interaction doesn't work in data visualization library
-   **Version 6.0.13 - August 2025**
    -   Fixed:
        -   Filter \(filter pill\) is not re-rendered in configuration mode when user makes changes to an already saved dashboard
        -   "Go to record list" action is broken for non-admin users on data visualizations
        -   When clicking on a visualisation, the query segment needs to include also the data source filter.
        -   Tooltip button and message do not receive focus and reader cannot access information in dashboard share modal
        -   Tabs in view mode don't have "More" dropdown when there are more number of tabs which does not fit in screen
-   **Version 5.1.6 - August 2025**
    -   Fixed:
        -   Filter \(filter pill\) is not re-rendered in configuration mode when user makes changes to an already saved dashboard
        -   When clicking on a visualisation, the query segment needs to include also the data source filter.
        -   Tooltip button and message do not receive focus and reader cannot access information in dashboard share modal
-   **Version 6.0.12 - June 2025**
    -   Fixed:
        -   Printer-friendly layout changes
        -   The filters applied in the Data visualization widget does not carry over to the list view
        -   Incorrect query when clicking "View all" on Simple List visualisation
-   **Version 5.1.5 - June 2025**
    -   Fixed:
        -   Embedded PNG export does not embed the image in the correct position
        -   Unable to schedule visualization export with value of system property 'glide.sys.time\_format' as 'h:mm:ss a' \(12 hour format\)
        -   "Bad Message 414" and "Bad Message 431" when clicking into the a widget to view the results in list view
        -   Changes made to a saved Data visualization in the dashboard are not stored
        -   The filter values don't persist on dashboards after refreshing the browser page
        -   When viewing a dashboard with no indicator based widgets in Platform Analytics, the Insights button does not work
-   **Version 6.0.11 - May 2025**

    Fixed: Changes made to saved data visualizations are not persisted after saving the dashboard.

-   **Version 6.0.8 - March 2025**
    -   Fixed:
        -   Avoid null values on data visualization's title and description
        -   Duplication call on page load
        -   Dashboard metadata broker not evaluating early
-   **Version 5.1.4 - March 2025**
    -   Fixed:
        -   Duplicating a shared visualization does not allow owner to configure the visualization in the visualization designer.
        -   Data visualizations drill down to Homepage.
        -   "Follow Filter" option is not available for existing List - Simple on dashboard and drill down is broken.
        -   Date filter is not getting applied to Active VA Users widgets and User page.
-   **Version 6.0.7 - February 2025**
    -   Fixed:
        -   Duplicating the tab in a Dashboard causes 400 Bad request error
        -   Grouped filter is visible when added to the top layout
        -   Embedding PNG in scheduled exports respects the position defined in the email composer
        -   Chart interactions for Indicator scorecards are respecting the configuration
        -   Filters are working when visualized in the Dashboard printer-friendly version
        -   Export capability is not broken when recipients are separated by semicolon
-   **Version 5.1.1 - December 2024**
    -   Fixed:
        -   Data visualization library page loads without errors when switching pages
        -   Indicator scorecard supports chart interactions configuration
-   **Version 5.1.0 - November 2024**
    -   Fixed:
        -   UI Builder configuration panel loading issue
        -   Analytics Generation "Add to Dashboard" support for all charts
-   **Version 4.2.7 - October 2024**

    Fixed: Filters apply to the compatibility components in Platform Analytics Dashboards.

-   **Version 5.0.7 - September 2024**
    -   Fixed:
        -   Export of saved visualizations from Visualization library
        -   Filter values are not cleared for filters that are not in the current tab
        -   Name change of the Platform Analytics &gt; Library "KPIs" menu to "Indicators"
-   **Version 5.0.6 - August 2024**
    -   Fixed:
        -   Not able to confirm the changes on saved/non-saved visualizations on Dashboards
        -   Insight panel is not loading for data visualization that are have not triggered any insight
        -   User with par\_scheduler role cannot delete the scheduled exports
-   **Version 4.2.4 - July 2024**
    -   Fixed:
        -   Drilldown chart to chart keeps the information of the section selected by user
        -   Scheduled export supports adding multiple visualization in the same export
        -   Printer-friendly page loads correctly
        -   Menus connected to previous Platform Analytics Workspace redirects after Washington to Platform Analytics experience new navigation
-   **Version 4.2.3 - June 2024**
    -   Fixed:
        -   The visualization title when updated displays the Save button in the Visualization designer.
        -   Add saved filters and visualizations modal in the Dashboards are updated on how they retrieve the data.
-   **Version 4.1.3 - March 2024**
    -   Fixed:
        -   Allow to drill down from Calendar reports
        -   Configuration for drill-down chart to chart on Visualization designer
        -   Rich text component respects the styling selected by the users on the dashboard
-   **Version 4.1.1 - February 2024**

    With Platform Analytics, you have a central location for analytics. Users can view all the dashboards and data visualizations that they have access to. They can create new dashboards and data visualizations and delve into key performance indicators. Privileged users can make what they and others create available for others to include in their workspaces.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

