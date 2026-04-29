---
title: Google Cloud SQL Spoke
description: Mange provisioning of MySQL and PostgreSQL in Google Cloud SQL from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Cloud SQL Spoke

Mange provisioning of MySQL and PostgreSQL in Google Cloud SQL from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud SQL spoke v1.0.1 is the latest version.

## Supported versions

This spoke was built for Google Cloud SQL v1beta4, but may be compatible with later versions.

## Spoke requirements

-   Google Cloud Platform account
-   Google Identity and Access spoke \(sn\_gcpcloudsql\_spk\)

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   • ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   • ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   • ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   • ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   • Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Cloud SQL provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|Required Permission|
|--------|------|-----------|-------------------|
|Back up Run Management:|Create Backup|Creates a backup.|cloudsql.backupRuns.create|
|Delete Backup Run|Deletes a backup.|cloudsql.backupRuns.delete|
|Get Backup Run|Retrieves details of the backup.|cloudsql.backupRuns.get|
|Look up Backup Runs|Retrieves a list of the backup runs.|cloudsql.backupRuns.list|
|Database Management|Create Database|Creates a database.|cloudsql.databases.create|
|Delete Database|Deletes a database.|cloudsql.databases.delete|
|Get Database|Retrieves details of the instance.|cloudsql.databases.get|
|Look up Databases|Retrieves a list of the databases.|cloudsql.databases.list|
|Update Database|Updates a database.|cloudsql.databases.update|
|Instance Management|Clone Instance|Clones an instance.|cloudsql.instances.clone|
|Create Instance|Creates an instance.|cloudsql.instances.create|
|Delete Instance|Deletes an instance.|cloudsql.instances.delete|
|Get Instance|Retrieves details of the instance.|cloudsql.instances.get|
|Look up Instances|Retrieves a list of the instances.|cloudsql.instances.clone|
|Restart Instance|Restarts an instance.|cloudsql.instances.restart|
|Update Instance|Updates an instance.|cloudsql.instances.update|
|Operations|Get Operation|Retrieves details of the operation.|N/A|
|Look up Operations|Retrieves a list of the operations.|N/A|
|Tiers|Look up Tiers|Retrieves a list of the tiers.|N/A|
|User Management|Create User|Creates a user.|cloudsql.users.create|
|Delete User|Deletes a user.|cloudsql.users.delete|
|Look up User|Retrieves a list of the users.|cloudsql.users.list|
|Update User|Updates a user.|cloudsql.users.update|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Cloud SQL spoke](../task/setup-gcloud-sql.md#).

