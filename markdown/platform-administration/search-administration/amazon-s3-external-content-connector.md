---
title: Amazon S3 external content connector
description: The Amazon S3 external content connector retrieves files from buckets in your Amazon S3 source system and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/amazon-s3-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Amazon S3 external content connector

The Amazon S3 external content connector retrieves files from buckets in your Amazon S3 source system and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to update searchable content and metadata from your source system. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Important:** All content the connector retrieves from your Amazon S3 buckets is treated as public content, searchable by everyone who has access to your configured AI Search experience.

## Advanced connection settings

You can optionally specify the following connection settings for an Amazon S3 external content connector.

-   The AWS region for the connector.

    **Note:** For regulatory market compliance, specify a regulated market AWS region, such as `us-gov-east-1` or `us-gov-west-1`.

-   Automatic selection or manual specification of the Amazon S3 endpoint used for connection and authentication operations. For AWS regions that offer endpoints compliant with FIPS \(the Federal Information Processing Standards\), you can optionally restrict automatic selection to those endpoints.
-   A list of Amazon S3 buckets that the connector can access content from. If you leave this list empty, the connector finds buckets using auto-discovery. If you populate this list, the connector only accesses content from the specified buckets.

For the full list of supported Amazon S3 endpoints and regions, see the [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html) Amazon documentation resource.

-   **[Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md)**  
Create an Identity and Access Management \(IAM\) user in the Amazon Web Services \(AWS\) Management Console. Define an access key for your new user to allow the Amazon S3 external content connector to access your Amazon S3 source system.
-   **[Create an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-amazon-s3.md)**  
Create an external content connector to retrieve searchable content from your Amazon S3 source system.
-   **[Configure crawl settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-crawl-settings-amazon-s3-external-content-connector.md)**  
Define inclusion and exclusion filters to specify the buckets and file types you want your Amazon S3 external content connector to retrieve when running content crawls.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

