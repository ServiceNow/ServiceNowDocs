---
title: Playbook Experience Components release notes
description: Version history for the Playbook Experience Components application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-playbook-exp-components.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Playbook Experience Components release notes

Version history for the Playbook Experience Components application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.3.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   The Playbook stage picker header hid stages at 400% browser zoom or 320px viewport width in the CSM/FSM workspace.
        -   A playbook activity was incorrectly marked complete when its Declarative Action UI action returned an error.
        -   Single-section playbook activity forms incorrectly displayed the section heading \(for example, "Variables"\).
        -   Work notes entered on a playbook activity form were added to the parent record's Work Notes component after Update or Mark Complete.
        -   Saving an unmodified playbook activity form left the loading indicator on screen until refresh.
        -   The Restart Stage action did not appear on a playbook stage when its display conditions were met.
        -   Playbook card status action element was keyboard-focusable without a semantic role for screen reader users.
-   **Version 28.5.1 - May 2026 \(Zurich\)**
    -   New: The Automation Test Framework \(ATF\) can now be used to test the Playbook Experience
    -   Fixed:
        -   Declarative Actions configured on workspace forms were firing twice in Zurich due to the CLIENT\_SCRIPT\_EXECUTION\_REQUESTED event propagating to the parent form. Event propagation is now stopped at the Playbook component level, ensuring each action executes exactly once.
        -   Form section headings were incorrectly displayed when a Playbook activity contained only a single form section. Section headings are now suppressed for single-section activities. For multi-section activities, the first section heading is also correctly hidden while subsequent section headings remain visible.
        -   When filling out work notes on a form, it no longer populates the work notes fields elsewhere in a configurable workspace.
-   **Version 29.2.1 - April 2026 \(Australia\)**
    -   Fixed:
        -   When triggering a record in a custom layout type, the Playbook portal erroneously displayed a messageThere are no playbooks available.
        -   HTML formatting defined via sys\_ui\_message translations \(such as custom fonts and colors\) was not applied on the initial load of a Playbook activity until the form was refreshed.
-   **Version 28.4.2 - April 2026 \(Zurich\)**
    -   Fixed:
        -   Declarative Actions configured on workspace forms were firing twice in Zurich due to the CLIENT\_SCRIPT\_EXECUTION\_REQUESTED event propagating to the parent form. Event propagation is now stopped at the Playbook component level, ensuring each action executes exactly once.
        -   HTML formatting defined via sys\_ui\_message translations \(such as custom fonts and colors\) was not applied on the initial load of a Playbook activity. Styling now renders correctly on first load without requiring a form refresh.
        -   Form section headings were incorrectly displayed when a Playbook activity contained only a single form section. Section headings are now suppressed for single-section activities. For multi-section activities, the first section heading is also correctly hidden while subsequent section headings remain visible.
-   **Version 27.3.4 - April 2026 \(Yokohama\)**

    Fixed: HTML from sys\_ui\_message renders on initial load in Playbook Cards

-   **Version 29.1.4 - March 2026 \(Australia\)**
    -   New:
        -   The Automated Test Framework \(ATF\) can now be used to test playbooks
        -   "Reorganization" and "New" fields have been added to the Playbook Custom Layout Controller:
            -   Fields in the controller and sections are ordered intuitively
            -   "Force Compact Mode" field is provided for showing compact mode regardless of screen size
            -   "Only show selected playbook field is provided to show one playbook at a time
            -   Parent record field is provided for standalone playbook vs. record-driven playbook support
            -   "Playbook to launch" field is provided for mapping to specific playbook process definitions
    -   Changed:
        -   Playbook generation features have new distinct and uplifted experience
        -   Wizard Layout enhancements have been added to provide guidance for visual progress, reflow, and actions
    -   Fixed: Keyboard navigation improvements have been made
-   **Version 28.4.1 - March 2026 \(Zurich\)**
    -   Agent as Activity: This enables executing any custom agent inside playbook.
    -   Generative AI: AI visual uplift for Playbook Generation and Agentic Playbooks.
    -   UX Enhancements: Continued modernization of the Agentic Playbooks experience.
-   **Version 28.3.3 - February 2026 \(Zurich\)**

    New: Added more robust analytics tracking

-   **Version 27.3.3 - February 2026 \(Yokohama\)**
    -   Fixed:
        -   Playbook not moving forward in some cases after the record generator is triggered
        -   When Expand first prioritized card is set to false, focused mode playbooks now show activity content
    -   Changed: Added more robust analytics tracking
