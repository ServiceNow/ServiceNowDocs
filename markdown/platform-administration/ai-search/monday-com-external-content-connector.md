---
title: monday.com external content connector
description: The monday.com external content connector crawls workspaces, boards, board items, and workdocs from your monday.com source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-15"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# monday.com external content connector

The monday.com external content connector crawls workspaces, boards, board items, and workdocs from your monday.com source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure monday.com for external content indexing](../task/configure-monday-com-external-content-indexing.md)**  
Obtain an API token for a monday.com user account with admin privileges to allow the monday.com external content connector to access searchable content and metadata from your monday.com source system.
-   **[Create a monday.com external content connector](../task/create-ext-cont-connector-monday-com.md)**  
Create an external content connector to retrieve searchable content and security principals from your monday.com source system.
-   **[Configure crawl settings for a monday.com external content connector](../task/configure-crawl-settings-monday-com-external-content-connector.md)**  
Specify the workspaces you want your monday.com external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

