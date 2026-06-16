---
title: Appointment calendar component release notes
description: Version history for the Appointment calendar component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-appt-calendar-component.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Appointment calendar component release notes

Version history for the Appointment calendar component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 28.2.0 - June 2026**
    -   New:
        -   Appointment slot pills are now configurable to display start and end times: Admins can configure the appointment calendar component to show both start and end times in each slot pill and hide the duration field globally or per slot, enabling users to view full time ranges at a glance.
        -   Consistent date format support: Admins can apply a date format across all calendar views and slots ensuring consistent date formatting throughout the workflow.
    -   Fixed: Fixed the date-processing issue in Safari.
-   **Version 28.1.1 - December 2025**

    Changed: TokenizationDesign tokens have now been applied to the Appointment Calendar as part of the broader Horizon system-token initiative. For additional background, refer to the internal Horizon documentation on Tokens.

-   **Version 28.0.2 - August 2025**
    -   New Features and updates:
        1.  UI and Display Enhancements in Appointment Calendar
        2.  Slot Layout Configuration
            1.  Tablet and Mobile View: Default 3 slots per row \(configurable to 2 or 1\).
            2.  Desktop View: Default 5 slots per row \(configurable to fewer\).
        3.  Text Truncation Behavior
            1.  Truncation OFF by default in resolutions lower than 640px.
            2.  When OFF, long text wraps fully \(only applies for screen widths 640px\).
        4.  Secondary and Tertiary Info Display
            1.  Secondary Info: Now supports only one object \(instead of two\); supports optional divider in label.
            2.  Tertiary Info is now time duration: Shown only when time duration is configured via UIB \(see below\).
            3.  Secondary info wraps when truncation is off.
            4.  Overflow Behavior: Time label and event title truncate if content overflows.
            5.  Appointment Calendar Features
        5.  Week View Enhancements
            1.  Current date highlighted as a bar.
            2.  Week changes persisted only when applied from the week selector.
            3.  Cancel in week selector closes the modal without saving.
        6.  Slot State Handling
            1.  Next Available Slot is now configurable:
                -   Hidden if not configured.
                -   Label repositioned to bottom of the page.
            2.  Slot Selection Behavior:
                -   Re-selecting a selected slot unselects it.
                -   Cancel button unselects all slots or closes a modal \(if implemented\).
                -   In rescheduling, previously booked slots show with green tick mark and cascade to sticky footer in resolution lower than 344px.
        7.  Time Duration Config Options \(UIB\)
            1.  Option 1: Global Duration Header \(top-right\): With info icon: Use when all appointments have same duration.
            2.  Option 2: Per-Slot Tertiary Info:
                1.  With info icon: Use when durations differ between slots.
                2.  Recommended when durations vary.
            3.  Only one option from above can be selected at a time.
            4.  Tertiary info shown only when Option 2 is selected.
        8.  Timezone Display: Time zone always shown under Global Settings.
        9.  View Configuration
            1.  Default to Week View.
            2.  Admin can enable Day View as an additional option via config.
            3.  If only one view is configured, dropdown is hidden.
        10. More Button Behavior in collapsed state
            1.  Week View: Appears after 4 rows to open more slots.
            2.  Day View: Appears after 2 rows to open more slots.
            3.  Show less button added when all slots are expanded.
        11. Categories and Tags
            1.  Categories can be enabled through "Enable categories" property \(need to also configure "Categories" property as per user requirement\).
            2.  Functionality remains unchanged.
        12. Look and Feel Updates
            1.  UI alignment and spacing improvements.
            2.  Padding: Default 8px all around \(can be disabled by admin via config using "Bare" property\). Responsive and Mobile Behavior
        13. Responsive Reflow Support
            1.  Day View in mobile behaves as Week View.
            2.  Sticky footer always visible.
            3.  Footer contains:
                -   Schedule, Cancel, and Selected Slot Info.
                -   Selected slot for rescheduling if applicable.
            4.  At page end: Next available slot visible.
            5.  Responsive support for 320px-940px, with accordions for small screens.
            6.  Default 3 slots shown in mobile.
        14. NDS Date-Time Picker Integration
            1.  Replaces old mini calendar component.
            2.  Day View: Picker is inline.
            3.  Week View: Picker opens on range click.
            4.  Features:
                -   Highlight current date and week.
                -   Apply persists the view; Cancel reverts.
                -   Week/month navigation.
                -   Temporarily preview week on hover.
                -   Adaptive positioning for smaller screens.
                -   Technical Enhancements and Fixes
        15. Slot State Styling
            1.  Booked slot: Green with tick mark.
            2.  Rescheduling state and scheduled state clearly labeled at the bottom right.
        16. Unavailable Slot Dates Fix: Week view now correctly disables non-available dates.
        17. Height Behavior: Appointment Calendar height is set to 100% Out-Of-Box \(OOB\).
        18. Sticky Footer: Available across all views and mobile/tablet resolutions.
        19. Screen Resolution Handling:
            1.  Inherits behavior from parent container.
            2.  Switches between resolutions based on parent, not internal settings.
        20. WCAG 2.1 AA Compliant: Fully accessible for inclusive experiences.
        21. Localization Support.
        22. UIB Properties recategorized into Basic and Advanced configurations for ease of understanding.
