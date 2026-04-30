---
title: Adobe Experience Manager as a Cloud Service external content connector
description: The Adobe Experience Manager as a Cloud Service external content connector retrieves assets from nodes in your Adobe Experience Manager as a Cloud Service source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-02"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Adobe Experience Manager as a Cloud Service external content connector

The Adobe Experience Manager as a Cloud Service external content connector retrieves assets from nodes in your Adobe Experience Manager as a Cloud Service source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Limitations

The Adobe Experience Manager as a Cloud Service external content connector only crawls assets. It doesn't crawl web page content or social content such as reviews, blog posts, or comments. All asset content retrieved by the connector is treated as public, meaning that it's searchable by all users with access to your configured AI Search experience.

-   **[Configure Adobe Experience Manager as a Cloud Service for external content indexing](../task/configure-adobe-expmgr-cs-external-content-indexing.md)**  
Create Service Credentials in Adobe Cloud Manager to allow the Adobe Experience Manager as a Cloud Service external content connector to access nodes and assets in your source system.
-   **[Create an Adobe Experience Manager as a Cloud Service external content connector](../task/create-ext-cont-connector-adobe-expmgr-cs.md)**  
Create an external content connector to retrieve searchable content from your Adobe Experience Manager as a Cloud Service source system.
-   **[Configure crawl settings for an Adobe Experience Manager as a Cloud Service external content connector](../task/configure-crawl-settings-adobe-expmgr-cs-external-content-connector.md)**  
Specify the nodes you want your Adobe Experience Manager as a Cloud Service external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

