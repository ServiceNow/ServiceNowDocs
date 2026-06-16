---
title: Conversational Analytics release notes
description: Version history for the Conversational Analytics on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-conversational-analytics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Conversational Interfaces, ServiceNow Store release notes]
---

# Conversational Analytics release notes

Version history for the Conversational Analytics on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 9.2.0 - June 2026 \(Australia\)**
    -   Fixed: Minor defects
    -   Removed: Appsee plugin dependency
-   **Version 9.1.3 - March 2026 \(Australia\)**

    Fixed: Minor defects

-   **Version 9.1.2 - December 2025 \(Zurich\)**
    -   New: Enhanced to support domain separation
    -   Fixed: Minor bugs
-   **Version 9.1.1 - September 2025 \(Zurich\)**

    Minor bugs.

-   **Version 9.1.0 - August 2025 \(Zurich\)**
    -   Changed:
        -   Redesigned the User Search Metrics page to improve data visualizations and usability.
            -   Introduced single score visualizations to display overall totals at a glance.
            -   Added bar charts to highlight the top 10 items in each of the following categories: AI Search, Contextual Search, Topic Links.
-   **Version 8.0.16 - August 2025 \(Yokohama\)**
    -   Changed:
        -   Redesigned the User Search Metrics page to improve data visualizations and usability.
            -   Introduced single score visualizations to display overall totals at a glance.
            -   Added bar charts to highlight the top 10 items in each of the following categories: AI Search, Contextual Search, Topic Links.
-   **Version 8.0.15 - May 2025**
    -   Changed: Minor modifications in UI
    -   Fixed: Minor bugs
-   **Version 8.0.12 - March 2025 \(Yokohama\)**

    Fixed minor bugs.

-   **Version 8.0.11 - February 2025 \(Yokohama\)**
    -    New :
        -   Added drill-downs to the following visualizations on the Overview page :
            -   VA Success 
            -   Topic Category - Complete 
            -   Topic Category - Incomplete 
            -   User Feedback 
            -   Channel 
            -   Conversation end state 
        -   Added drill-down to the following visualization on the Topics page : Spokes used 
    -   Fixed  minor bugs 
-   **Version 8.0.7 - November 2024 \(Xanadu\)**
    -   New:
        -   Added drill downs to the list of conversations from the Usage dashboard page.
        -   Added drill downs to the Topic details page from the Overview and Topic pages.
        -   Added a system property to hash user IDs on the dashboard pages.
    -   Fixed: Minor bugs
-   **Version 8.0.4 - August 2024 \(Xanadu\)**

    Minor bug fixes.

-   **Version 6.1.0 - February 2024 \(Washington DC\)**
    -   Changed:
        -   Notification conversations are excluded from analytics.
        -   Consumer-less conversations are treated as guest conversations.
    -   Removed: sn\_ci\_analytics.ca.allow\_broadcast property has been removed.
-   **Version 6.0.2 - November 2023**

    Minor fixes.

-   **Version 6.0.1 - August 2023**
    -   New:
        -   Added support for Next Experience UI.
        -   Added drop-down in the Topics tab to view metrics based on selected categories.
    -   Changed: In the Users tab, Unhashed User IDs display as Anonymous and Hashed User IDs display User ID of the user.
    -   Minor fixes.
-   **Version 5.2.1 - May 2023**

    Minor fixes.

-   **Version 5.1.0 - February 2023**
    -   New: Conversation transcript .txt file: Conversation transcript downloadable file format has been changed to .txt file and includes ServiceNow Flow Designer Integration Hub \(FDIH\) debug logs for input and output controls, topic block information, flow action, and custom controls, to troubleshoot conversations.
    -   Fixed: UX fixes
-   **Version 4.3.0 - May 2023**

    Minor fixes.

-   **Version 4.2.4 - November 2022**

    Fixes, based on priority.

-   **Version 4.2.0 \(Tokyo\) - August 2022**

    New: Added the ability to download chat transcript.

-   **Version 3.0.8 \(San Diego\) - August 2022**

    Minor fixes.

-   **Version 2.1.27 \(Rome\) - August 2022**

    Minor fixes.

-   **Version 3.0.5 - May 2022**
    -   Fixed:
        -   Installation issue
        -   Issue with export of custom events
        -   Funnels - create, edit, and updateIssues in the Spokes tab
-   **Version 3.0.3 - February 2022**
    -   New:
        -   Added Click Metrics feature
        -   Added VA Transcript feature
    -   Fixed:
        -   Issue regarding loading of Transcript header and icon when users view the first conversations transcript
        -   Data not being displayed properly in User Search Metrics tab
        -   Log error issue while processing Contextual Search Topic
        -   Missing hashed user id and labels in the User detail page
        -   Capitalised 'p' in NLU prediction tab text
        -   Issue of scorecard difference count being shown in exponent values
        -   Issue of Usage Search Metrics tab disappearing after every glide change upgrade
        -   Removed Extra space below the Transcript preview
        -   Preview conversations being processed
        -   Overlap of Close icon with widget
        -   Topics being incorrectly sorted in funnel builder in certain settings
        -   Changing of transcripts when conversation messages do not exist in the instance
        -   Transcripts not getting updated when users switch conversations
        -   Decimal values being displayed for counts in all charts
        -   Alignment and spacing of icons in IAR, topic details, custom events widgets
        -   Incorrect representation of "Queries with no results" as "Queries with no clicks"
        -   Missing borders and extra spaces in users table and usage widgets
        -   Calendar date being reset to one week when user moves from "user detail page" to Users tab
        -   Blank page when user tries to edit page in UIB from Virtual agent analytics page
-   **Version 2.1.2 - December 2021**

    New: LUA metrics related to topic completion data is added.

-   **Version 2.1.1 - October 2021**

    Fixed: Bug fixes.

-   **Version 2.0.6 - August 2021**
    -   New:
        -   Updated Issue Auto Resolution page
        -   Added Deflection Metrics widgets
        -   Introduced Funnel Builder capability
        -   Replaced classic Query Builder with the VA condition builder
    -   Fixed: Minor functional changes and fixes for list pagination, export functionality, and so on.
-   **Version 1.1.0 - April 2021**

    Fixed: Security fixes.

-   **Version 1.0.10 - February 2021**

    New: The Conversational Analytics Dashboard helps you improve Virtual Agent \(VA\) interactions with users by providing deep insights into conversational data. Discover which topics confuse users. Find out where users often transfer to live agents. The dashboard helps you refine your topics and increase the percentage of issues resolved by VA.


