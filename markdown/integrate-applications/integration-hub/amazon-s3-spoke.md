---
title: Amazon S3 Spoke
description: Integrate ServiceNow with Amazon S3. Manage buckets, objects, tags, and related ACLs in Amazon S3 from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon S3 Spoke

Integrate ServiceNow with Amazon S3. Manage buckets, objects, tags, and related ACLs in Amazon S3 from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon S3 spoke v1.2.1 is the latest version.

## Supported version

This spoke was built for API version 2010-03-31, but may be compatible with later versions.

## Supported regions

Currently, the spoke does not support the government or federal government regions.

## Spoke requirements

-   User with full access to Amazon S3.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For information about creating and accessing keys, see the [AWS Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-security-credentials.html) documentation.

## Spoke actions

The Amazon S3 spoke provides actions to automate Amazon S3 tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Bucket Management|Create Bucket|Creates a bucket in Amazon S3.|
|Look up Buckets|List Amazon S3 buckets.|
|Object Management|Copy Object|Copies object from source to destination.|
|Delete Object|Deletes specified object from a bucket.|
|Look up Objects by Bucket Stream|Lists the objects in the specified Amazon S3 bucket.|
|Download S3 Object to ServiceNow Record|Downloads the requested object from Amazon S3 and attaches it to a record in ServiceNow.|
|Upload ServiceNow Attachment to S3|Uploads file from the System Attachment Table \(sys\_attachment\) to a specified Amazon S3 bucket.|
|Permission Management|Create ACL|Create new ACL for a bucket and delete the existing one.|
|Look up ACL|Retrieves the ACL details for the requested resource.|
|Tag Management|Look up Tags|Lists tags of the specified Amazon S3 resource.|
|Update Tags|Updates the tags of the specified Amazon S3 resource.|

**Note:** Spoke actions can be used independently without subscribing to notifications from Amazon S3.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon S3 spoke](../task/setup-amazon-s3.md#).

