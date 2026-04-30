---
title: AI Search in Service Operations Workspace for ITSM
description: Intelligent query features enable you to quickly find the answers that you require. The Next Experience Unified Navigation search field enables you to search multiple record types and switch between global search results and results from the workspace applications that you can access.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# AI Search in Service Operations Workspace for ITSM

Intelligent query features enable you to quickly find the answers that you require. The Next Experience Unified Navigation search field enables you to search multiple record types and switch between global search results and results from the workspace applications that you can access.

For information about AI Search, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For information about installing and configuring AI Search in Next Experience, see [Install AI Search for Next Experience](https://www.servicenow.com/docs/access?context=install-ais-next-experience-app&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following configurations are added for the AI Search experience in Service Operations Workspace.

-   A search application configuration, \[AIS\]. For information about search application configurations, see [Search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). To modify the card layout of the AI Search results, you can modify its EVAM definition, AI Search for Next Experience. Search for and add an EVAM configuration bundle. For information about the EVAM definition, see [Configuring EVAM definition](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   A search profile. For information about search profiles, see [AI search profiles](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    **Note:**

    -   AI Search experience is available in Service Operations Workspace starting in version 1.3.
    -   AI Search for Service Operations Workspace version 1.3 is compatible with the SR - PlatformX - Search - AI Search for Next Experience Bundle - v2.0. For all upgrade scenarios, use the Guided Setup for Zing to AI Search Migration module and ensure that the following conditions are met:

        -   New search sources should be indexed.
        -   The search profile should be published.
        -   AI Search should be enabled.
        For information about using Guided Setup for Zing to AI Search Migration, see [Configuring AI Search for Next Experience](https://www.servicenow.com/docs/access?context=configuring-ais-next-experience&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    -   Ensure that the search engine is set to AI Search. To set the AI Search, ensure that the **globalSearchDataConfigId** UX page property value is set to the sys\_id of the AI Search, `6fcaa8d770a45110f877edb72a2fbd2f`.
-   Genius results display the most relevant information and actions for a search query using Genius Result cards. The genius result cards appear alongside the regular search results. For more information about genius results, see [Genius Results](https://www.servicenow.com/docs/access?context=genius-results-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). By default, Service Operations Workspace supports the Q&amp;A genius result configuration. If it isn’t active, ensure the following:
    -   Ensure that the version of AI Search for Next Experience is 3.0 or later.
    -   Ensure that the Q&amp;A genius result configuration is in an Active state. For more information about the Q&amp;A genius result configurations, see [Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=genius-result-q-a-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

![AI Search in Service Operations Workspace.](../image/ai-search-sow.png "AI Search experience in Service Operations Workspace")

You can customize the AI Search experience by adding a data source, editing a search profile, and so on, by using the AI Search Guided Setup. For information on using this guided setup, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Configuring Service Operations Workspace for ITSM](configure-sow.md)

**Related topics**  


[Admin Center in Service Operations Workspace for ITSM](admin-center-sow.md)

[Customize the Service Operations Workspace for ITSM landing page](customize-sow-landing-page.md)

[Assign the service desk agent role to the user in Service Operations Workspace](../task/assign-service-desk-agent-role-sow.md)

[Reorder the navigation pane modules in Service Operations Workspace for ITSM](../task/reorder-left-navigation-pane-modules.md)

[Configure a record page tab in Service Operations Workspace](../task/configure-record-page-tab.md)

[Configure a task record form in Service Operations Workspace](../task/configure-form-layout-task.md)

[Configure the inbox in Service Operations Workspace](../task/configure-inbox-in-sow.md)

[Configure Standard Record Page in Service Operations Workspace](srp-service-operations-workspace.md)

[Configure the SOW list page](../task/incident-list-page.md)

[Define and customize activity stream tags](../task/define-customize-activity-stream-tags.md)

[Configure the Assign or Resolve dialog box for an incident or change request in Service Operations Workspace](../task/configure-assign-resolve-modals-incident.md)

[Customize the incident record page](customize-the-incident-record-page.md#)

[Setting up Investigation Framework in Service Operations Workspace](set-up-investigate.md)

[Create a task type for problem or change in Service Operations Workspace](../task/create-task-type-sow.md)

[Configuring Recommendation Framework in Service Operations Workspace](set-up-recommendation-framework-sow.md)

[Configure the display of requester related records in an interaction](../task/configure-order-related-records-interaction.md)

[On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)

[Configure the experts On-call panel](../task/customize-experts-on-call-tab.md)

[Setting up Service Desk assisted Password Reset in Service Operations Workspace](setup-password-reset-sow.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](../task/integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](../task/configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](../task/specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](../task/install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](../task/install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](configure-interaction-management-sow.md)

