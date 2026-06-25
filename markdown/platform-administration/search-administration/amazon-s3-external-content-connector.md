---
title: Amazon S3 external content connector
description: The Amazon S3 external content connector retrieves files from buckets in your Amazon S3 source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/amazon-s3-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Amazon S3 external content connector

The Amazon S3 external content connector retrieves files from buckets in your Amazon S3 source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Important:** All content the connector retrieves from your Amazon S3 buckets is treated as public content, searchable by everyone who has access to your configured AI Search experience.

-   **[Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md)**  
Create an Identity and Access Management \(IAM\) user in the Amazon Web Services \(AWS\) Management Console. Define an access key for your new user to allow the Amazon S3 external content connector to access your Amazon S3 source system.
-   **[Create an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-amazon-s3.md)**  
Create an external content connector to retrieve searchable content from your Amazon S3 source system.
-   **[Configure crawl settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-amazon-s3-external-content-connector.md)**  
Define inclusion and exclusion filters to specify the buckets and file types you want your Amazon S3 external content connector to retrieve when running content crawls.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

