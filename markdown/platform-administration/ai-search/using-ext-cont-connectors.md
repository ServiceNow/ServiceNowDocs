---
title: Crawling content with External Content Connectors
description: Search administrators can use the External Content Connectors application to run one-time document and user mapping crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-01"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Crawling content with External Content Connectors

Search administrators can use the External Content Connectors application to run one-time document and user mapping crawls on demand. They can review connector-specific crawl history and analytics and details of user and group mappings retrieved from external data sources.

To access the External Content Connectors application, navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

On the application's main page, the Connectors list shows your external content connectors with their source, status, count of documents retrieved, last document crawl start date and time, and failed crawl count.

-   **[Define a crawl schedule for an external content connector](../task/define-schedule-ext-cont-connector.md)**  
Keep your search index up to date by scheduling regular document and user mapping crawls for your external content connector. Scheduled crawls can run daily or on selected days of the week, starting at a time that you specify.
-   **[Run a one-time full or partial document crawl for an external content connector](../task/run-doc-crawl-ext-cont-connector.md)**  
Retrieve document content and metadata from all or part of your external content connector's data source on demand. A document crawl sends retrieved content and metadata to AI Search for indexing, making them available to users of your AI Search applications.
-   **[Run a one-time user mapping crawl for an external content connector](../task/run-umap-crawl-ext-cont-connector.md)**  
Retrieve users and group access permissions from your external content connector's data source on demand. A user mapping crawl maps retrieved user and group permissions to your ServiceNow AI Platform® users to facilitate content security in your AI Search applications.
-   **[Cancel a running external content connector crawl](../task/cancel-ext-cont-connector-crawl.md)**  
Cancel a running crawl for an external content connector to prevent the connector from retrieving and feeding additional documents or access permissions to AI Search for indexing.
-   **[Rename an external content connector](../task/rename-ext-cont-connector.md)**  
Change the name of an existing external content connector.
-   **[Deactivate, reactivate, or delete an external content connector](../task/deactivate-del-ext-cont-connector.md)**  
Deactivate an external connector to pause its scheduled crawls while retaining all of the content and metadata that it has already crawled. Reactivate a deactivated connector to resume its scheduled crawls. Delete an external content connector to remove the connector's definition along with all content and metadata that it has crawled.

**Parent Topic:**[External Content Connectors](../reference/ext-cont-connectors-landing-page.md)

