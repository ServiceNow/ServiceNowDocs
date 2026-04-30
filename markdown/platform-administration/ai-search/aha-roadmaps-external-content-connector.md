---
title: Aha! Roadmaps external content connector
description: The Aha! Roadmaps external content connector retrieves Features, Goals, Ideas, Notes, and Releases from workspaces in your Aha! Roadmaps source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-01-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Aha! Roadmaps external content connector

The Aha! Roadmaps external content connector retrieves Features, Goals, Ideas, Notes, and Releases from workspaces in your Aha! Roadmaps source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Aha! Roadmaps for external content indexing](../task/configure-aha-roadmaps-external-content-indexing.md)**  
Generate an API key in Aha! Roadmaps to allow the Aha! Roadmaps external content connector to access content from your workspaces.
-   **[Create an Aha! Roadmaps external content connector](../task/create-ext-cont-connector-aha-roadmaps.md)**  
Create an external content connector to retrieve searchable content and security principals from your Aha! Roadmaps source system.
-   **[Configure crawl settings for an Aha! Roadmaps external content connector](../task/configure-crawl-settings-aha-roadmaps-external-content-connector.md)**  
Specify the products you want your Aha! Roadmaps external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

