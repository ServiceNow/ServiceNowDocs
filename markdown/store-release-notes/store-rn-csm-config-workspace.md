---
title: CSM Configurable Workspace release notes
description: Version history for the CSM Configurable Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-config-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# CSM Configurable Workspace release notes

Version history for the CSM Configurable Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 26.3.2 - June 2026**

    Java 21 Compile Upgrade

-   **Version 26.2.3 - May 2026**

    Configurable workspace release with minor enhancements and Activity Timer Log that displays a report of time spent by agents on records.

-   **Version 26.0.2 - March 2026**
    -   New Features:
        -   Email Response Notifications on Record Tabs: Agents now see a badge with a counter on the record tab when new customer email responses arrive. This reduces manual checking, prevents missed updates, and aligns the email experience with existing chat notification patterns for smoother multi‑channel workflows.
        -   Dashboard List Migration to Record Lists: Dashboard widgets now open using the default Record List instead of Simple List, enabling pagination, richer filtering, and consistent drill‑down behavior.
-   **Version 26.1.1 - March 2026**
    -   AI &amp; Productivity
        -   AI Wrap-Up: Auto-populates wrap-up fields with AI-generated notes and codes, clearly flagged for agent review.
        -   Hybrid Search for Recommended Actions: Combines keyword and semantic matching to surface more relevant KB articles faster.
        -   Knowledge Article Advanced Editor: Drag-and-drop KB authoring with Now Assist prompts and Article Optimization built in.
    -   Agent Experience:
        -   Modeless Dialogs &amp; Attachments: Create actions and attachment previews open modeless, keeping agents in context with carousel navigation across files.
        -   ITSM–CSM Page Interoperability: Case, Incident, and Change pages now render inside the CSM workspace, reducing context switching. Off by default.
        -   Editable Record Headers: Edit short descriptions inline without scrolling. Changes save immediately with unsaved-state indicators.
        -   Visual Dirty-State Indicators: Unsaved form changes are highlighted with color and dot indicators to reduce errors.
        -   Front-line Case Bottom Utility Panel: Persistent contextual actions and modeless dialog placeholders that stay visible during case work.
    -   Workspace Flexibility:
        -   Multiple Dashboards in Primary Tabs: Open multiple dashboards and lists in separate tabs instead of replacing the current view.
        -   Form Template Enhancements: Advanced field conditions, variable pickers, and email integration in v2 templates.
        -   EAAI Revamp: New Lookup component, bottom email composer, and reversed activity stream for streamlined email handling.
-   **Version 25.4.1 - December 2025**
    -   New Features:
        -   Email Interaction Enhancements: We’ve modernized the email compose experience! You’ll notice reversed activity stream sorting and quick access to related emails and attachments right from the case record, making email interactions smoother and more contextual.
        -   State Field Control: The State field is now read-only on the Front-line and CSM default record pages. This ensures changes happen only through proper UI actions, keeping processes consistent and error-free.
        -   Introducing the ‘Follow’ Button: Want to stay in the loop? A new configurable Follow button on case pages lets you track updates easily. Admins can enable or disable this at the site level.
        -   Activity Stream Optimization: Cleaner, more responsive design with less white space and improved visuals for a better experience across all devices.
        -   Knowledge Article Recommendations: Get smarter suggestions! Machine learning now recommends similar knowledge articles based on case descriptions, with Now Assist integration for helpful actions and messaging tips.
        -   Thin Compose on Interaction Pages: Thin Compose is here \(default off\) for CSM, Voice, Email, and Center chat interaction record pages, bringing new productivity features to your workflow.
        -   Responsive Pages &amp; Resizable Panes: Interaction, case, and chat pages now adapt beautifully to smaller screens. Plus, you can resize panes and enjoy modeless dialogs that fit your view.
        -   Task activity timeline preset and controller: Use this preset and controller to add the Timeline component as a flexible, standalone timeline for activity history that you can place anywhere in the workspace.
        -   Notifications via Mentions: Get instant in-app notifications when you’re mentioned in work notes, comments, or emails, with accurate counts and quick navigation to the right record.
    -   Performance Improvements: Faster chat acceptance times and ongoing optimizations for smoother agent and customer interactions.
    -   Defect Fixes: We’ve squashed bugs! Fixes include UI action issues, access errors, sidebar clicks, metric script problems, field dependency failures, and watchlist visibility glitches.
-   **Version 25.3.6 - October 2025**

    Bug fixes for the CSM Front-line case page and activity stream.

-   **Version 24.3.16 - September 2025**

    Defect fix to add sentiment analysis to the CSM default record page.