-   **Version 26.4.1 - February 2026 \(Xanadu\)**
    -   Fixed: When Expand first prioritized card is set to false, focused mode playbooks now show activity content
    -   Changed: Added more robust analytics tracking
-   **Version 28.3.2 - January 2026 \(Zurich\)**

    Fixed: When the playbook experience configuration property of "Expand first prioritized card" is set to false, and we change the card view to "Focused", the elements weren't rendering correctly on cards.

-   **Version 28.3.1 - December 2025 \(Zurich\)**

    New: Enable AI agents to complete activities without human intervention during runtime.

-   **Version 28.2.3 - October 2025**
    -   Fixed: Updated styling and icons for playbook activities that are assisted by AI Agents
-   **Version 27.3.2 - October 2025**

    Fixed: Corrected playbook record generator behavior to show a form on load when glide.sys.domain.use\_domain\_determining\_field is enabled and default domain is sys\_domain.

-   **Version 26.3.8 - October 2025**

    Changed: Updated ACL record to only be editable by maint users.

-   **Version 28.2.1 - September 2025 \(Zurich\)**

    New: Combine the power of AI agents with pre-defined, customizable playbooks, organizations can streamline processes, reduce manual effort, and achieve higher levels of efficiency. Enable form-based activities to be pre-filled by AI Agents, accelerating manual human work. Humans in the loop will review and modify or accept AI Agent suggested form values before marking activities as complete. Human agents can also view the AI Agents' reasoning and progress via the Now Assist panel.

-   **Version 28.1.1 - August 2025 \(Zurich\)**
    -   New:
        -   Enhanced UI components of the Activity Viewer, Stage and Activity Picker, Horizontal Stage Picker, and Compact Mode
        -   Added the ability to select activities from the Horizontal Stage Picker
        -   Added Back declarative action
    -   Fixed:
        -   Stopped showing placeholder activities in the Optional Activity modal
        -   Updated the Open record declarative action behavior in the playbook incident form field for Service Portal and Workspaces
        -   Updated the Open list declarative action on the Show list of records activity to redirect and open list
        -   Updated the Resolve declarative action on Incident Resolution to move the activity to a Complete state
        -   Corrected the User form activity using the new form controller to update the associated record properly
        -   Stopped User form fields from overflowing and showing outside of a playbook card
        -   Enhanced accessibility features for Keyboard focus, selected state and contrast in Coral default/dark theming
        -   Corrected the Activity Picker dropdown dismissing on the selected activity
        -   Restricted Keyboard actions on pending stages
    -   Changed:
        -   Updated the Restart button in the restart warning modal from primary-negative color to primary-positive color
        -   Renamed all platform level out of the box activities to match new naming convention
-   **Version 27.3.1 - August 2025 \(Yokohama\)**

    Changed: Updated to show declarative actions in archived playbooksFixed: Corrected the Open List declarative action to work with the Service Operations Workspace

-   **Version 27.2.4 - June 2025 \(Yokohama\)**
    -   Fixed:
        -   Corrected overflowing text in running playbooks
        -   Updated archived playbooks to show declarative actions
-   **Version 26.3.6 - June 2025 \(Xanadu\)**
    -   Fixed:
        -   Corrected overflowing text in running playbooks
        -   Updated archived playbooks to show declarative actions
-   **Version 27.2.2 - May 2025 \(Yokohama\)**
    -   Fixed:
        -   Corrected to allow delegated developers and admins to test playbooks
        -   Corrected playbook performance in the portal when dynamic height is set to true
        -   Stopped cutting off playbook activity border for longer height activities
        -   Corrected playbook to remain visible when selecting optional activities
-   **Version 26.3.4 - May 2025 \(Xanadu\)**
    -   Fixed:
        -   Corrected to allow delegated developers and admins to test playbooks
        -   Corrected playbook performance in the portal when dynamic height is set to true
-   **Version 27.1.8 - April 2025**
    -   Fixed:
        -   Corrected scroll bar for Service Portal playbooks that use the Focused Layout
        -   Corrected the link for Preview in Playbook
        -   Stopped showing an empty UI Builder page when opening the Edit Default UI in UI Builder link
-   **Version 26.2.9 - April 2025**
    -   Fixed:
        -   Corrected scroll bar for Service Portal playbooks that use the Focused Layout
        -   Corrected the link for Preview in Playbook
        -   Stopped showing an empty UI Builder page when opening the Edit Default UI in UI Builder link
