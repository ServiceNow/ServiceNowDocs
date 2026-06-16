---
title: Common Page Templates release notes
description: Version history for the Common Page Templates application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-common-page-templates.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Common Page Templates release notes

Version history for the Common Page Templates application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.0.3 - June 2026**

    Fixed the child case creation issue in the CSM workspace \(PRB2013865\)

-   **Version 29.0.1 - March 2026**

    Changed: Standard record page template has been moved to plugin Record Page Resources \(com.sn\_record\_page\_resources\).

-   **Version 27.1.0 - August 2025**
    -   Changed:
        -   Updated hide component attribute on record page to use form preset
        -   Renamed popover element id
    -   Fixed:
        -   Record page template changes for PRB1802918: CSM Workspace: created catalog request from Case via Agent Assist does not make Case parent
        -   Various minor issues
-   **Version 27.0.0 - February 2025**
    -   Changed: Update Standard record page header from using flex layout to using grid layout
    -   Removed: Remove legacy List template and Simple List template from the template list in UI Builder
-   **Version 26.0.2 - August 2024**
    -   Changed:
        -   Record page template now uses selectedTab in url params instead of selectedTabIndex
        -   Record page template is now compatible with the latest form controller changes for multi-form:
            -   Used new component presets for related list and modal viewport
            -   Used new form controller preset
            -   Updated layout for form domain separation
    -   Fixed: Minor defects
-   **Version 25.0.4 - February 2024**
    -   New:
        -   Record preview
        -   Design changes to font and spacing
        -   Shortcuts for 'tabs' on the standard record page
    -   Fixed multiple minor issues.
-   **Version 24.0.6 - August 2023**
    -   Added Record History as a related list item on the Standard Record Page
    -   Template Added a new side bar option to open email templates on the Standard Record Page Template
    -   Various fixes to address minor issues
-   **Version 22.0.11 - March 2023**

    Fixed: Minor fix for the list page template.

-   **Version 23.0.12 - February 2023**
    -   Fixed: Various fixes to address UI issues on the template.
    -   Removed: All UI controller logic for controlling how the form behaves is removed from the template and is now part of the form component itself.

