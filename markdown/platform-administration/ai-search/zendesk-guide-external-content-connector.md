---
title: Zendesk Guide external content connector
description: The Zendesk Guide external content connector retrieves articles and attachments from knowledge bases in your Zendesk Guide source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-04"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Zendesk Guide external content connector

The Zendesk Guide external content connector retrieves articles and attachments from knowledge bases in your Zendesk Guide source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Limitations for the Zendesk Guide external content connector

Search results from Guide Media attachments open normally in new browser tabs when selected from the search results page. Selecting a search result for a non-Guide Media attachment may open the attachment in the same browser tab or may prompt you to download it, depending on your browser settings. To learn more about Guide Media attachments, see [https://developer.zendesk.com/api-reference/help\_center/help-center-api/guide\_medias/](https://developer.zendesk.com/api-reference/help_center/help-center-api/guide_medias/).

-   **[Configure Zendesk for external content indexing](../task/configure-zendesk-guide-external-content-indexing.md)**  
Create an API token in Zendesk Admin Center to allow the Zendesk Guide external content connector to access your Zendesk source system.
-   **[Create a Zendesk Guide external content connector](../task/create-ext-cont-connector-zendesk-guide.md)**  
Create an external content connector to retrieve searchable content and security principals from your Zendesk source system.
-   **[Configure crawl settings for a Zendesk Guide external crawl connector](../task/configure-crawl-settings-zendesk-guide-external-crawl-connector.md)**  
Specify the article locales and attachment file types you want your Zendesk Guide external content connector to crawl when running content crawls. Define inclusion or exclusion filters for domains to restrict the set of users the crawl retrieves access permissions for when running user permission crawls.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

