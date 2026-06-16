---
title: Recommended Actions release notes
description: Version history for the Recommended Actions application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-rec-actions.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Recommended Actions release notes

Version history for the Recommended Actions application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 42.0.0 - June 2026**
    -   New:
        -   Java 21 Compile Upgrade – The Recommended Actions application has been upgraded to compile with Java 21, ensuring platform compatibility and performance improvements.
        -   Role inheritance &amp; ACL review in the base system – Role inheritance and ACL configurations in the base system have been reviewed and aligned for subscription-based access control.
        -   Accessibility \(A11y\) improvements – Core UI and seismic components now meet WCAG 2.2 AA standards, including 400% zoom and reflow support for improved accessibility compliance.
        -   Agentic workflow enhancement – Dynamic search terms can now be passed as Guidance input to support agentic workflow execution in Recommended Actions.
-   **Version 41.0.2 - March 2026**
    -   New: The total number of search results is displayed in the AI search tab of the Recommended Actions Contextual side panel when Hybrid Search is enabled.
    -   Fixed: Minor fixes for this release.
-   **Version 40.0.0 - February 2026**

    Fixed: Minor defect fixes for this release.

-   **Version 39.0.0 - January 2026**
    -   New:
        -   Supports relevancy score for the Attach and share article, Default guidance for search results, Share KB in chat interactions, and all no-code guidances.
        -   Supports top N results and relevancy scores for AI search results.
        -   Supports contextual filter preprocessing in AI Search.
-   **Version 38.0.2 - December 2025**
    -   New:
        -   Enabled Recommended Actions pre-fetch functionality.
        -   Enabled logging of AI search and result events originating from Recommended Actions component across workspaces.
        -   Enabled selection of multiple search sources for AI search within Recommended Actions.
    -   Fixed: Minor fixes.
-   **Version 37.0.2 - September 2025**
    -   Fixed:
        -   The field recommendations now display correctly upon page refresh.
        -   The search results now update correctly when you select a source or facet filters on the Search page.
-   **Version 37.0.1 - August 2025**
    -   Enabled the trigger refresh for recommendations both explicitly and in response to UI events.
    -   Optimized Recommended Actions refresh experience by excluding non-critical field updates.
    -   Enhanced context management with dynamic context inputs.
    -   Minor bug fixes for this release.
-   **Version 35.0.1 - May 2025**
    -   New:
        -   Enabled Async mode for Recommended Actions, which allows the Recommend Actions API to be invoked asynchronously to fetch the recommendations.
        -   Enabled multiple contexts for the table, which allows the creation of multiple Recommended Action contexts for it.
    -   Fixed: Minor bug fixes for this release.
-   **Version 34.1.0 - April 2025**

    New:

    -   Added the ability to customize font size for questions in a decision tree.
    -   Added the ability to control the visibility of completed guidance in a decision tree.
-   **Version 34.0.1 - February 2025**
    -   Automate creation of Search Result Mapping records for new contexts.
    -   Improved performance of Recommended Actions Suggested tab and Search tab generation.
-   **Version 33.0.2 - January 2025**

    Bug fix.

-   **Version 33.0.1 - November 2024**
    -   Improvements to support new RA component property and guidance action triggered event propagation
    -   Bug fixes
-   **Version 32.0.1 - August 2024**
    -   Added support for new Task Intelligence similarity Resource Generator Type.
    -   Added support to configure context records through an active flag mechanism.​
-   **Version 31.0.3 - July 2024**

    Added a job which will add guidance user role to NBA Author users when the upgrade is triggered. This is to reduce the upgrade time when there are many user records with the NBA Author Role.

-   **Version 29.0.2 - June 2024**

    Bug fixes.

-   **Version 31.0.2 - May 2024**
    -   Changed the default icon for the side panel.
    -   Enabled sorting on search results based on relevancy and recency.
    -   Added new property for hiding full search view icon and change label for default search field.
    -   Enabled parsing of genius result pill picker as part of search result mapping.
    -   Support for full view search.
-   **Version 29.0.1 - March 2024**

    The searchTerm from AI Search resource generator is preprocessed before making the search to provide more accurate results.

-   **Version 29.0.0 - February 2024**
    -   Capturing sys id for predicted values to support top N recommendations for a record field.
    -   Fixes
-   **Version 28.0.0 - November 2023**

    New feature to show unified search results powered by AI discovery engine. Search across entities and view unified search results ranked by relevance.

-   **Version 27.0.1 - September 2023**

    Fix for error on case load in CSM/FSM Configurable workspace.

-   **Version 27.0.0 - August 2023**
    -   Changes in Recommended Actions framework to support Task Intelligence Classification Resource generator changes.
    -   Changes to reference qualifiers for Resource generators using ML models.
    -   Other fixes.
-   **Version 26.0.0 - May 2023**
    -   Changes for field recommendations definitions to support Task Intelligence Classification resource generators.
    -   Fixes for field recommendations for unsaved changes.
-   **Version 25.0.0 - February 2023**
    -   New
        -   -   Changes to support the grouping of recommendations based on recommendation criteria.
-   Changes to support custom preview and detail experiences for guidance recommendation cards.
-   **Version 24.0.1 - November 2022**
    -   Changes to guidance experience to show error messages and notifications in case multiple users are acting on the same recommendation.
    -   Changes to show error messages if recommendations fail during execution.
-   **Version 23.0.0 - August 2022**

    Recommended Actions enable agents to view and select one or more contextually relevant actions based on insights generated with defined rules. For example, an agent working on a case can review and select a contextually relevant action that links the case to a related product issue. Recommended Actions provides the ability to configure recommendations based on related context, giving agents the resources and information they need to resolve cases quickly.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

