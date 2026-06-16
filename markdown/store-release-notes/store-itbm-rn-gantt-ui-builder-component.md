---
title: Gantt UI Builder Component release notes
description: Version history for the on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-gantt-ui-builder-component.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Gantt UI Builder Component release notes

Version history for the on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 26.1.1 - June 2026 \(Yokohama, Zurich, Australia\)**
    -   Fixed:
        -   Resolved an issue where focus moved unexpectedly to the first table's column headers when using the resizable panes divider handle.
        -   Resolved an issue where rollup bars did not accurately reflect the span of actual dates in a multi-level hierarchy.
        -   Resolved an issue where the timeline bar did not display the label name when the Show Label check box was selected.
-   **Version 26.1.0 - April 2026**
    -   Changed: Redesigned the timeline configuration panel with clearly defined sections, making it easier for users to customize the timeline’s appearance and behavior during runtime.
    -   Fixed: Introduced a horizontal scroll bar in the Capacity tab to improve navigation and accessibility.
-   **Version 26.0.4 - March 2026**

    Fixed: Improved the white space between the grid and side panel for smaller data sets and added the expand/collapse all configuration as a prop in UIB.

-   **Version 26.0.0 - December 2025**
    -   New: Introduced Compact Mode in Gantt for improved data density and usability.
    -   Fixed:
        -   Resolved timeline hang issue when dragging bars in hierarchical view.
        -   Addressed accessibility \(A11y\) issues for zoom in/out controls and legend elements. Fixed i18n date format issue in Project Workspace.
-   **Version 25.1.0 - August 2025**
    -   Fixed:
        -   Separating resizer from the task bar.
        -   Gantt timeline rendering when date is passed in different formats.
        -   Considering baselines for timeline data.
        -   Expose precision for timeline data.
-   **Version 24.4.0 - February 2025**
    -   Fixed:
        -   Project Workspace - Issues with switching between the Grid and Gantt view have been fixed
        -   Fixed the lagging experience in scrolling between the column header and the cells
-   **Version 24.3.1 - November 2024**
    -   New features:
        -   Grid Header Updates: Updated the bottom tree for the rendered grid header.
        -   Improvement to the expand all events for grid expansions separately.
        -   Improved rendering performance and interactive features for Gantt chart elements.
    -   Bug fixes:
        -   Fix to the rendering of the CP grid bottom tray
        -   Addition of informative labels to Slide buttons and Shift column buttons
        -   Currency Editing: Fix to the discrepancies when editing currency values
        -   Multi-select Issues: Inline edit problems when non-editable cell value could be updated are addressed
        -   Fix for issues related to sorting columns
        -   Fix for editing issues in specific column types
        -   Checkbox Accessibility: Improvement to the labels for checkboxes and column menu buttons
        -   Cell Editing: Correction to focus navigation and editing behavior. UI Flickering: Resolved flickering of percent complete during scrolling
        -   Grid Alignment: Adjustments to the alignment of choice fields as number type
        -   Read-only Cells: Improvements to visual representation for read-only cells
        -   Gantt Task Dependencies: Fix to the issues with displaying and editing task dependencies
        -   Component Actions: Fix to the bugs related to component actions
-   **Version 24.2.0 - August 2024**
    -   New:
        -   Multiple icons in the timeline bar of the Gantt
        -   Column virtualization on the capacity planning console
    -   Fixed:
        -   Row editing - rendering on other dit value update on row editing
        -   Drag &amp; Drop - Updated the tooltip info to "Rearrange row"
        -   Cell Focus and Actions Cell focus is now shifted to the other cell when clicking on the comment icon of the other cell. Cell actions are now aligned for the Reference/api\_reference column type
        -   Section resizer is now focusable using a keyboard
        -   SECTION\_RESIZED event is exposed to UIB
        -   Accessibility
            -   Fixed toggle flicker issue when a user scrolls.
            -   Hiding a column from the column context menu in the grid is not saving in the user preference table
            -   Included RTL padding
            -   Added icon start, end, variant, and tooltip properties to clickable column types
            -   Passing the first and last task for sub-columns
            -   While having an avatar\_group\_select field open, if we open the side panel, it appears on top of the side panel
            -   When the scroll is present for columns, pressing the tab from the last column does not shift focus from it
-   **Version 24.1.0 - May 2024**
    -   Fixed:
        -   Addressed an issue where the Mac reader failed to read out relevant information upon focusing a timeline bar.
        -   Resolved an issue where task bars were erroneously moving and resizing despite the disable Editing setting being enabled.
    -   New:
        -   Updated filter comparison operators for improved functionality.
        -   Added options to adjust the width of the side panel.
        -   Introduced a new column type for tags in the Gantt Chart.
