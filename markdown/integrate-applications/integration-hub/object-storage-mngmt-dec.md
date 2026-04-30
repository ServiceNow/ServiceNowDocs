---
title: Oracle Object Storage Management Spoke
description: Manage objects, buckets, and namespace in the Oracle Object Storage Management account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Object Storage Management Spoke

Manage objects, buckets, and namespace in the Oracle Object Storage Management account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Object Storage Management spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Oracle Object Storage Management API version 20160918, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Oracle Cloud IAM Spoke](oracle-iam.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Object Storage Management spoke provides actions to automate Oracle Object Storage Management tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Bucket Management|Create Bucket|Creates a bucket in the specified Oracle Cloud Namespace.|
|Delete Bucket|Deletes the specified bucket.|
|Get Bucket|Retrieves details of the specified bucket.|
|Look up Buckets|Retrieves a list of buckets in the specified compartment.|
|Re-encrypt Bucket|Re-encrypts the specified bucket.|
|Update Bucket|Updates details of the specified bucket.|
|Namespace Metadata|Get Namespace|Retrieves the name of the Object Storage namespace for the user.|
|Object Management|Copy Object|Creates a request to copy an object within a region or to another region.|
|Create or Update Object|Creates a new object or overwrites an existing object with the same name|
|Delete Object|Deletes the specified object.|
|Get Object|Retrieves the specified object.|
|Look up Objects|Retrieves a list of objects in the specified bucket.|
|Re-encrypt Object|Re-encrypts the specified object.|
|Rename Object|Renames the specified object.|
|Restore Object|Restores the specified object.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Object Storage Management spoke](../task/obj-storg-mngmt-setup-dec.md).

