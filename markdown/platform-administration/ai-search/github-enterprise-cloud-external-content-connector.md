---
title: GitHub Enterprise Cloud external content connector
description: The GitHub Enterprise Cloud external content connector retrieves commits, issues, and pull requests from public and internal repositories in your GitHub Enterprise Cloud source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# GitHub Enterprise Cloud external content connector

The GitHub Enterprise Cloud external content connector retrieves commits, issues, and pull requests from public and internal repositories in your GitHub Enterprise Cloud source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure GitHub Enterprise Cloud for external content indexing](../task/configure-github-enterprise-cloud-external-content-indexing.md)**  
Create and authorize a GitHub App to allow the GitHub Enterprise Cloud external content connector to access your GitHub Enterprise Cloud content.
-   **[Create a GitHub Enterprise Cloud external content connector](../task/create-ext-cont-connector-github-enterprise-cloud.md)**  
Create an external content connector to retrieve searchable content and security principals from your GitHub Enterprise Cloud source system.
-   **[Configure crawl settings for a GitHub Enterprise Cloud external content connector](../task/configure-crawl-settings-github-enterprise-cloud-external-content-connector.md)**  
Specify the public and internal repositories you want your GitHub Enterprise Cloud external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