-   **Version 27.1.5 - March 2025 \(Yokohama\)**
    -   Fixed:
        -   Corrected to show all activities after previous ones are completed in HR Playbooks
        -   Corrected to allow delegated developers and admins to test playbooks
        -   Made playbook content visible in the background when opening a record from a list activity
        -   Removed title page tooltip from Playbooks in Portal
        -   Made playbook content visible again in Optional Activities mode
-   **Version 25.2.4 - March 2025 \(Washington DC\)**
    -   Fixed:
        -   Corrected to show all activities after previous ones are completed in HR Playbooks
        -   Corrected to allow delegated developers and admins to test playbooks
-   **Version 27.1.3 - February 2025 \(Yokohama\)**

    New: All playbook activities that use a presentational list now ship with an out-of-the-box preset and component bundle for the now-presentational-list component.

-   **Version 26.3.2 - February 2025 \(Xanadu\)**
    -   Changed:
        -   Enhanced the portal page refresh behavior to handle the following use cases:
            -   Without Full Page Refresh: When a user initiates a Record Generator playbook, the portal page URL updates to reflect the table and sysId of the created record without performing a full page refresh.
            -   With Full Page Refresh: If the "Full Page Refresh after Record Generator" widget option is enabled, the URL updates with the table and sysId, followed by a full page refresh \(current behavior\).
            -   Preserving Query Parameters: In both scenarios, only the table and sysId are updated in the URL, while all other query parameters remain unchanged.
-   **Version 26.2.6 - January 2025 \(Xanadu\)**

    Fixed: Corrected to display the accurate order of activity executions.

-   **Version 26.2.3 - November 2024 \(Xanadu\)**
    -   New: Added a Guided view mode to the Playbook Activity Viewer
    -   Changed:
        -   Updated the Table field in Playbook Content Item to take up to 80 characters
        -   Stopped showing inactive activities in the Activity Definition picker in activity overrides
    -   Fixed:
        -   Stopped the Playbook Form Validation from firing multiple times
        -   Corrected access for the "Preview in Playbook" UI Action
        -   Corrected auto-refresh behavior for lists in the mobile playbook environment
        -   Corrected tooltip in playbook heading to only show once
        -   Stopped showing activities as Pending when they should be In Progress in HR Playbook
        -   Set stepper playbook preset to "sm"
        -   Stopped showing conditional lanes when run conditions are not met
        -   Corrected population of the declarative action model field 'is\_last\_in\_playbook'
-   **Version 26.1.2 - September 2024 \(Xanadu\)**
    -   Fixed:
        -   Corrected tooltip to only show once when playbook title is truncated
        -   Updated lists to auto-refresh when using mobile playbook
        -   Updated stages with unmet run conditions to hide
        -   Updated stages to stop incorrectly showing "Pending" state instead of "In Progress" HR Playbooks
        -   Corrected the value for the stepper preset size
        -   Updated activities in focus view to render even when screen height is shorter than the activity
-   **Version 25.2.3 - September 2024 \(Washington DC\)**
    -   Fixed:
        -   Corrected tooltip to only show once when playbook title is truncated
        -   Updated stages with unmet run conditions to hide
        -   Updated stages to stop incorrectly showing "Pending" state instead of "In Progress" HR Playbooks
        -   Updated playbook form to save data when the field is of type "checkbox"
        -   Corrected declarative actions to show in activities when the associated record is changed
-   **Version 26.1.1 - August 2024 \(Xanadu\)**
    -   New:
        -   Added a "Starting" indicator to the first activity in a playbook to prevent a process of sequential activities from being blocked.
        -   Added UIB Presets for the now-stepper when using the Playbook Custom Layout Controller.
        -   Added a "Hide Back to Playbook" toggle to turn on/off the "Back to Playbook" button in compact mode in the Playbook Connected and Playbook Activity Viewer.
        -   Improved Accessibility and WCAG Compliance.
        -   Updated Playbook Activity UIs to be compatible with the Form Controller in UI Builder.
    -   Changed:
        -   Changed the option in the declarative action assignment page to "Overflow menu" instead of "Header Dropdown".
        -   Moved the declarative actions overflow menu to the bottom right of the Playbook Card.
    -   Fixed:
        -   Corrected Activity Override's activity definition reference picker to only show the active activity definitions.
        -   Updated Playbook Cards to load the list and checklist components when expanded.
