---
title: Customizing the result-card interface of an AI Search application by using EVAM
description: You can customize the appearance and layout of the result-card interface in AI Search applications by accessing Entity View Action Mapper \(EVAM\) configurations from the AI Search Admin console. This helps to enhance usability, clarity of search results, making them easier to read and navigate.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Using AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Customizing the result-card interface of an AI Search application by using EVAM

You can customize the appearance and layout of the result-card interface in AI Search applications by accessing Entity View Action Mapper \(EVAM\) configurations from the AI Search Admin console. This helps to enhance usability, clarity of search results, making them easier to read and navigate.

## Using EVAM to modify the Result-card interface overview

AI Search Admin console provides a unified platform that enables you to manage the search result interface of your AI Search application with EVAM configurations. EVAM standardizes how different data sources are displayed in cards and lists. You can create, edit, copy, view usage, activate, deactivate, or delete EVAM view configurations, and even create EVAM definitions as needed all from the AI Search Admin console. To learn more about EVAM, see Exploring Entity View Action Mapper.

The Result-card interface in AI Search applications displays a search result in clear, visual format. It includes key details, such as title, a brief description, relevant icons, and other important information. This helps users quickly understand each search result and decide which one to explore further.

The following example shows the Result-card interface of the AI Search application. You can select a EVAM view config bundle and its related view configs to create or edit the EVAM configurations, customizing how the search results are displayed and organized.

![Result-card interface of the search application in the AI Search Admin console where you can configure EVAM display options for search results in AI Search.](../image/ais-view-config.png "Result-card interface")

The following table describes the tasks that you can do to set up the search result interface by using EVAM.

|Task|Description|
|----|-----------|
|Map fields to display in search results|Define which fields from your data should be shown in the search results to help ensure that the most relevant information is presented to users. For more information, see [View config details fields](../reference/ais-edit-view-config-form.md).|
|Configure icons for search results|Assign specific icons to different types of search results to make them visually distinct and easier to identify at a glance. For more information, see [Card image fields](../reference/ais-edit-view-config-form.md).|
|Configure navigation actions|Set up actions that users can take directly from the search results, such as navigating to a related page. For more information, see [Card details field](../reference/ais-edit-view-config-form.md).|

-   **[Create or edit an EVAM view definition](../task/ais-admin-console-evam-configurations.md)**  
Create or edit an Entity View Action Mapper \(EVAM\) view definition in the AI Search Admin console to customize how your AI Search results appear in the portal or workspace.
-   **[Create a copy of an EVAM view configuration](../task/copy-evam-viewconfig-ais-admin-console.md)**  
Modify the search results of your AI Search application by creating a copy of an existing Entity View Action Mapper \(EVAM\) view and then changing the copy. Copying an EVAM is more efficient than creating an EVAM, especially when the changes are minimal.
-   **[Track how your EVAM view configurations are used](../task/ais-admin-console-evam-viewusage.md)**  
Track where Entity View Action Mapper \(EVAM\) view configurations are being used in the AI Search application. It helps you understand search result layouts, identify shared settings, and make adjustments for better search results.
-   **[Activate or deactivate an EVAM view configuration](../task/enable-evam-config-ais-admin-console.md)**  
Activate or deactivate the Entity View Action Mapper \(EVAM\) view configurations in the AI Search application as needed. This helps you to control which view configurations are in use.
-   **[Delete an EVAM view configuration](../task/delete-evam-config-ais-admin-console.md)**  
Delete unnecessary Entity View Action Mapper \(EVAM\) view configuration from your AI Search application at any time to keep the application clean and organized

**Parent Topic:**[Using AI Search Admin console](using-ais-admin-console.md)

