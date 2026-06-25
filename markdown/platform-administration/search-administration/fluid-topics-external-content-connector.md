---
title: Fluid Topics external content connector
description: The Fluid Topics external content connector retrieves Topics, Articles, Publications, and associated content pages delivered through portals in your Fluid Topics source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/fluid-topics-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Fluid Topics external content connector

The Fluid Topics external content connector retrieves Topics, Articles, Publications, and associated content pages delivered through portals in your Fluid Topics source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Note:** Default retrieval limits in the Fluid Topics API may prevent the connector from indexing all of your source system content. To learn about these retrieval limits and how you can request to have them increased, see [Request limits in Fluid Topics Knowledge Hub web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/fluid-topics-api-request-limits.md).

-   **[Configure Fluid Topics for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-fluid-topics-external-content-indexing.md)**  
Generate an API key in your Fluid Topics tenant to allow the Fluid Topics external content connector to access your Fluid Topics source system.
-   **[Create a Fluid Topics external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-fluid-topics.md)**  
Create an external content connector to retrieve searchable content and security principals from your Fluid Topics source system.
-   **[Configure crawl settings for a Fluid Topics external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-fluid-topics-external-content-connector.md)**  
Specify restrictions on source content status, visibility, category/collection, tags, languages, and modification dates for the Fluid Topics external content connector's content crawls. Define inclusion or exclusion filters to limit the content the crawl retrieves and feeds to AI Search for indexing.
-   **[Request limits in Fluid Topics Knowledge Hub web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/fluid-topics-api-request-limits.md)**  
By default, the Fluid Topics API limits the number of maps, topics, and unstructured documents retrieved by requests to Knowledge Hub web services. These default limits may prevent the Fluid Topics external content connector from indexing all of your source system content. To request increases to these limits, open a ticket in the Fluid Topics Help Center.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)

