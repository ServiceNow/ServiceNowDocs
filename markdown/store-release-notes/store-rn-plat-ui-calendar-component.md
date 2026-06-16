---
title: Calendar component release notes
description: Version history for the Calendar component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-calendar-component.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Calendar component release notes

Version history for the Calendar component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.0.1 - June 2026**
    -   New:
        -   Admins can now customize the calendar event bar display and add event icons: Admins can configure which event details \(such as time, description, or label order\) appear in the event bar across all calendar views, and can display icons to convey event type, priority, or status.
        -   Users can view more event details directly in month view: In month view, clicking "more events" now reveals additional event details within the same view, improving event navigation and visibility.
    -   Changed:
        -   The calendar component now uses system design tokens for consistent styling: Most of color, shape, font, and \(where available\) spacing properties in the calendar component have been updated to use centralized system tokens, ensuring a consistent look and feel and easier theming across platforms. All header variations and the timeline view are fully tokenized.
        -   The contextual panel width is now fixed at default and extra-large screen sizes: The width of the contextual panel remains consistent at large and extra-large breakpoints, preventing layout shifts and improving accessibility. Default width at each level is customizable though contextualPanelItems property.
    -   Fixed: Fixed inconsistent date internationalization in date picker.
-   **Version 26.1.0 - May 2026**
    -   Improved agent identification using visible viewport data when scrolling stops.
    -   Added sticky section headers that remain visible while scrolling; row data updates independently until the section ends.
    -   Preserved viewport, scroll position, and visible rows across date changes and calendar refreshes.
    -   Option to scroll to a predefined section after a date change or data refresh.
    -   Option to customize the event label.
    -   Option to hide event duration in the event pill.
    -   Option to display an icon in the event pill to convey event type, priority, or status.
    -   Optimized event duration display for multi-day events.
    -   Fixed an issue where multi-day events did not render correctly in the week view.
-   **Version 26.0.2 - March 2026**
    -   Fixed an issue where drag and drop assignment was not working in the dispatcher workspace.
    -   Resolved an issue where the work week view was not rendered properly when there was a high volume of 20-minute events.
    -   Fixed an issue where the Calendar Range Updated event was being triggered twice when custom Start of Day and End of Day times were defined for the day view.
    -   Resolved an issue where the dispatcher workspace calendar view did not display correctly on initial load.
    -   Fixed a missing background colour fill on the time indicator for calendar rows.
    -   Resolved an issue where the contextual side panel in the schedule view was open by default starting on version 25.0.8.
    -   Fixed an issue where selecting a specific date did not reflect the corresponding date in the left side panel, and the selected date was not getting highlighted.
    -   Resolved an issue where the popup was getting cut off at the end of the scroll in the dispatcher workspace.
-   **Version 26.0.1 - December 2025**
    -   The Synchronized Timezone Calendar View introduces a unified, task-centric scheduling experience designed to simplify dispatch operations across multiple regions and time zones. This enhancement removes the need for manual time-zone conversions, reduces scheduling errors, and improves clarity when coordinating technicians working in different locations.
    -   1. Task-Based Timezone Alignment What’s New Calendar rows are now aligned based on the technician’s local time, rather than the dispatcher’s time zone. Impact Technicians consistently appear in the correct time slot relative to the customer’s location. Dragging a task into a 9 AM slot guarantees a 9 AM local start time, regardless of the technician’s time zone. Eliminates the need for manual cross-checking and time conversion when scheduling across multiple regions.
    -   2. Enhanced Timezone Indicators Visual Improvements
        -   Timezone indicators now display at both ends of a technician’s calendar row when working across multiple time zones. Indicators remain color-stable, consistent, and easily recognizable. When all technicians fall into the same time-zone group, the timeline displays as a single unified row without additional markers.
        -   Label Control
            -   Labels for timezone indicators remain off by default to keep the interface clean. Labels can be toggled on or off from the Calendar Header if the feature is not used.
    -   3. Advanced Timeline Settings \(UIB Configurations\) New configuration options are available in UIB under Advanced Timeline Settings:
        -   Enable or disable multiple timezone indicators Enable or disable timezone indicator labels Enable or disable the global “current time” red line for focused planning sessions
        -   These controls offer flexibility for different workflows, territories, and operational needs. 4. Automatic Timezone Indicator Refresh Auto-Refresh Behavior
        -   If the calendar remains idle for 3 minutes, timezone indicators and the entire calendar automatically refresh to remain accurate.
        -   Manual Refresh
        -   Users can still refresh manually using existing actions or the refresh button at any time.
    -   4. UIB Simplification This release improves UIB authoring by replacing JSON editing with a richer, error-resistant Collection experience—making configuration faster, clearer, and easier across supported components.
-   **Version 25.0.9 - October 2025**

    Fixed the issue where the calendar did not update based on changes in View setting's Size and Start properties after the first load.

-   **Version 23.1.0 - September 2023**
    -   Bug fixes including but not limited to:
        -   Timeline loading issues
        -   Issue with event spanning updates after changing current Mexico/BahaSur timezone
        -   Calendar events overlapping &amp; alignment issue
        -   Calendar event context menu options hide/show issue
        -   Non-blocking markspans display issue in CALENDAR view
-   **Version 23.0.5 - August 2023**
    -   New
        -   Configurable context menu
-   **Version 23.0.0 - May 2023**
    -   New:
        -   Added context menu for an empty cell.
        -   Added double click for an empty cell.
    -   Fixed:
        -   Context date calculation issue.
        -   Pop over location issue.
        -   Sticky behavior of template issue.
-   **Version 22.2.2 - May 2023**
    -   Fixed:
        -   Fixed keyboard shortcuts to switch views.
        -   Fixed popover model location issue.
-   **Version 22.2.1 - March 2023**
    -   Fixed:
        -   Fixed infinite scrolling issue in the Calendar component for the Safari browser.
        -   Fixed the popover location issue.
-   **Version 22.2.0 - February 2023**
    -   Fixed:
        -   Fixed accessibility issues \(Key board navigations\).
        -   Fixed I18n translations issues.
        -   Fixed month view more link functionalities.
        -   Added null check for viewSettings.
        -   Fixed drag event payload.
-   **Version 22.1.1 - November 2022**

    Changed: Included sentence case updates.

-   **Version 22.0.6 - September 2022**

    Fixed: Fixed the localization issue.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform UI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-ui.md)