-   **Version 25.3.2 - August 2025**
    -   New:
        -   CSM Centered Chat Interaction Page: Redesigned interaction page with a modernized, central chat component for front-line chat agents.
        -   Callback Component for Voice Interactions: Agents can return customer calls and create interaction records during callbacks.
        -   Thin Compose Modeless Dialogs: Start comments, work notes, or emails from the activity stream in a non-blocking dialog.
        -   Lookup Component Improvements: New, streamlined Lookup component replaces previous Lookup and Verify on CSM Configurable Workspace pages.
        -   Inbox Auto-hide: Inbox panel collapses upon item selection for better screen focus.
        -   Alert Dismissal Configuration: Choose between auto or manual alert dismissal globally or per alert to reduce overload and improve focus.
        -   ServiceNow Link Manager Chrome Extension: Consolidate ServiceNow tabs and easily share record links via common collaboration platforms. Cross-platform support and easy on/off control.
        -   Coral Theme Default: The fresh, brand-neutral Coral theme is now the default for new experiences. Includes a dark theme option.
    -   Changed:
        -   Customer History updates
            -   New options for quarterly time grouping, custom feed icons/colors, and feeds sorted by last updated date.
            -   Dynamic refresh for history feeds relevant to the current context.
        -   Recommended Actions Enhancements
            -   Set as the first tab for instant agent access across all major CSM pages.
            -   Loads asynchronously to keep the UI responsive.
            -   Agents can now send KB articles via SMS for voice interactions.
            -   Default recommendations available to Pro customers with contextual insights, such as similar cases.
        -   Special Handling Notes: Easily access special handling information from the case record action bar across key tables.
-   **Version 25.1.4 - June 2025**

    Support for Sentiment Analysis at case level.

-   **Version 25.1.3 - May 2025**
    -   Changed:
        -   Click improvements - when using Form templates with modeless dialogs they automatically open the modeless dialog \(comment/worknotes\) with the populated content making it easier to edit and save clicks of opening the modeless.
        -   Lookup component improvements include the ability to collapse the card saving real-estate and advanced search.
        -   Replaced Agent Assist with Recommend Actions – AI Search on Agent Workspace Case and Interaction pages.
        -   Improved performance in page and component load times.
-   **Version 25.0.11 - April 2025**

    Fixed the issue where the Case Summarization card does not show on the first load of a record page.

-   **Version 25.0.10 - March 2025**

    Fix for missing Case type functionality.

-   **Version 25.0.9 - February 2025**

    Includes product bug fixes.

-   **Version 24.4.10 - January 2025**

    Includes product bug fixes.

-   **Version 24.4.4 - November 2024**

    Incremental release of the CSM Configurable Workspace with a few improvements.

-   **Version 24.3.8 - August 2024**
    -   New: Hide Entitlements related list for service contract lines
        -   Sold Product Covered related list filters on workspace now shows all the active SP Covered records
-   **Version 24.3.6 - August 2024**
    -   New: Improvement for Case type selector \(product filter\)
    -   Fixed: auto populate field values which are set up on single selection definition configuration
-   **Version 24.2.0 - Mary 2024**
    -   New:
        -   Front-line case page which introduces modeless dialogs for Activity Compose \(work notes and comments\) and Email Compose.
        -   Keyboard shortcuts for Compose email/work-note/comment.
-   **Version 23.4.5 - September 2023**
    -   New:
        -   Chat summarization
        -   Case summarization
        -   Now Assist for Search
        -   Now Assist
        -   Now Assist Admin
-   **Version 23.3.6 - August 2023**

    New:

    The following are the new features:

    -   Dashboards as landing pages
    -   Updated compact mode
    -   Email templates
-   **Version 23.2.4 - June 2023**

    Fixed:

    -   Assigned to value from cases is not auto-filled when creating case from multi and single selector.
    -   Back button works only for product service selector; for multi select and single selection it is not working.
    -   Voltron Enabled: Case task selector doesn't open on click of New button on Task related list.
-   **Version 23.2.3 - May 2023**

    New: The Record Presence feature and the AI Search facet for escalated cases are available to customers out-of-the-box on installing this store app.

-   **Version 23.1.3 - February 2023**

    Changed:

    -   CSM modal page collection that includes CSM related modal pages
    -   CSM record page templates for CSM default record page and CSM Interaction record page
    -   Uptake AI search capabilities for CSM Configurable Workspace
-   **Version 23.0.5 - November 2022**

    New:

    Two new record pages built with Presets and Controllers are introduced in this store release.

    -   CSM default record page
    -   CSM Interaction record page
    If you install this store app and you want to use any of the following features, you must also upgrade to the corresponding store apps:

    -   Recommended Actions for Customer Service v24.0.0
    -   Playbooks for Customer Service Management v2.1.0
    -   Case Playbook for Onboarding v4.1.0
    -   Case Playbook for Complaints v4.1.0
    -   FSM Configurable Dispatcher Workspace v23.2.3
-   **Version 22.2.15 - August 2022**

    Next Experience UI Builder is a WYSIWYG web user interface builder for building and configuring CSM Configurable Workspace pages and components. With UI Builder, you can preview workspace experiences as you're developing them. The CSM Configurable Workspace includes experiences that use lists and forms.


