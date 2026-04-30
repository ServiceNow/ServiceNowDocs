---
title: Amazon DynamoDB Spoke
description: Manage streams, tables, and tags in your Amazon DynamoDB database from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon DynamoDB Spoke

Manage streams, tables, and tags in your Amazon DynamoDB database from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon DynamoDB spoke v1.0.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for API version 2012-08-10, but may be compatible with later versions.

## Spoke requirements

-   User with full access to Amazon DynamoDB.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke actions

The Amazon DynamoDB spoke provides actions to automate Amazon DynamoDB tasks when events occurs in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Stream Management|Disable Stream|Disables the stream for the specified table.|
|Enable Stream|Enables the stream for the specified table.|
|Get Shard Iterator|Returns a shard iterator. Use the shard iterator in a subsequent Get Records request to read the stream records from the shard.|
|Get Stream|Returns information about the specified stream.|
|Look up Records|Retrieves the stream records from a given shard.|
|Look up Streams|Returns the list of all the streams associated with the current account.|
|Table Management|Create Backup|Creates a backup for an existing table.|
|Create Table|Creates a table in the account.|
|Delete Backup|Deletes an existing backup of a table.|
|Delete Table|Deletes the specified table.|
|Get Backup|Retrieves the details of an existing backup.|
|Get Continuous Backup|Retrieves the status of continuous backups and point in time recovery of the specified table.|
|Get Table|Retrieves information about the table.|
|Look up Backups|Retrieves the list of all the backups associated with the account or backups of the specified table.|
|Look up Tables|Retrieves the list of table names.|
|Restore Table From Backup|Creates a table from an existing backup.|
|Restore Table To Point In Time|Restores the specified table to the specified point in time within Earliest Restorable Date Time and Latest Restorable Date Time.|
|Update Continuous Backup|Enables or disables point in time recovery for the specified table.|
|Update Table|Updates the specified table.|
|Tag Management|Add Tags To DynamoDB Resource|Adds tags to DynamoDB resource.|
|Look up Tags Of DynamoDB Resource|Lists the tags of the DynamoDB resource.|
|Remove Tags From DynamoDB Resource|Removes the tags from the DynamoDB resource.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

**Note:** Two Credential aliases are available for the Amazon DynamoDB spoke.

For information about setting up the spoke, see [Set up the Amazon DynamoDB spoke](../../integrationhub/tasks/setup-dyndb.md#).

