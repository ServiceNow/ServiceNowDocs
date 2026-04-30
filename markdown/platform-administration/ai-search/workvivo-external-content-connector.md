---
title: Workvivo external content connector
description: The Workvivo external content connector retrieves articles, comments, documents, events, kudos, pages, and updates from your Workvivo source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-05"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Workvivo external content connector

The Workvivo external content connector retrieves articles, comments, documents, events, kudos, pages, and updates from your Workvivo source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Workvivo for external content indexing](../task/configure-workvivo-external-content-indexing.md)**  
Create and authorize a new application in your Workvivo instance to allow the Workvivo external content connector to access your source system and content.
-   **[Create a Workvivo external content connector](../task/create-ext-cont-connector-workvivo.md)**  
Create an external content connector to retrieve searchable content and security principals from your Workvivo source system.
-   **[Configure crawl settings for a Workvivo external content connector](../task/configure-crawl-settings-workvivo-external-content-connector.md)**  
Define inclusion or exclusion filters to control the attachment file types the Workvivo external content connector retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

