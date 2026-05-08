---
title: Setting up AI Search in Service Operations Workspace for ITSM
description: Intelligent query features enable you to quickly find the answers that you require. The Next Experience Unified Navigation search field enables you to search multiple record types and switch between global search results and results from the workspace applications that you can access.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Setting up AI Search in Service Operations Workspace for ITSM

Intelligent query features enable you to quickly find the answers that you require. The Next Experience Unified Navigation search field enables you to search multiple record types and switch between global search results and results from the workspace applications that you can access.

For information about AI Search, see AI Search.

For information about installing and configuring AI Search in Next Experience, see Install AI Search for Next Experience.

The following configurations are added for the AI Search experience in Service Operations Workspace.

-   A search application configuration, \[AIS\]. For information about search application configurations, see Search application configurations. To modify the card layout of the AI Search results, you can modify its EVAM definition, AI Search for Next Experience. Search for and add an EVAM configuration bundle. For information about the EVAM definition, see Configuring EVAM definition.
-   A search profile. For information about search profiles, see AI search profiles.

    **Note:**

    -   AI Search experience is available in Service Operations Workspace starting in version 1.3.
    -   AI Search for Service Operations Workspace version 1.3 is compatible with the SR - PlatformX - Search - AI Search for Next Experience Bundle - v2.0. For all upgrade scenarios, use the Guided Setup for Zing to AI Search Migration module and ensure that the following conditions are met:

        -   New search sources should be indexed.
        -   The search profile should be published.
        -   AI Search should be enabled.
        For information about using Guided Setup for Zing to AI Search Migration, see Configuring AI Search for Next Experience.

    -   Ensure that the search engine is set to AI Search. To set the AI Search, ensure that the **globalSearchDataConfigId** UX page property value is set to the sys\_id of the AI Search, `6fcaa8d770a45110f877edb72a2fbd2f`.
-   Genius results display the most relevant information and actions for a search query using Genius Result cards. The genius result cards appear alongside the regular search results. For more information about genius results, see Genius Results. By default, Service Operations Workspace supports the Q&amp;A genius result configuration. If it isn’t active, ensure the following:
    -   Ensure that the version of AI Search for Next Experience is 3.0 or later.
    -   Ensure that the Q&amp;A genius result configuration is in an Active state. For more information about the Q&amp;A genius result configurations, see Q&amp;A Genius Results.

![AI Search in Service Operations Workspace.](../image/ai-search-sow.png "AI Search experience in Service Operations Workspace")

You can customize the AI Search experience by adding a data source, editing a search profile, and so on, by using the AI Search Guided Setup. For information on using this guided setup, see Configuring AI Search.

**Parent Topic:**[Setting up integrations in Service Operations Workspace for ITSM](setting-up-sow-itsm.md)

