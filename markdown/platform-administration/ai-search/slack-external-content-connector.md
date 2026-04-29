---
title: Slack external content connector
description: The Slack external content connector retrieves messages and attachments from public channels in your Slack source system and makes their content and metadata searchable in AI Search applications.
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

# Slack external content connector

The Slack external content connector retrieves messages and attachments from public channels in your Slack source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Slack for external content indexing](../task/cfg-src-sys-settings-slack-ext-cont-connector.md)**  
Create a Slack API application to allow the Slack external content connector to crawl public channels in your Slack source system.
-   **[Create a Slack external content connector](../task/create-ext-cont-connector-slack.md)**  
Create an external content connector to retrieve searchable content from public channels in your Slack source system.
-   **[Configure crawl settings for a Slack external content connector](../task/configure-crawl-settings-slack-ext-cont-connector.md)**  
Specify the public channels you want your Slack external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

