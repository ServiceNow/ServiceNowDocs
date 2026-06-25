---
title: Microsoft Teams external content connector
description: The Microsoft Teams external content connector retrieves conversations and attachments from teams in your Microsoft Teams source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/microsoft-teams-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Microsoft Teams external content connector

The Microsoft Teams external content connector retrieves conversations and attachments from teams in your Microsoft Teams source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Create a public/private key pair for the Microsoft Teams external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/gen-cert-msteams-ext-cont-connector.md)**  
Generate a public/private key pair for the Microsoft Teams external content connector. Extract the public key as a DER-encoded binary X.509 format certificate for use in configuring API access for the connector in the Microsoft Entra admin center.
-   **[Configure Microsoft Teams for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-src-sys-settings-msteams-ext-cont-connector.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft Teams external content connector to access your Microsoft Teams source system.
-   **[Create a Microsoft Teams external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-msteams.md)**  
Create an external content connector to retrieve searchable content and security principals from your Microsoft Teams source system.
-   **[Configure crawl settings for a Microsoft Teams external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-msteams-ext-cont-connector.md)**  
Specify the teams you want your Microsoft Teams external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)

