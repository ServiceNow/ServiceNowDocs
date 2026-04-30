---
title: Atlassian Jira Cloud external content connector
description: The Atlassian Jira Cloud external content connector retrieves work items and attachments from projects in your Atlassian Jira Cloud source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-04"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Atlassian Jira Cloud external content connector

The Atlassian Jira Cloud external content connector retrieves work items and attachments from projects in your Atlassian Jira Cloud source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure a connector user in Atlassian Jira Cloud](../task/configure-connector-user-jira-cloud.md)**  
Create a user and group in your Atlassian Jira Cloud tenant with access and permissions required by the Atlassian Jira Cloud external content connector. The connector runs as this user when accessing data from your tenant.
-   **[Configure Atlassian Jira Cloud for external content indexing](../task/cfg-src-sys-settings-jira-ext-cont-connector.md)**  
Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Jira Cloud external content connector to crawl projects and security principals in your Atlassian Jira Cloud source system.
-   **[Create an Atlassian Jira Cloud external content connector](../task/create-ext-cont-connector-jira.md)**  
Create an external content connector to retrieve searchable content and security principals from your Atlassian Jira Cloud source system.
-   **[Configure crawl settings for an Atlassian Jira Cloud external content connector](../task/configure-crawl-settings-jira-ext-cont-connector.md)**  
Specify the projects you want your Atlassian Jira Cloud external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