-   **Version 24.2.5 - June 2024 \(Vancouver\)**

    Fixed: Updated stages to show correct state.

-   **Version 25.2.1 - May 2024 \(Washington DC\)**
    -   New:
        -   Added bundled components for the Focused Vertical, Focused Horizontal, Stacked Vertical, and Stacked Horizontal custom layouts so that you can add layouts to new or existing pages.
        -   Added the record generator function to Custom Layouts so that you can directly configure a record generator for your playbook in UI Builder.
    -   Fixed: Modals no longer result in blank pages when creating records through them.
-   **Version 25.1.5 - April 2024 \(Washington DC\)**
    -   Fixed:
        -   Corrected to open the first activity that is in progress when you select a stage.
        -   Corrected optional activities to be placed correctly when added through a scripted API.
        -   CorrectedDownloadandDelete file attachmentdeclarative actions to work in Portal playbooks.
-   **Version 24.2.4 - March 2024**
    -   Fixed:
        -   When an open activity's associated record changes to show a declarative action, agents no longer have to refresh the page in order to see the declarative action on the open activity.
        -   When selecting one declarative action on an activity shows another declarative action, agents no longer have to refresh the page in order to see the new declarative action.
-   **Version 25.1.4 - February 2024**
    -   New:
        -   Added the function to restart a playbook from the beginning, from certain stages, or from certain activities if restart is enabled and defined in the Workflow Studio process design environment.
        -   Added to support using playbooks in Portal:
            -   Dynamic Catalog Content Type when creating a catalog item
            -   A Scripted Extension Point
            -   A Portal page
            -   A Portal widget
            -   A UIB page
        -   Added Next Activity and Previous Activity client actions for the focused activity viewer and for layouts using focused activity viewer.
        -   Apply reflow to out-of-the-box standalone and custom layout playbook components so that the UI adjusts when you resize your window or zoom.
        -   Added form sections to playbook forms.
        -   Added the following mobile playbooks events:
            -   Scan Barcode allows users to scan barcodes.
            -   Open Launcher Screen allows users to open launcher screens.
            -   Initial Load Started and Initial Load Completed streamlines the display of loaders between the native mobile and playbook web-based loaders.
            -   Playbook AMB update received lets the mobile controller know when an activities record has changed.
    -   Fixed: Key performance, accessibility, and user experience improvements, such as showing playbook forms in activity UIs.
-   **Version 24.2.3 - January 2024 \(Vancouver\)**
    -   New:
        -   Added the function to restart a playbook from the beginning, from certain stages, or from certain activities if restart is enabled and defined in theWorkflow Studioprocess design environment.
        -   Added to support using playbooks inPortal:
            -   Dynamic Catalog Content Typewhen creating a catalog item
            -   AScripted Extension Point
            -   APortalpage
            -   APortalwidget
            -   AUIBpage
        -   AddedNext ActivityandPrevious Activityclient actions for the focused activity viewer and for layouts using focused activity viewer.
        -   The UI adjusts when you resize your window or zoom for out-of-the-box monolith and custom layout playbook components.
        -   Added form sections to playbook forms.
        -   Added the following mobile playbooks events:
            -   Scan Barcodeallows users to scan barcodes.
            -   Open Launcher Screenallows users to open launcher screens.
            -   Initial Load Started and Initial Load Completedstreamlines the display of loaders between the native mobile and playbook web-based loaders.
            -   Playbook AMB update receivedlets the mobile controller know when an activities record has changed.
    -   Fixed: Key performance, accessibility, and user experience improvements, such as showing playbook forms in activity UIs.
-   **Version 24.2.2 - December 2023 \(Vancouver\)**

    Fixed: You no longer receive the "needs previous activity to finish before proceeding" error when using new record generators, custom activity UIs, or show list of records.

-   **Version 24.2.1 - November 2023**
    -   Changed:
        -   Improved readability of the vertical stage and activity pickers with new progress indicators, status icons, priority icons and more.
        -   Updated forms for completed activities to display as forms instead of key-value pairs.
    -   Fixed: Corrected color contrast of adding optional activities to meet accessibility standards.
-   **Version 24.1.3 - September 2023 \(Vancouver\)**
    -   Fixed:
        -   Updated permissions so that pd\_admin role users without write access to a triggercan still cancel a record.
        -   Corrected UIB page for Activity UIs so that the entire Activity UI displays.
