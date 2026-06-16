---
title: Checklist Component release notes
description: Version history for the Checklist Component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-checklist-component.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Checklist Component release notes

Version history for the Checklist Component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 26.0.2 - March 2026**

    Fixed an issue where custom properties in checklist item objects were not returned in event payload

-   **Version 26.0.0 - December 2025**
    -   This release introduces a major upgrade to the Checklist component, focusing on usability, flexibility, accessibility, and configurability. The update includes a redesigned UI, new interaction patterns, improved editing capabilities, link support enhancements, and expanded configuration options through UIB:
        -   New Features:
            -   1.1 Empty State
                -   Brand-new empty state UI for checklists with:
                    -   Title and description support. Entry point for adding the first checklist item. Three-dot action menu with Delete All functionality
            -   1.2 Three-Dot Menu
                -   Added contextual menu for global checklist actions. Options included:
                    -   Delete all items
            -   1.3 Inline Editing
                -   Users can edit checklist items directly inline via:
                    -   Hover → Click edit icon Double-click on item text
                    -   Required-field option adds an asterisk when enabled. Changes applied on Apply; discarded on Cancel.
            -   1.4 Text Wrapping
                -   Longer checklist items wrap automatically based on container width. Ensures full readability without truncation.
            -   1.5 Inline Link Controls
                -   Checklist items now support embedded links \(configurable; enabled by default\). On hover, users can:
                -   Edit link Delete link
                -   "Add Link" button leads directly to inline edit mode with link text.
            -   1.6 Item Reordering
                -   Checklist items support drag-and-drop reordering. Feature is configurable. Sequence prefix updates dynamically after reordering.
            -   1.7 Sequence Prefix
                -   Users can enable numeric or alphabetic prefixes on list items. Automatically maintains correct order after reordering.
            -   1.8 Checklist Description
                -   Component now supports an optional description field above the checklist.
        -   2. UI &amp; Interaction Enhancements
            -   2.1 Hover Controls
                -   Edit and Delete icons appear on hover. If “Invisible Controls” preference is enabled:
                    -   Icons remain permanently visible for ease of use.
            -   2.2 Updated Visual Styling
                -   Refreshed UI for empty and populated checklists for improved clarity and consistency.
            -   2.3 Edit Mode Behaviour
                -   Disabled, read-only, and invalid fields display as-is while editing. All configuration states continue to be respected.
        -   3. Keyboard Accessibility Updates
            -   3.1 Drag Handle Focus
                -   Focus on drag-and-drop handle reveals Edit/Delete icons. Users can navigate to icons and perform actions using Enter.
            -   3.2 Keyboard Editing Support
                -   Enter or Tab + Enter triggers inline editing mode. Fully accessible interaction flow for keyboard-only users.
        -   4. New UIB Elements &amp; Configuration Options
            -   4.1 Component Visibility
                -   Checklist component visibility can be toggled through UIB.
            -   4.2 Checklist Configuration Options
                -   Empty state configuration:
                    -   Empty state title Empty state description
                -   Font size customization for checklist items. Prefix configuration:
                    -   Number Alphabet
                -   Loading spinner toggle during checklist render. Configure checklist item objects:
                    -   State, labels, validations, etc.
            -   4.3 Edit Mode Configuration
                -   Allow or restrict user editing of checklist items. Configure available edit options \(required flag, delete, etc.\). Disable link embedding if needed. Option to open item links in a new browser tab/window.
    -   Summary of Improvements This release modernizes the Checklist component with:
        -   A cleaner, more intuitive UI Powerful inline editing Enhanced link management Better accessibility &amp; keyboard usage Comprehensive configurability via UIB Flexible visuals, ordering, and metadata
    -   These changes provide a more robust, customizable, and user-friendly checklist experience for all users.
-   **Version 24.2.2 - March 2025**

    Improved the edit mode experience to show or hide checklist item configurations.

-   **Version 24.2.1 - February 2025**

    Fixed issues with reordered checklist items. UI Builder panel configurations and the hasLink property.

-   **Version 24.1.2 - September 2024**

    \* Fixed issue with empty payload in event.

-   **Version 24.1.1 - August 2024**
    -   Introduction of property which indicates a checklist item as mandatory
    -   Admin can configure which individual option/item in the checklist is mandatory.
        -   Benefits:
            -   This will prevent users from making incomplete or incorrect form submissions.
            -   This will prevent users from having to navigate once more through a page/form in order to fix submission errors.
    -   It should be a part of screen reader and the ARIA label to be used is "Required"
    -   What is used for indication:
        -   The asterisk symbol at the end of the checklist
        -   It should be a part of screen reader and the ARIA label to be used is "Required"
        -   Existing way of showing asterisk is used \(as used in checkbox\)
    -   The word "required" is part of the label associated with the form control
    -   Additional Implementation: a. Inclusion of properties like Disabled, Read only, and Invalid apart from Required.
        -   Disabled - An admin can mark a checklist item is disabled \(not to consider\) and it's shown in greyed out format. Associated link \(if any\) doesn't get disabled. This can be configured for any role by the admin and can be customised for any use case.
        -   Read Only - An admin can mark a checklist item as Read only if they want agents to just read them and not take any action on them. However, the link associated with it \(if any\) can be clicked and read. This can be configured for any role by the admin and can be customised for any use case.
        -   Invalid - If an Admin wants to provide context to why a checklist item is invalid, they can mark a checklist item as invalid along with an associated condition. It's highlighted in red if stated as invalid. Associated link \(if any\) won't get disabled.
        -   Size option - Small font option is provided as an option for the admin to configure. Link remains in the existing font style.
-   **Version 22.1.1 - May 2023**

    Fixed: Fixed checklist component to handle empty link object in the payload.


