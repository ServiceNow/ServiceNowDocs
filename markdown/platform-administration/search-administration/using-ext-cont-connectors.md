---
title: Crawling content with External Content Connectors
description: Search administrators can use the External Content Connectors application to run one-time document and user permission crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/using-ext-cont-connectors.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Crawling content with External Content Connectors

Search administrators can use the External Content Connectors application to run one-time document and user permission crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.

To access the External Content Connectors application, navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

On the application's main page, the Connectors list shows your external content connectors with their source, status, count of documents retrieved, last content crawl start date and time, and failed crawl count.

**Note:** Beginning in External Content Connectors 6.0, crawls that time out due to connectivity issues during their run are automatically resumed when connectivity resumes.

-   **[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)**  
Retrieve searchable content and metadata from your source system with a content crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
-   **[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)**  
Retrieve security principals from your source system with a user permission crawl. Run the crawl as a one-time task or schedule it to run on a recurring basis.
-   **[Cancel a running external content connector crawl](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cancel-ext-cont-connector-crawl.md)**  
Cancel a running crawl for an external content connector to prevent the connector from retrieving and feeding additional documents or access permissions to AI Search for indexing.
-   **[Refresh content for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/refresh-content-external-content-connector.md)**  
Refresh searchable content and metadata, including unchanged items, for an external content connector by running a one-time full or partial content crawl.

**Parent Topic:**[External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/ext-cont-connectors-landing-page.md)

