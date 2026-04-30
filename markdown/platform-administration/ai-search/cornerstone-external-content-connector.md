---
title: Cornerstone external content connector
description: The Cornerstone external content connector retrieves Catalogue and Learning objects from organization units in your Cornerstone Learning Management System \(LMS\) and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-01-13"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Cornerstone external content connector

The Cornerstone external content connector retrieves Catalogue and Learning objects from organization units in your Cornerstone Learning Management System \(LMS\) and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Cornerstone for external content indexing](../task/configure-cornerstone-external-content-indexing.md)**  
Create and authorize an OAuth 2.0 application in the Cornerstone  to allow the Cornerstone external content connector to access your Cornerstone source system.
-   **[Create a Cornerstone external content connector](../task/create-ext-cont-connector-cornerstone.md)**  
Create an external content connector to retrieve searchable content from your Cornerstone source system.
-   **[Configure crawl settings for a Cornerstone external content connector](../task/configure-crawl-settings-cornerstone-external-content-connector.md)**  
Specify the organization units you want your Cornerstone external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

