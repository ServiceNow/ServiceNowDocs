---
title: Docusign external content connector
description: The Docusign external content connector retrieves agreements from envelopes in your Docusign source system and makes their content and metadata searchable in AI Search applications.
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

# Docusign external content connector

The Docusign external content connector retrieves agreements from envelopes in your Docusign source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Important:**

The Docusign external content connector doesn’t support the [shared access](https://support.docusign.com/s/document-item?language=en_US&bundleId=oeq1643226594604&topicId=rdu1656546423934.html&_LANG=enus) feature in Docusign. As a result, users in search applications can't see searchable content and metadata from envelopes that they only have shared access to.

-   **[Configure Docusign for external content indexing](../task/configure-docusign-external-content-indexing.md)**  
Create an app and integration key in Docusign to allow the Docusign external content connector to access your source system.
-   **[Create a Docusign external content connector](../task/create-ext-cont-connector-docusign.md)**  
Create an external content connector to retrieve searchable content and security principals from your Docusign source system.
-   **[Configure crawl settings for a Docusign external content connector](../task/configure-crawl-settings-docusign-external-content-connector.md)**  
Define inclusion or exclusion filters to control which agreements you want your Docusign external content connector to make searchable.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

