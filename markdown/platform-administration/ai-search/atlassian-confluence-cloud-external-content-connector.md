---
title: Atlassian Confluence Cloud external content connector
description: The Atlassian Confluence Cloud external content connector retrieves pages and attachments from spaces in your Atlassian Confluence Cloud source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-01-16"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Atlassian Confluence Cloud external content connector

The Atlassian Confluence Cloud external content connector retrieves pages and attachments from spaces in your Atlassian Confluence Cloud source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Note:**

When running crawls for the Atlassian Confluence Cloud external content connector, always run your content crawl first, before running a user permission crawl. If you run the user permission crawl before the content crawl completes, some Confluence Cloud content may not be searchable.

The connector automatically runs a user permission crawl after its first full content crawl completes. It also automatically runs a user permission crawl if you modify its connection settings and then run a complete full content crawl. In all other cases, you need to run or schedule the user permission crawl so that it starts after your latest content crawl has completed.

## Role-Based Access Control \(RBAC\) beta support

The Atlassian Confluence Cloud external content connector only offers limited support for the Role-Based Access Control \(RBAC\) feature that's available in beta in Atlassian Confluence Cloud.

-   The connector maps user and group read permissions assigned via RBAC roles just as it does for non-RBAC read permissions.
-   The connector ignores user and group read permissions assigned via RBAC user classes. These include the anonymous permission assigned via the anonymous user class. If RBAC user class permissions are the only read permissions assigned on a page or attachment, the content from that page or attachment will not be searchable in AI Search applications.

Atlassian recommends enabling the RBAC feature for testing in a non-production Atlassian Confluence Cloud environment. Connector admins should test the connector's behavior with RBAC in non-production ServiceNow AI Platform® instances before deploying to production.

-   **[Estimate document volume for Atlassian Confluence Cloud](../task/estimate-doc-volume-acc.md)**  
Estimate the number of documents included in your Atlassian Confluence Cloud source system. Use this information to determine crawl scope settings needed for your Atlassian Confluence Cloud external content connector.
-   **[Configure Atlassian Confluence Cloud for external content indexing](../task/cfg-conf-cc-ext-cont-connector.md)**  
Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Confluence Cloud external content connector to crawl spaces and security principals in your Atlassian Confluence Cloud source system.
-   **[Create an Atlassian Confluence Cloud external content connector](../task/create-ext-cont-connector-acc.md)**  
Create an external content connector to retrieve searchable content and security principals from your Atlassian Confluence Cloud source system.
-   **[Configure crawl settings for an Atlassian Confluence Cloud external content connector](../task/configure-crawl-settings-cc-ext-cont-connector.md)**  
Specify the spaces you want your Atlassian Confluence Cloud external content connector to crawl. Define inclusion or exclusion filters for file extensions to dictate the types of documents the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

