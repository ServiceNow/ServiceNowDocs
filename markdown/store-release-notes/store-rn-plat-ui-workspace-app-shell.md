---
title: Workspace App Shell release notes
description: Version history for the Workspace App Shell application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-workspace-app-shell.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Workspace App Shell release notes

Version history for the Workspace App Shell application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.2.0 - June 2026**

    Fixed intermittent breadcrumb being displayed when hideBreadcrumb is set to true

-   **Version 28.0.10 - May 2026**

    Fixed an issue in the CSM Workspace where the agent chat box intermittently disappeared when switching between KB and interaction tabs

-   **Version 29.1.1 - March 2026**
    -   A page property was added in the Portal App Shell to make labels and alt text customizable.
    -   Utility Panel Slot Added to Breadcrumb AppShell
        -   Breadcrumb AppShell now includes a fully supported Utility Panel slot.
        -   Enables component rendering on the Interaction Record page in Manager Workspace.
    -   NVC Component Integration Support
        -   NVC subcomponents \(Interaction Controls, Lookup\) can now be loaded into Manager Workspace without custom workarounds.
        -   Standard workspace component communication is supported.
    -   UI Builder Configuration
        -   Utility Panel behavior and placement can be configured through UI Builder.
        -   Supports different layouts per record type or workspace page.
-   **Version 28.0.9 - February 2026**
    -   Fixed an issue where inbox icon in CSM/FSM Workspace keeps disappearing randomly
    -   Fixed an issue where chat panel fails to render during live interaction
-   **Version 28.0.7 - August 2025**
    -   Introduced a new Seismic component, utility panel designed to support dynamic utility panel experiences.
        -   The utility panel is rendered only when utility content is configured on the page, ensuring a clean and contextual UI.
        -   Visibility controls are available to conditionally display the panel based on page setup or user interactions on left side of the UI.
    -   This component improves layout adaptability while maintaining a streamlined interface.
-   **Version 27.0.3 - July 2025**
    -   Bug Fixes and Improvements:
        -   Breadcrumb Not Updating on Direct URL Navigation:
            -   Issue: Navigating directly to the list page via URL did not update the breadcrumb trail correctly.
            -   Fix: The breadcrumb now correctly reflects the navigation path when accessing the list page through direct URL entry.
        -   API Passive Navigation with Redirect Fails to Load: Fix: The navigation logic has been corrected to ensure that passive navigation with redirect functions as expected.
        -   Duplicate Chat Shell in DOM: Issue: A duplicate chat shell component was being rendered in the DOM in version 27.0.2, causing UI duplication and potential performance impact.
-   **Version 24.5.0 - July 2025**

    Bug Fix: Breadcrumb Not Displayed When Navigating Between Pages: Resolved an issue where the breadcrumb navigation would not appear when switching between two pages or opening a record in full details view. This fix ensures consistent breadcrumb visibility across navigation flows, improving user orientation and usability.

-   **Version 24.4.8 - May 2025**

    Fixed the incorrect breadcrumb item issue in Common Page templates.

-   **Version 27.0.2 - March 2025**

    Fixed an issue where Cancel button on Record page stopped working in YFixed an issue to address race condition between scripted extension and screen Titles.

-   **Version 27.0.1 - February 2025**

    New: Ability to resize chat shell.

-   **Version 24.4.2 - November 2024**

    Minor bug fixes.

-   **Version 24.4.1 - August 2024**

    New: You may hide the app shell search bar on the portal. This is configurable per-page.

-   **Version 24.0.5 - August 2023**

    New: Ability to collapse and expand L2 in Breadcrumb App Shell.

-   **Version 22.1.5 - December 2022**
    -   Fixed:
        -   Hide/Show L2 slot based on selected L1 item.
        -   L2 slot to show/hide based on page route.
        -   Dynamic content for L2 slot based on selected L1
-   **Version 22.1.4 - November 2022**

    This app shell focus' on workspace experiences for agents to view and resolve multiple records at the same time.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform UI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-ui.md)

