---
title: Microsoft Azure Cosmos DB Spoke
description: Manage Microsoft Azure Cosmos DB from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Azure Cosmos DB Spoke

Manage Microsoft Azure Cosmos DB from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure Cosmos DB spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for Microsoft Azure Cosmos DB v2, but may be compatible with later versions.

## Spoke requirements

Microsoft Azure Portal account.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   Microsoft Azure Resource Management spoke \(com.sn.ms.azure.resource.mgmt.spoke\) v 2.0.0 is installed and a connection alias is created on your instance.
-   The connection alias of Microsoft Azure Cosmos DB SAS is configured on your instance.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Azure Cosmos DB Spoke provides actions to automate Microsoft Azure Cosmos DB tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Cassandra Database Management|Create Cassandra Keyspace|Creates a Cassandra keyspace within the specified Subscription ID and Resource Group.|
|Delete Cassandra Keyspace|Deletes the specified Cassandra keyspace within the specified Subscription ID and Resource Group.|
|Look up Cassandra Keyspace|Get the details of the specified Cassandra keyspace within the specified Subscription ID and Resource Group.|
|Look up Cassandra Keyspace Throughput|Gets the details of the throughput of the specified Cassandra keyspace within the specified Subscription ID and Resource Group.|
|Look up Cassandra Keyspaces|Lists all the Cassandra keyspaces in the specified Subscription ID and Resource Group.|
|Update Cassandra Keyspace Throughput|Update the throughput of the specified Cassandra keyspace within the specified Subscription ID and Resource Group.|
|Core SQL Database Management|Create Database|Creates a database under a specified database account.|
|Create Permission|Creates a permission in the specified database.|
|Create User|Creates the user in a specified database.|
|Delete Database|Deletes the specified database information in a specified database account.|
|Delete Permission|Deletes the specified permission information of a user.|
|Delete User|Deletes the user of the specified database.|
|Look up Database|Retrieves the specified database information in a specified database account.|
|Look up Databases|Lists all the databases in the specified database account.|
|Look up Permission|Retrieves the specified permission information of a user.|
|Look up Permissions|Lists all the permissions of the specified database.|
|Look up User|Retrieves the specified user information in a specified database.|
|Look up Users|Lists all the users of the specified database.|
|Replace Permission|Replaces the specified permission.|
|Replace User|Replaces the specified user in a specified database by another user.|
|Database Account Management|Create DB Account|Creates an account in Azure Cosmos DB.|
|Delete DB Account|Deletes the specified Cosmos DB account.|
|Enable or Disable Options on DB Account|Updates the details of a specified database account.|
|Look up Access Keys|Lists all access keys in the specified Azure Cosmos DB database account.|
|Look up Connection Strings|Lists all the connection strings in the specified Azure Cosmos DB account.|
|Look up DB Account|Retrieves the DB account for the provided Subscription ID and Resource Group.|
|Look up DB Accounts by Resource Group|Retrieves the list of DB accounts for the provided Subscription ID and Resource Group.|
|Look up DB Accounts by Subscription ID|Retrieves the list of DB accounts for the provided Subscription ID.|
|Look up Usages|Retrieves the most recent data in the specified database account.|
|Regenerate Access Key|Regenerates an access key for the specified Azure Cosmos DB account.|
|Update Failover Priority|Updates the details of a specified database account.|
|Mongo Database Management|Create MongoDB Database|Creates the specified MongoDB database within the specified Subscription ID and Resource Group.|
|Delete MongoDB Database|Deletes the specified MongoDB database within the specified Subscription ID and Resource Group.|
|Look up MongoDB Database|Get the details of the provided MongoDB database within the specified Subscription ID and Resource Group.|
|Look up MongoDB Database Throughput|Get the details of the throughput of the provided MongoDB database within the specified Subscription ID and Resource Group.|
|Look up MongoDB Databases|Lists all the MongoDB databases within the specified Subscription ID and Resource Group.|
|Update MongoDB Database Throughput|Creates a Cassandra keyspace within the specified Subscription ID and Resource Group.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Microsoft Azure Cosmos DB spoke](../task/setup-azure-cosmos-db.md#).

Set up the Microsoft Azure Cosmos DB spoke by fulfilling the following dependencies:

-   Install and configure a connection alias of the Microsoft Azure Resource Management Spoke. To view the procedure, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).
-   Configure a connection alias of the Microsoft Azure Cosmos DB SAS. To view the procedure, see [Create a connection alias record for Microsoft Azure Cosmos DB SAS](../task/setup-azure-cosmos-db.md#).

