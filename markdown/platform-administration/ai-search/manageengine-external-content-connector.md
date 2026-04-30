---
title: ManageEngine external content connector
description: The ManageEngine external content connector retrieves public-domain knowledge articles from knowledge bases in your ManageEngine source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-06"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# ManageEngine external content connector

The ManageEngine external content connector retrieves public-domain knowledge articles from knowledge bases in your ManageEngine source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure ManageEngine for external content indexing](../task/configure-manageengine-external-content-indexing.md)**  
Create a server-based OAuth 2.0 client application in the Zoho API console to allow the ManageEngine external content connector to access your ManageEngine source system.
-   **[Create a ManageEngine external content connector](../task/create-ext-cont-connector-manageengine.md)**  
Create an external content connector to retrieve searchable content from your ManageEngine source system.
-   **[Configure crawl settings for a ManageEngine external content connector](../task/configure-crawl-settings-manageengine-external-content-connector.md)**  
Delimit the set of knowledge articles you want your ManageEngine external content connector to retrieve. Define inclusion or exclusion filters to specify which articles the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

