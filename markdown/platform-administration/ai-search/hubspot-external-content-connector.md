---
title: HubSpot external content connector
description: The HubSpot external content connector retrieves tickets and notes from your HubSpot source system and makes their content and metadata searchable in AI Search applications.
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

# HubSpot external content connector

The HubSpot external content connector retrieves tickets and notes from your HubSpot source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Note:** The HubSpot API provides only limited information about document permissions. As a result, the external content connector may reindex a significant number of crawled documents when you add or remove HubSpot users or members of HubSpot groups. In extreme cases, adding a single user or updating membership for a single group can trigger an update of all crawled HubSpot documents in the AI Search index.

-   **[Configure HubSpot for external content indexing](../task/configure-hubspot-external-content-indexing.md)**  
Create and authorize a legacy public app in HubSpot to allow the HubSpot external content connector to access your HubSpot source system.
-   **[Create a HubSpot external content connector](../task/create-ext-cont-connector-hubspot.md)**  
Create an external content connector to retrieve searchable content and security principals from your HubSpot source system.
-   **[Configure crawl settings for a HubSpot external content connector](../task/configure-crawl-settings-hubspot-external-content-connector.md)**  
Specify the tickets you want your HubSpot external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

