---
title: Trello external content connector
description: The Trello external content connector retrieves boards that are accessible to all users in your Trello source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Trello external content connector

The Trello external content connector retrieves boards that are accessible to all users in your Trello source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Note:** The Trello external content connector only retrieves searchable content and metadata from boards that can be accessed by all users in your Trello enterprise. It does not retrieve content and metadata from secure boards.

-   **[Configure Trello for external content indexing](../task/configure-trello-external-content-indexing.md)**  
Create and authorize a Power-Up in the Trello Power-Up Admin Portal to allow the Trello external content connector to access your Trello source system.
-   **[Create a Trello external content connector](../task/create-ext-cont-connector-trello.md)**  
Create an external content connector to retrieve searchable content from your Trello source system.
-   **[Configure crawl settings for a Trello external content connector](../task/configure-crawl-settings-trello-external-content-connector.md)**  
Specify the workspaces you want your Trello external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

