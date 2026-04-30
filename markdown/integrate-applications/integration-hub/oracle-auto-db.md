---
title: Oracle Autonomous DB Spoke
description: Manage the Oracle Autonomous Database operations from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Oracle Autonomous DB Spoke

Manage the Oracle Autonomous Database operations from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Autonomous DB spoke v1.0.6 is the latest version.

## Supported versions

This spoke was built for Oracle Autonomous DB 20160918, but may be compatible with later versions.

## Spoke requirements

Oracle Autonomous DB account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   Oracle Cloud IAM spoke\(com.sn.oci.iam.spoke\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Autonomous DB spoke provides actions to automate Oracle Autonomous DB tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Database Backup Management|Create Database Backup|Creates an Autonomous Database backup for the specified database based on the specified request parameters.|
|Get Database Backup|Retrieves the details of the specified Autonomous Database backup.|
|Look up Database Backups|Retrieves a list of Autonomous Database backups based on the specified database ID or compartment ID.|
|Database Management|Create Database|Creates an Autonomous Database.|
|Create Database by Cloning|Creates a clone of the existing Autonomous Database.|
|Delete Database|Deletes the specified Autonomous Database.|
|Deregister Database Data Safe|Deregisters the specified Autonomous Database asynchronously with data safe.|
|Failover Database|Initiates a failover database of the specified Autonomous Database to a standby.|
|Get Database|Retrieves details of the specified Autonomous Database.|
|Look up Databases|Retrieves a list of Autonomous Databases.|
|Register Database Data Safe|Registers the specified Autonomous Database asynchronously with data safe.|
|Restart Database|Restarts the specified Autonomous Database.|
|Start Database|Starts the specified Autonomous Database.|
|Stop Database|Stops the specified Autonomous Database.|
|Update Database|Updates the specified Autonomous Database.|
|Database Version|Look up Database Versions|Retrieves the list of supported Autonomous Database versions.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Autonomous DB spoke](../task/setup-oracle-auto-db.md#).