-   **Version 24.2.5 - June 2025**

    Fixed the issue where clicking the "Next available slot" button did not redirect users to the intended time slot.

-   **Version 24.2.4 - February 2025**
    -   Fixed bugs:
        -   Fixed CSS issues
        -   Fixed accessibility issues
-   **Version 24.1.1 - November 2024**
    -   New Features:
        -   Slot Categorization:
            -   Introduced the ability to categorize appointment slots for improved organization.
            -   Admin can now assign categories such as recommended, General etc to each appointment slot.
            -   Similarly categorized slots will be grouped together.
            -   Slots left without any category will be categorised as others automatically if categorization feature is configured.
            -   OOB offering for categorisation is "Time of the day" i.e. Morning, Afternoon, Evening etc.
            -   Time duration \(example 9:00 AM-12:30PM\), can be included.
            -   Icons can be associated with the category.
            -   Reflow is supported.
        -   Contextual Tags:
            -   Introduced the ability to provide contextual tags to each appointment slot.
            -   Two primary tag support is provided.
            -   Maximum 2 primary tags can be provided.
            -   Tooltip support for primary tags in case of truncation.
            -   Primary Tags can be colour coded.
            -   Icons can be associated with the primary tags.
            -   Secondary information can be provided inside the slot.
            -   Tooltip support for secondary information inside slots in case of truncation.
            -   Reflow is supported.
        -   Calendar data picker component support for available dates:
            -   Monthly view- Demarcate the available dates with non available dates in monthly view where minimum 1 slot is available.
            -   Day view- Show available slots highlighted, unavailable slots greyed out.
            -   Toggle setting in UIB by admin in appointment calendar under view settings to switch on/off available/non available date demarcation.
                1.  See all dates disabled before current dates \(UIB Label- Disable dates before today's date\)
                2.  See all dates disabled and greyed out that are not available \(availability of minimum 1 slot per date should be there to not disable the date\) \(UIB label - Disable dates with no slots.
            -   This functionality is applicable in day mobile and day view.
        -   Provision of an option to select no. of slot pills available in a single row:
            -   By default the number of slot pills available will be 3.
            -   The number of slot pills can be configured to 1 or 2 in day mobile view.
        -   Support multiple selection in Appointment calendar:
            -   Allow selection of one or more slots across days in appointment calendar
            -   If multiple slot selection is configured, agent can select one or more slots by clicking on the slots.
            -   Deselection of selected slot will happen if the agent clicks on the selected slot again.
            -   Propose button and preview will appear in case multiple selection of slots feature is configured.
            -   Schedule/reschedule button will appear along with Propose if multiple selection of slots feature is configured and only one slot is selected.
            -   In case more than one slot is selected \(not applicable in case of a scheduled slot\), only propose button will appear.
            -   No. of slots selected slots will appear with propose button.
            -   Propose is a OOB offering and is a label that can be changed.
            -   Preview of the multiple selected slots can be seen.
            -   Multiple/all selected slots can be removed through preview.
            -   Reflow is supported.
            -   If a slot is selected in day mobile view and the selected slot \(multiple or single\) will move up to show in the showed rows. \(Showed rows are configurable\).
-   **Version 24.0.0 - August 2024**
    -   Reflow for appointment calendar:
        -   Our current workspaces are not accessible for customers with Low-Vision who demand browser zoom/Reflow support. The workspaces don't support Reflow of component when either zoomed up to 400% or webpage screen is reduced and doesn't conform to WCAG 2.1 AA Guidelines for Reflow 1.4.10.
        -   Target user personas that will benefit from accessibility:
            -   Needs more than color affordances
            -   Needs high contrast views
            -   Needs to access content with mobile devices
            -   Needs to access content with a screen reader
            -   Needs to access content with a keyboard
            -   Needs to magnify content
        -   Reflow support for appointment calendar typically refers to the ability of the appointment calendar layout to adjust dynamically based on the size of the screen or window. This is very useful on devices with varying screen sizes or orientations.
    -   Understanding Reflow Support
        -   Reflow support ensures the appointment calendar adapts seamlessly when the device is rotated, optimizing the display for both portrait and landscape orientations.
        -   -   Event Display: It can rearrange how slots are displayed, potentially collapsing or expanding event details based on available screen space.
    -   Desktop: On larger screens, an appointment calendar displays multiple slots without scrolling horizontally. Reflow support ensures that as the window size changes, the appointment calendar adjusts to maintain usability and readability.
    -   Font Size: Reflow support can adjust font sizes and spacing between elements to optimize readability without compromising the overall layout
        -   Appointment calendar after reflow implementation has accordion and the view is vertical for slots for scheduling.
-   **Version 23.0.0 - May 2023**
    -   New:
        -   Enables the user to configure the title for the events.
        -   Enables the user to configure the number of events to be shown in raw form for DAY VIEW.
    -   Fixed: Fixed the context date issue.
-   **Version 22.2.0 - February 2023**
    -   Changed: Updated the theme variables to support VA environments.
    -   Fixed: The scroll behaviour in VA
    -   New: Added logic to recalculate the date range when the timezone get changed.
-   **Version 22.1.0 - November 2022**

    New: Added support for internationalization and localization

-   **Version 22.0.3 - September 2022**

    Fixed the localization issue.


