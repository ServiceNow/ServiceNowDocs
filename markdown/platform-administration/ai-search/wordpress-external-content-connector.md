---
title: WordPress external content connector
description: The WordPress external content connector retrieves pages and blog posts and their attachments from websites in your WordPress source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-14"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# WordPress external content connector

The WordPress external content connector retrieves pages and blog posts and their attachments from websites in your WordPress source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure WordPress for external content indexing](../task/configure-wordpress-external-content-indexing.md)**  
Create an admin user and an application password in your WordPress website to allow the WordPress external content connector to access your WordPress content.
-   **[Create a WordPress external content connector](../task/create-ext-cont-connector-wordpress.md)**  
Create an external content connector to retrieve searchable content and security principals from your WordPress source system.
-   **[Configure crawl settings for a WordPress external content connector](../task/configure-crawl-settings-wordpress-external-content-connector.md)**  
Specify the pages and blog posts you want your WordPress external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

