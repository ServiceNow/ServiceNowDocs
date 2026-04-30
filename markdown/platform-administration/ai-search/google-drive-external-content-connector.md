---
title: Google Drive external content connector
description: The Google Drive external content connector retrieves files and attachments from eligible shared drives in your Google Drive source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Google Drive external content connector

The Google Drive external content connector retrieves files and attachments from eligible shared drives in your Google Drive source system and makes their content and metadata searchable in AI Search applications.

Search administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Drive eligibility

To be eligible for crawling, a shared drive must be accessible by at least one member who is a user in the Directory and who has the Manager role \(or is a member of a group with the Manager role\). To learn more about the Directory, see [https://support.google.com/a/answer/1628009](https://support.google.com/a/answer/1628009). For details on the Manager role, see [https://support.google.com/a/users/answer/12380484](https://support.google.com/a/users/answer/12380484).

-   **[Configure Google Drive for external content indexing](../task/cfg-gcloud-settings-gdrive-ext-cont-connector.md)**  
Enable the Google Drive and Admin SDK APIs and create a Google Cloud service account to allow the Google Drive external content connector to crawl eligible shared drives and security principals in your Google Drive source system.
-   **[Create a Google Drive external content connector](../task/create-ext-cont-connector-gdrive.md)**  
Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.
-   **[Configure crawl settings for a Google Drive external content connector](../task/configure-crawl-settings-gdrive-ext-cont-connector.md)**  
Specify the shared drives you want your Google Drive external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

