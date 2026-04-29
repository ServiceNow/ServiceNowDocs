---
title: Smartsheet external content connector
description: The Smartsheet external content connector retrieves sheets from workspaces in your Smartsheet source system and makes their content and metadata searchable in AI Search applications.
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

# Smartsheet external content connector

The Smartsheet external content connector retrieves sheets from workspaces in your Smartsheet source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Smartsheet for external content indexing](../task/configure-smartsheet-external-content-indexing.md)**  
Generate an API key in Smartsheet to allow the Smartsheet external content connector to access your Smartsheet source system.
-   **[Create a Smartsheet external content connector](../task/create-ext-cont-connector-smartsheet.md)**  
Create an external content connector to retrieve searchable content and security principals from your Smartsheet source system.
-   **[Configure crawl settings for a Smartsheet external content connector](../task/configure-crawl-settings-smartsheet-external-content-connector.md)**  
Specify the items you want your Smartsheet external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

