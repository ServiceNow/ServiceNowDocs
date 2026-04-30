---
title: Customizing the result-card interface of an AI Search application by using EVAM
description: You can customize the appearance and layout of the result-card interface in AI Search applications by accessing Entity View Action Mapper \(EVAM\) configurations from the AI Search Admin console. By customizing this interface, you can help to enhance the usability and clarity of the search results for your users.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Customizing the result-card interface of an AI Search application by using EVAM

You can customize the appearance and layout of the result-card interface in AI Search applications by accessing Entity View Action Mapper \(EVAM\) configurations from the AI Search Admin console. By customizing this interface, you can help to enhance the usability and clarity of the search results for your users.

## Using EVAM to modify the result-card interface overview

The AI Search Admin console provides a unified platform that enables you to manage the search result interface of your AI Search application with EVAM configurations. EVAM standardizes how different data sources are displayed in cards and lists. You can create, edit, copy, view usage, activate, deactivate, or delete EVAM view configurations, and even create EVAM definitions from the AI Search Admin console. To learn more about EVAM, see .

The result-card interface in AI Search applications displays the search results in a clear, visual format and includes such key details as the title, a brief description, and relevant icons. Your users can quickly understand each search result and decide which result to explore further.

The following example shows the result-card interface configurations of the AI Search application. By selecting an EVAM view config bundle and its related view configs to create or edit EVAM configurations, you can customize how the search results are displayed and organized.

![Result-card interface of the search application in the AI Search Admin console where you can configure EVAM display options for search results in AI Search.](../image/ais-view-config.png "Result-card interface configurations")

The following table describes the tasks that you can do to set up the search result interface by using EVAM.

|Task|Description|
|----|-----------|
|Map fields to display in search results|Define which fields from your data should be shown in the search results to help ensure that the most relevant information is displayed to your users. For more information, see [View config details fields](../reference/ais-edit-view-config-form.md).|
|Configure icons for search results|Assign specific icons to different types of search results to make them visually distinct and easier to identify at a glance. For more information, see [Card image fields](../reference/ais-edit-view-config-form.md).|
|Configure navigation actions|Set up actions that users can take directly from the search results, such as navigating to a related page. For more information, see [Card details field](../reference/ais-edit-view-config-form.md).|

-   **[Create or edit an EVAM view definition](../task/ais-admin-console-evam-configurations.md)**  
Create or edit an Entity View Action Mapper \(EVAM\) view definition in the AI Search Admin console to customize how your AI Search results are displayed in the portal or workspace.
-   **[Copy an EVAM view configuration](../task/copy-evam-viewconfig-ais-admin-console.md)**  
Copy an existing Entity View Action Mapper \(EVAM\) view configuration and modify it to customize the search result display in your AI Search application. Copying an EVAM is more efficient than creating an EVAM, especially if the changes are minimal.
-   **[Track how your EVAM view configurations are used](../task/ais-admin-console-evam-viewusage.md)**  
Track where Entity View Action Mapper \(EVAM\) view configurations are being used in the AI Search application. Tracking helps you to understand the search result layouts, identify the shared settings, and make the adjustments for better search results.
-   **[Activate or deactivate an EVAM view configuration](../task/enable-evam-config-ais-admin-console.md)**  
Activate or deactivate the Entity View Action Mapper \(EVAM\) view configurations in the AI Search application as needed. By activating or deactivating an EVAM view configuration, you can control which view configurations are in use.
-   **[Delete an EVAM view configuration](../task/delete-evam-config-ais-admin-console.md)**  
Delete an unnecessary Entity View Action Mapper \(EVAM\) view configuration from your AI Search application at any time helps to improve the search result performance.

**Parent Topic:**[Using the AI Search Admin console](using-ais-admin-console.md)

