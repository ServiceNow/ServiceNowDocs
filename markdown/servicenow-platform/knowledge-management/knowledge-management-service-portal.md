---
title: Configure the Knowledge Management Service Portal
description: The Knowledge Management Service Portal enables users to perform the same operations that are available with the Knowledge Management V3 plugin. From the portal, users can view knowledge bases and articles, search for information, sort and filter search results, and provide feedback.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the Knowledge Management Service Portal

The Knowledge Management Service Portal enables users to perform the same operations that are available with the Knowledge Management V3 plugin. From the portal, users can view knowledge bases and articles, search for information, sort and filter search results, and provide feedback.

-   For new customers on the Madrid and later releases, the Knowledge Management Service Portal plugin \(com.snc.knowledge\_serviceportal\) is active by default.
-   For existing customers on release versions prior to Madrid, activate the plugin, if required.
-   Configure the [Knowledge Management Service Portal properties](../reference/knowledge-service-portal-properties.md), including the property that directs users to the Knowledge Management homepage in the Knowledge Management Service Portal.

-   Navigate to **Service Portal** &gt; **Portals** and click **Knowledge Portal** \(Knowledge Management Service Portal is named as Knowledge Portal\). See [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information about creating a custom interface.
-   System administrators can configure portal pages and configure widgets for searching, sorting, and filtering knowledge base information. To configure widget instance options and configure search, sort, and filter features, see [Knowledge Management Service Portal widgets](km-service-portal-widget-instances.md)
-   To add knowledge bases to the Knowledge Service Portal, complete the following steps.
    1.  Navigate to **Service Portal** &gt; **Portals**, and click **Service Portal**.
    2.  Click the **Knowledge Bases** related list.
    3.  Click **Edit** to map one or more knowledge bases to the portal.

        **Note:** If no knowledge bases are added, all knowledge bases are available in the portal.

        If knowledge bases are mapped, only those knowledge bases are available in the portal. All search results and all widgets display results from the mapped knowledge bases only.

-   **Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](knowledge-service-portal-pages.md).


## Section 508 compliance features

Users can view and interact with the Knowledge Management article view page in the Knowledge Management Service Portal using Section 508 compliance features. See [Enabling accessibility features](https://www.servicenow.com/docs/access?context=c_SetUpSect508ComplianceFeature&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

-   **[Enable external or public users to view knowledge articles from the Knowledge Management Service Portal](../task/make-knowledge-visible-to-public.md)**  
Enable knowledge articles on the Knowledge Management Service Portal to be visible to external or public users.
-   **[Knowledge Management Service Portal widgets](km-service-portal-widget-instances.md)**  
The Knowledge Management Service Portal uses a number of widgets to enable searches, display search results, and display articles, related articles, and related items.
-   **[Search using the Knowledge Management Service Portal](../reference/knowledge-service-portal-searching.md)**  
Enter one or more words in the search bar on the Knowledge Management Service Portal homepage to view all search results.
-   **[Integrating Knowledge Management features with the Service Portal](conf-service-portal-know-management.md#)**  
To create a consistent user experience for Knowledge Management, integrate Knowledge Management Service Portal in your end-user facing Service Portal.
-   **[Configure custom SEO tags for canonical URLs and localized knowledge articles](../task/configure-seo-knowledge.md)**  
Discover relevant knowledge articles through search engines by adding custom SEO tags for canonical URLs and **hreflang** tags to the knowledge article view page.
-   **[Enable and configure AI Search for Knowledge Management Service Portal](../task/enable-and-configure-ai-search-for-km-service-portal.md)**  
Enable and define the AI Search experience in Knowledge Management Service Portal.

**Parent Topic:**[Configuring Knowledge Management](configuring-knowledge-management.md)

**Related topics**  


[Knowledge Management FAQ](https://community.servicenow.com/community?id=community_article&sys_id=637ffc92db519490d82ffb24399619f3)

[Import a Word document to a knowledge base](../task/import-word-platform.md)

[Import a Word document to a knowledge base using Knowledge Management v3](../task/t_ImportADocument.md)

