---
title: Notion external content connector
description: The Notion external content connector retrieves pages and files from your Notion source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Notion external content connector

The Notion external content connector retrieves pages and files from your Notion source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Important:** The Notion external content connector doesn't retrieve per-user permissions when running content crawls. All content indexed by the connector is searchable by all mapped users who have access to your configured AI Search experience.

-   **[Configure Notion for external content indexing](../task/configure-notion-external-content-indexing.md)**  
Create and authorize an internal integration in the Notion integrations dashboard to allow the Notion external content connector to access your Notion source system.
-   **[Create a Notion external content connector](../task/create-ext-cont-connector-notion.md)**  
Create an external content connector to retrieve searchable content and security principals from your Notion source system.
-   **[Configure crawl settings for a Notion external content connector](../task/configure-crawl-settings-notion-external-content-connector.md)**  
Specify the pages you want your Notion external content connector to crawl and feed to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

