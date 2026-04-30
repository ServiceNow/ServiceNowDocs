---
title: Cornerstone external content connector
description: The Cornerstone external content connector retrieves Catalogue and Learning objects from your Cornerstone Learning Management System \(LMS\) and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-12-18"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Cornerstone external content connector

The Cornerstone external content connector retrieves Catalogue and Learning objects from your Cornerstone Learning Management System \(LMS\) and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Cornerstone for external content indexing](configure-cornerstone-external-content-indexing.md)**  
Create and authorize an OAuth 2.0 application in the Cornerstone  to allow the Cornerstone external content connector to access your Cornerstone source system.
-   **[Create a Cornerstone external content connector](create-ext-cont-connector-cornerstone.md)**  
Create an external content connector to retrieve searchable content from your Cornerstone source system.
-   **[Configure crawl settings for a Cornerstone external content connector](configure-crawl-settings-cornerstone-external-content-connector.md)**  
Specify the  you want your Cornerstone external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

