---
title: Adobe Acrobat Sign external content connector
description: The Adobe Acrobat Sign external content connector retrieves documents from agreements in your Adobe Acrobat Sign source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/adobe-acrobat-sign-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Adobe Acrobat Sign external content connector

The Adobe Acrobat Sign external content connector retrieves documents from agreements in your Adobe Acrobat Sign source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Configure Adobe Acrobat Sign for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-adobe-acrobat-sign-external-content-indexing.md)**  
Create and authorize an OAuth 2.0 application in Adobe Acrobat Sign to allow the Adobe Acrobat Sign external content connector to access your Adobe Acrobat Sign source system.
-   **[Create an Adobe Acrobat Sign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-adobe-acrobat-sign.md)**  
Create an external content connector to retrieve searchable content and security principals from your Adobe Acrobat Sign source system.
-   **[Configure crawl settings for an Adobe Acrobat Sign external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-adobe-acrobat-sign-external-content-connector.md)**  
Specify the agreement documents you want your Adobe Acrobat Sign external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)

