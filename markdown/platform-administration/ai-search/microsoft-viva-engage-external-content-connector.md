---
title: Microsoft Viva Engage external content connector
description: The Microsoft Viva Engage external content connector retrieves messages and attachments from conversations in your Microsoft Viva Engage source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-04"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Microsoft Viva Engage external content connector

The Microsoft Viva Engage external content connector retrieves messages and attachments from conversations in your Microsoft Viva Engage source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Limitations for the Microsoft Viva Engage external content connector

The Microsoft Viva Engage external content connector only retrieves searchable content from attachments that are stored in Microsoft SharePoint Online. To learn about file attachment storage in Microsoft Viva Engage, see the Microsoft [Viva Engage file storage overview](https://learn.microsoft.com/en-us/viva/engage/get-started-with-viva-engage/file-storage) resource.

Only members of a private community can see searchable content from attachments found in that community. Non-members cannot see searchable content from attachments in the private community, even if those attachments are shared with them in Microsoft Viva Engage.

-   **[Configure Microsoft Viva Engage for external content indexing](../task/configure-microsoft-viva-engage-external-content-indexing.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft Viva Engage external content connector to access your Microsoft Viva Engage source system.
-   **[Create a Microsoft Viva Engage external content connector](../task/create-ext-cont-connector-microsoft-viva-engage.md)**  
Create an external content connector to retrieve searchable content and security principals from your Microsoft Viva Engage source system.
-   **[Configure crawl settings for a Microsoft Viva Engage external content connector](../task/configure-crawl-settings-microsoft-viva-engage-external-content-connector.md)**  
Specify the communities you want your Microsoft Viva Engage external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