-   **Version 24.0.0 - February 2024**

    New Features:

    -   New:
        -   Invisible Accessibility Control Support for Gantt Chart: Implemented support for invisible accessibility controls specifically tailored for Gantt Chart interactions, enhancing usability for diverse user needs.
        -   Truncation Accessibility Support for Gantt Chart: Introduced truncation accessibility support for the Gantt Chart, ensuring a seamless and inclusive experience for users in varied scenarios.
        -   Popover Support for Timeline Phases and Icons on Gantt Chart: Changed the Gantt Chart timeline by incorporating popover support, providing additional context and information for timeline phases and icons.
        -   Multiple Bars for Single Row on Gantt Chart Timeline: Empowered users with the ability to display multiple bars for a single row on the Gantt Chart timeline, offering a more comprehensive representation of project timelines.
        -   Manage Side Panel Using Props: Added functionality to manage the side panel using props, offering users greater control and customization options.
    -   Fixes:
        -   Title of the Timeline Bar Tooltip Length Issue: Addressed the problem where the title of the timeline bar tooltip extended beyond its container when excessively lengthy.
        -   Grid Content Visibility on Timeline at 15% Grid Width: Fixed the issue where grid content was visible on the Gantt Chart timeline when the grid width was set to 15%, ensuring a cleaner and more polished presentation.
        -   Event Dispatch on Side Panel Opening: Implemented the dispatch of an event when the side panel is opened, facilitating improved integration and responsiveness.
        -   Bar Labels Toggle Behavior: Resolved the issue where the bar labels toggle was resetting when switching to the grid layout under the side panel, ensuring consistent user preferences.
        -   Empty State Message in Capacity View: Added an empty state message to the capacity view, providing users with clear feedback in scenarios where no data is present.
        -   Styling Changes:
            -   Corrected flat border styles in the capacity view for a more polished and cohesive visual presentation.
            -   Optimized hover styles by moving them to the bottom, preventing unintended style overriding and improving the overall user experience.
        -   Attribute Unselection Issue in Group Resource By: Resolved the problem where unselecting an attribute in the group resource by section while selecting planning items resulted in displaying all planning items instead of the selected ones.
-   **Version 23.0.1 - January 2024**

    Fixed: Read only cell have grey background now.

-   **Version 23.0.0 - November 2023**
    -   New:
        -   Forced color: Apply forced colors to Gantt charts for accessible Gantt Chart.
        -   Timeline Bar Color Split: Introduced support for using multiple colors to update the visual differentiation of timeline bars.
        -   Rating Column: Added a new column type to capture and display ratings.
        -   Extended Column Header Information: Allows to provide additional information for column headers.
        -   Streamlined Column Management: Added options to simplify the process of adding new columns.
        -   Expanded Column Context Menu: Provides more options to add context menu items for columns.
        -   Text Wrapping: Update readability by wrapping text into multiple lines.
        -   Column Header Indicators: Added indicators to provide additional functionality to column headers.
        -   Section Resizer: Adjust section sizes easily for a more organized workspace.
        -   Row Editing Support: Allows to edit rows within your tables.
        -   Updated Color Palette: Added more color options for cells and headers to improve interactivity.
    -   Fixed:
        -   Side Panel Checkbox Toggle: Fixed an issue where the checkbox toggle event was not functioning properly with additional options in the side panel.
        -   Row Selection Checkbox: Resolved an issue where row selection checkboxes could be toggled using the spacebar.
        -   Advanced Criteria Support: Criteria now include 'ISEMPTY' and 'ISNOTEMPTY' for more extensive customization.
        -   Universal Comment Icon: Comment icons now work seamlessly with every type of column.
        -   Individual Currency Codes: You can now assign individual currency codes to financial records.
        -   Manual Date Editing: In certain cases, you can manually edit dates for added flexibility.
        -   Total Row Count Accuracy: Corrected an issue where the total row count displayed inaccurate numbers when non-selectable rows were present.
        -   Context Menu Fix: The 'Edit Row' context menu option is now functioning correctly.
-   **Version - August 2023**
    -   on on Grid columns
    -   Cell-level colouring for background and text
    -   Support for column-level personalization hidden mode
    -   Support for Capacity Planning view
    -   Changed:
        -   The side panel will not block the Gantt body and push to remaining space
        -   Side Panel slots have been spilt into Header and Content for an optimal experience
    -   Fixed:
        -   Outside click will raise the save event
        -   The editor will select, clicking the appropriate part while the edit start
        -   Date can be manually edited
        -   The date sorting issue fixed
        -   The number filter will be fault tolerant for the string value
        -   NaN was coming for aggregated value
        -   The Avatar group was not editable
        -   The side panel can be navigated using a keyboard
        -   Some AXE accessibility has been fixed
    -   Removed: Some unused events have been removed
-   **Version 22.0.0 - May 2023**
    -   New:
        -   Gantt chart availability on UIB
        -   Custom calendar support
        -   Records filter on load for Gantt chart
        -   Manage column personalisation props
        -   Show dependency line property
        -   Multi Currency column inline editing
        -   Avatar select column inline editing
        -   Dynamic query parameter for Avatar select columns
        -   Ability to add background color for column header
    -   Changed:
        -   Configuration type changed to Basic, Standard, Advanced on UIB
        -   Removed the gap between the timeline zoom selector and the side panel
        -   Gantt chart timeline bar popover placement is not restricted to the timeline section
        -   Gantt chart header color change \(now support theme\)
    -   Fixed:
        -   Theme issue on input fields on column filter
        -   Accessibility issue in cell click and enter
        -   Positioning shadow of the right-side panel
        -   Localization support for currency

**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

