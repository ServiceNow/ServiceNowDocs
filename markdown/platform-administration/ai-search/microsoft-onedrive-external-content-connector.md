---
title: Microsoft OneDrive external content connector
description: The Microsoft OneDrive external content connector retrieves files from individual drives in your Microsoft OneDrive source system and makes their content and metadata searchable in AI Search applications.
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

# Microsoft OneDrive external content connector

The Microsoft OneDrive external content connector retrieves files from individual drives in your Microsoft OneDrive source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Create a public/private key pair for the Microsoft OneDrive external content connector](../task/gen-cert-msod-ext-cont-connector.md)**  
Generate a public/private key pair for the Microsoft OneDrive external content connector. Extract the public key as a DER-encoded binary X.509 format certificate for use in configuring API access for the connector in the Microsoft Entra admin center.
-   **[Configure Microsoft OneDrive for external content indexing](../task/configure-microsoft-onedrive-external-content-indexing.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft OneDrive external content connector to access your Microsoft OneDrive source system.
-   **[Create a Microsoft OneDrive external content connector](../task/create-ext-cont-connector-microsoft-onedrive.md)**  
Create an external content connector to retrieve searchable content and security principals from your Microsoft OneDrive source system.
-   **[Configure crawl settings for a Microsoft OneDrive external content connector](../task/configure-crawl-settings-microsoft-onedrive-external-content-connector.md)**  
Specify the individual drives you want your Microsoft OneDrive external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

