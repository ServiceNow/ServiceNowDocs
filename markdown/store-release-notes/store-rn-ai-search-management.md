---
title: Advanced AI Search Management Tools release notes
description: Version history for the Advanced AI Search Management Tools on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ai-search-management.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Admin release notes, ServiceNow Store release notes]
---

# Advanced AI Search Management Tools release notes

Version history for the Advanced AI Search Management Tools on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.0.2 - March 2026**
    -   Fixed:
        -   Resolved issue where users with the roles of analytics\_viewer, now\_experience\_analytics\_viewer, report\_analytics\_viewer were unable to see visualizations
        -   Resolved an issue where errors appeared in the logs when dashboard first opened
        -   Added logic to delete old record for pre-calculated data
-   **Version 8.0.1 - December 2025**

    New: Updated and expanded metrics for a unified view of search performance across AI Search, Now Assist, and Virtual Agent.

-   **Version 7.0.2 - August 2025**
    -   New: AI Search Analytics Dashboard: Added support for Mobile Platform search in the search application interactive filter.
    -   Changed: AI Search Analytics Dashboard: Increased the supported time period from 3 months to 6 months in the date range interactive filter.
-   **Version 6.0.10 - February 2025**
    -   Changed:
        -   Fix bug: Filter UI in Analytics dashboard
        -   Fix bug: ACL bypass for security
        -   Fix bug: Display correct trend labels
-   **Version 6.0.6 - July 2024**
    -   Fixed:
        -   AI Search Analytics Dashboard: Genius Results \(triggered vs. clicked\) shows "no data available"
        -   Search preview not displaying right count on left hand panel
        -   Last 7 days and inputting same dates in custom date range behaves different
        -   No Data /scope access issue in Documents by Search Source widget in Search Profile Analytics Dashboard
        -   Complete migration to Next Experience
        -   ACL Cleanup
-   **Version 6.0.3 - January 2024**

    Fixed misconfiguration of table/field ACLs with 'com.glide.ais.advanced\_management\_tools' plugin.

-   **Version 6.0.0 - November 2023**

    New: Update to Next Experience.

-   **Version 5.0.0 - August 2023**

    Fixed: Added validation script to the date picker to prevent selection of invalid date range

-   **Version 4.0.2 - May 2023**
    -   New:
        -   Search Analytics Dashboard now supports AI Search applications in Next Experience, including global search and Configurable Workspaces
        -   Support Next Experience Theming
    -   Changed: Modified ranges in Average Response Time Report in Search Analytics Dashboard
    -   Fixed:
        -   Fixed number of issues in Search Analytics Dashboard
        -   Fixed number of issues in Search Index Analytics
    -   Important Note: If you are using Search Analytics in San Diego and wish to see Search Analytics for Genius Results, please continue to use version 3.1.2.
-   **Version 4.0.0 - February 2023**
    -   New:
        -   Search Analytics Dashboard now supports AI Search applications in Next Experience, including global search and Configurable Workspaces
        -   Support Next Experience Theming
    -   Changed: Modified ranges in Average Response Time Report in Search Analytics Dashboard
    -   Fixed:
        -   Fixed number of issues in Search Analytics Dashboard
        -   Fixed number of issues in Search Index Analytics
    -   Important Note: If you are using Search Analytics in San Diego and wish to see Search Analytics for Genius Results, please continue to use version 3.1.2.
-   **Version 3.1.2 - June 2022**
    -   New:
        -   A new widget and visual changes are introduced in the AI Search Analytics Dashboard, including:
            -   Updated visualizations for "Average response time" and "Average click position"
            -   Added "Search Result Clicks" and "Genius Result Clicks" to the "Searches over time" trendline
            -   Added new "Self-Solved Rate" widget to quantify how AI Search improves self-service and case deflection
        -   A new Queries page is introduced in the AI Search Analytics Dashboard. Clicking on the "View all" link in the main page's "Queries" section takes users to the Queries page, where they can review detailed results for individual user search queries. This page helps business users better understand search usage and identify potential knowledge gaps.
            -   Top queries
            -   Queries with no clicks
            -   Queries with no results
    -   Fixed:
        -   Performance changes for AI Search Analytics dashboard
        -   Fixed loading failures for Search Analytics widgets
        -   Queries which result in Genius Results clicks are no longer reported as "searches without clicks"
        -   Other minor UI fixes
    -   \(This version of the AI Search Analytics Dashboard does not support accessibility.\)
-   **Version 3.1.1 - March 2022**
    -   Fixed:
        -   The AI Search Admin Dashboard now displays total and per-source counts for all indexed records \(whether they are searchable or not\).
        -   The AI Search Admin Dashboard now displays indexed record counts over time for both internal and external content sources.
        -   Updated performance for AI Search Analytics Dashboard.
    -   This version of the AI Search Analytics Dashboard does not support accessibility.
-   **Version 3.1.0 - December 2021**
    -   New:
        -   A new widget and visual changes are introduced in the AI Search Analytics Dashboard, including:
            -   Updated visualizations for "Average response time" and "Average click position"
            -   Added "Search Result Clicks" and "Genius Result Clicks" to the "Searches over time" trendline
            -   Added new "Self-Solved Rate" widget to quantify how AI Search improves self-service and case deflection
        -   A new Queries page is introduced in the AI Search Analytics Dashboard. Clicking on the "View all" link in the main page's "Queries" section takes users to the Queries page, where they can review detailed results for individual user search queries. This page helps business users better understand search usage and identify potential knowledge gaps.
            -   Top queries
            -   Queries with no clicks
            -   Queries with no results
    -   Fixed:
        -   The AI Search Admin Dashboard now displays total and per-source counts for all indexed records \(whether they are searchable or not\).
        -   The AI Search Admin Dashboard now displays indexed record counts over time for both internal and external content sources.
        -   Updated performance for AI Search Analytics Dashboard.
    -   This version of the AI Search Analytics Dashboard does not support accessibility.
-   **Version 1.0.0 - January 2021**
    -   New:
        -   The two main features this app includes are:
            -   AI Search dashboards
                -   The AI Search dashboard displays AI Search indexed record counts, configuration settings in use, and search query traffic trends.
                -   The AI Search Profile dashboard displays indexed record counts and search query traffic trends for a specific search profile.
            -   AI Search preview UI
                -   The AI Search preview UI enables search admins to test and preview search queries using settings from a selected search profile.
                -   The AI Search preview UI helps search admins review search queries' processing information, including performance data and feedback.
                -   Search admins can also debug queries, impersonate search users, and override default query settings for testing purposes in the AI Search preview UI.

**Parent Topic:**[ServiceNow Store - Admin release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-admin.md)

