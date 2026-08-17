---
title: Amazon S3 metadata collector
description: The Amazon S3 metadata collector harvests read-only metadata from an AWS S3 account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/amazon-s3-metadata-collector.html
release: australia
topic_type: concept
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [Amazon S3, metadata collector, S3 bucket, S3 object]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Amazon S3 metadata collector

The Amazon S3 metadata collector harvests read-only metadata from an AWS S3 account.

The collector harvests metadata from AWS S3, including buckets, objects, and their associated metadata.

## Authentication supported

The collector supports the following authentication methods. For details, see [Credentials and authentication](https://docs.aws.amazon.com/sdk-for-java/latest/developer-guide/credentials.html) in the AWS documentation.

-   Authentication details supplied through an AWS credentials file
-   Access Key ID and AWS Secret Access Key

## Metadata cataloged

<table id="table-s3-metadata-cataloged"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Bucket

</td><td>

-   ARN \(Amazon Resource Name\)
-   Region
-   Name
-   Version state
-   Creation date
-   ACL \(access control list\) owner ID
-   ACL grantee ID
-   ACL grant permission

</td></tr><tr><td>

Object

</td><td>

-   Key
-   ARN \(Amazon Resource Name\)
-   Region
-   Size
-   Last modified date
-   ACL \(access control list\) owner ID
-   ACL grantee ID
-   ACL grant permission
-   Metadata

</td></tr></tbody>
</table>## Relationships between objects

By default, the harvested metadata includes catalog pages for the following resource types. Each catalog page has a relationship to the other related resource types. If the metadata presentation for this data source has been customized, you might see other resource pages and relationships.

|Resource page|Relationship|
|-------------|------------|
|S3 Bucket|S3 Object|
|S3 Object|S3 Bucket|

## Limits for S3 buckets

The collector has a default limit of 10,000 objects per bucket. If a bucket exceeds this limit, the collector skips the bucket, harvests no metadata for it, and logs a warning message.

To increase the limit beyond the default, set the **--max-resources** parameter in your collector command. The maximum value for this parameter is 10,000,000 \(ten million\). If the total contents across all buckets and objects exceed this limit, the collector stops cataloging additional buckets and logs a warning message.

-   **[Prepare to run the Amazon S3 collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-amazon-s3-collector.md)**  
Create an AWS IAM user with the permissions required for the metadata collector to harvest metadata from Amazon S3 buckets and objects.
-   **[Create an Amazon S3 metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-amazon-s3-metadata-collector.md)**  
Use a metadata collector to import Amazon S3 bucket and object metadata into the data catalog.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)