-   **Version 24.1.2 - August 2023 \(Vancouver\)**
    -   Changed:
        -   Added support for more mobile API features like the perform function
        -   Added the playbook title to the mobile page
        -   Added a Leave playbook button that you can add to the last activity
    -   Fixed:
        -   Updated to show only the correct tooltip when hovering on an activity
        -   Corrected filter appearance
-   **Version 23.1.5 - July 2023**

    Fixed: Selected activity is no longer skipped over when moving to a stage with activities that are scheduled to start 'With previous' \[activities in the stage\].

-   **Version 23.1.4 - April 2023**
    -   Fixed:
        -   Playbook Custom Layouts:
            -   Corrected the button label from 'Show stages flag' to 'Show stages' in the Activity Picker.
            -   Updated the 'Create Task' declarative action in the new CSM playbook layout to carry over the account, contact, and consumer from parent case to new task.
            -   Updated the Horizontal Stage Picker to hide stage when all activities are hidden.
            -   Updated the Horizontal Stage Pickers to respond to declarative actions.
            -   Added optional activities for the Horizontal Stage Picker configuration.
            -   Added resizable panes to all templates.
            -   Stopped looping behavior when selecting a stage in the Horizontal Stage Picker after filtering.
            -   Hid activity card progress icons temporarily.
            -   Corrected blurriness of icons for selected pending activities.
        -   Accessibility:
            -   Corrected focus issues for the Horizontal Stage Picker.
            -   Made minor visual changes.
-   **Version 23.1.3 - March 2023**
    -   Fixed:
        -   Made icons visible in the horizontal stage picker.
        -   Updated the filter to work as expected.
        -   Updated the browser's Back button response, so it takes you to previous activities, etc.
        -   Accessibility:
            -   Added an ARIA label to the input field in forms.
            -   Added alternative text to images for stage and activity elements.
-   **Version 23.1.2 - February 2023**
    -   New:
        -   Customize the layouts of your Playbook by arranging modular components.
            -   The Playbook Custom Layout UI Controller provides access to the underlying process data, so you can also create your own process-aware UI components.
            -   If you're using the provided components, Presets can automatically use data from the Playbook Custom Layout UI Controller as inputs for the components.
            -   See progress and navigate between stages in a horizontal bar instead of the standard vertical view.
            -   If you're not sure where to start, choose from 4 layout templates to try.
-   **Version 21.4.1 - November 2022 \(San Diego\)**
    -   New: The link to destination feature from UI Builder is now also available in the out-of-the-box, reusable Client Action.
    -   Fixed: Agent experience improvements.
-   **Version 22.1.2 - November 2022 \(Tokyo\)**
    -   New: The link to destination feature from UI Builder is now also available in the out-of-the-box, reusable Client Action.
    -   Fixed: Agent experience improvements.
-   **Version 22.0.4 - August 2022**
    -   New: Playbooks now auto advance to the next stage, without users having to manually navigate
    -   Fixed: Key performance and accessibility improvements, usability changes, and fixes
-   **Version 21.3.6 - August 2022 \(San Diego\)**
    -   New:
        -   Agents and fulfillers no longer need to manually navigate to the next stage of a Playbook. Auto Advance now does this for you.
        -   The Playbook form component has adopted the new client script behavior.
-   **Version 21.2.1 - May 2022 \(San Diego\)**
    -   New:
        -   The left navigational pane will be collapsed by default when an agent has one Playbook and one visible stage in Stacked view.
        -   The left navigational pane will be collapsed by default when an agent has one Playbook, one visible stage, and one activity in Focused view.
        -   A Proxied Data Broker is provided to be used when building custom Activity UIs to increase performance.
            -   Note: users should update any existing custom Activity UIs to adopt the new data broker
    -   Changed:
        -   Updated colors for Playbook theming
        -   Activities are lazy loaded in Focused view
        -   Various performance optimizations for Playbook forms
-   **Version 20.5.1 - May 2022 \(Rome\)**

    Fixed: Detached form component when activity is not visible to free up resources

-   **Version 20.4.2 - February 2022**
    -   Changed:
        -   Playbook left-hand navigational panel can now be collapsed via keyboard navigation
        -   The Create Record activity definition now supports a description property
    -   Fixed: User time zones are now honored in Playbook Forms
-   **Version 20.3.3 - October 2021**

    Changed: Submit forms before executing declarative actions \(excluding server scripts\) when the "Requires Form Fields" checkbox is selected.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

