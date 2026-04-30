---
title: Zoom external content connector
description: The Zoom external content connector retrieves webinars and meetings from your Zoom source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-07"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zoom external content connector

The Zoom external content connector retrieves webinars and meetings from your Zoom source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Zoom for external content indexing](../task/configure-zoom-external-content-indexing.md)**  
Create and activate a Server-to-Server OAuth app in the Zoom App Marketplace to allow the Zoom external content connector to access your Zoom source system.
-   **[Create a Zoom external content connector](../task/create-ext-cont-connector-zoom.md)**  
Create an external content connector to retrieve searchable content and security principals from your Zoom source system.
-   **[Configure crawl settings for a Zoom external content connector](../task/configure-crawl-settings-zoom-external-content-connector.md)**  
Specify the content types you want your Zoom external content connector to retrieve.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

