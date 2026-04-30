---
title: Crawling content with External Content Connectors
description: Search administrators can use the External Content Connectors application to run one-time document and user permission crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-02-20"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Crawling content with External Content Connectors

Search administrators can use the External Content Connectors application to run one-time document and user permission crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.

To access the External Content Connectors application, navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

On the application's main page, the Connectors list shows your external content connectors with their source, status, count of documents retrieved, last content crawl start date and time, and failed crawl count.

**Note:** Beginning in External Content Connectors 6.0, crawls that time out due to connectivity issues during their run are automatically resumed when connectivity resumes.

-   **[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)**  
Retrieve searchable content and metadata from your source system with a content crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
-   **[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)**  
Retrieve security principals from your source system with a user permission crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
-   **[Cancel a running external content connector crawl](../task/cancel-ext-cont-connector-crawl.md)**  
Cancel a running crawl for an external content connector to prevent the connector from retrieving and feeding additional documents or access permissions to AI Search for indexing.
-   **[Refresh content for an external content connector](../task/refresh-content-external-content-connector.md)**  
Refresh searchable content and metadata, including unchanged items, for an external content connector by running a one-time full or partial content crawl.

**Parent Topic:**[External Content Connectors](../reference/ext-cont-connectors-landing-page.md)

