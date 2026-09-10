---
title: Google Drive external content connector
description: The Google Drive external content connector retrieves files and attachments from eligible shared drives in your Google Drive source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/google-drive-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Google Drive external content connector

The Google Drive external content connector retrieves files and attachments from eligible shared drives in your Google Drive source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Drive eligibility

To be eligible for crawling, a shared drive must be accessible by at least one member who is a user in the Directory and who has the Manager role \(or is a member of a group with the Manager role\). To learn more about the Directory, see [https://support.google.com/a/answer/1628009](https://support.google.com/a/answer/1628009). For details on the Manager role, see [https://support.google.com/a/users/answer/12380484](https://support.google.com/a/users/answer/12380484).

## Delta content crawls

The Google Drive external content connector supports the ability to run delta content crawls in between full content crawls. Unlike full content crawls, delta content crawls only examine, retrieve, and index newly added, changed, or deleted items from your shared drives. By ignoring unchanged items, delta content crawling can significantly reduce the time taken to crawl content from the source system. This means you can refresh your searchable content more often by running delta content crawls between your scheduled full or partial content crawls.

To learn more about delta content crawls, see [Delta content crawls for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/delta-content-crawls-external-content-connectors.md). For details on the activation procedure for delta content crawls, see [Activate delta content crawling for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/activate-delta-content-crawling-external-content-connector.md).

**Note:** Delta content crawls don't replace full content crawls. They're supplemental crawls that enable you to refresh searchable content more frequently in between full content crawls.

Delta content crawls for the Google Drive external content connector have the following limitations.

-   Delta content crawls can't detect membership changes for Google Drive shared drives. As a result, user access permissions to files and attachments from your shared drives may be out of sync until the connector completes its next full content crawl.
-   If members with the Manager role are removed from shared drives, future delta content crawls may not retrieve changed items from those drives. As a result, searchable content may be out of sync with the source system until the connector completes its next full content crawl.

-   **[Configure Google Drive for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/cfg-gcloud-settings-gdrive-ext-cont-connector.md)**  
Enable the Google Drive and Admin SDK APIs and create a Google Cloud service account to allow the Google Drive external content connector to crawl eligible shared drives and security principals in your Google Drive source system.
-   **[Create a Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-gdrive.md)**  
Create an external content connector to retrieve searchable content and security principals from your Google Drive source system.
-   **[Configure crawl settings for a Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-gdrive-ext-cont-connector.md)**  
Specify the shared drives you want your Google Drive external content connector to crawl. Define inclusion or exclusion filters to dictate the types of content the crawl retrieves and feeds to AI Search for indexing.
-   **[Filter content by label for a Google Drive external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/filter-content-label-google-drive-external-content-connector.md)**  
Configure a label filter for your Google Drive external content connector. The connector only retrieves content that has one or more of your specified label values applied.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)

