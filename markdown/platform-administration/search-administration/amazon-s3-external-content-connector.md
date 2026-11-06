---
title: Amazon S3 external content connector
description: The Amazon S3 external content connector makes content and metadata from your Amazon S3 buckets searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/amazon-s3-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Amazon S3 external content connector

The Amazon S3 external content connector makes content and metadata from your Amazon S3 buckets searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

## Advanced connection settings

You can optionally specify the following connection settings for an Amazon S3 external content connector.

-   The AWS region for the connector.

    **Note:** For regulatory market compliance, specify a regulated market AWS region, such as `us-gov-east-1` or `us-gov-west-1`.

-   Automatic selection or manual specification of the Amazon S3 endpoint used for connection and authentication operations. For AWS regions that offer endpoints compliant with the Federal Information Processing Standards \(FIPS\), you can optionally restrict automatic selection to those endpoints.
-   A list of Amazon S3 buckets that the connector can access content from. If you leave this list empty, the connector finds buckets using auto-discovery. If you populate this list, the connector only accesses content from the specified buckets.

For the full list of supported Amazon S3 endpoints and regions, see the [Amazon Simple Storage Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/s3.html) Amazon documentation resource.

-   **[Configure Amazon S3 for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-external-content-indexing.md)**  
Create an Identity and Access Management \(IAM\) user and access key that the Amazon S3 external content connector uses to access your Amazon S3 source system.
-   **[Create an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-ext-cont-connector-amazon-s3.md)**  
Create an external content connector to retrieve searchable content from your Amazon S3 source system.
-   **[Configure crawl settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-crawl-settings-amazon-s3-external-content-connector.md)**  
Define inclusion and exclusion filters to specify the buckets and file types for your Amazon S3 external content connector to retrieve during content crawls.
-   **[Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-permission-modes-external-content-connector.md)**  
The Amazon S3 external content connector offers multiple permission modes to control which users can see its crawled content items in AI Search applications.
-   **[Configure permission mode and user mapping settings for an Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-amazon-s3-permission-settings-external-content-connector.md)**  
Select the permission mode that controls which users can see content crawled by an Amazon S3 external content connector, and specify user mapping if needed.
-   **[Amazon S3 bucket policy elements supported by the external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-bucket-policy-support-external-content-connector.md)**  
In a standard user permission crawl, the Amazon S3 connector evaluates only the policy elements listed here. It doesn't index content items with policy statements that use other elements.
-   **[AWS permissions required for Amazon S3 external content connector permission modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/amazon-s3-required-permissions-external-content-connector.md)**  
The Identity and Access Management \(IAM\) user for an Amazon S3 external content connector requires Amazon S3 and IAM permissions that depend on the permission mode.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)

