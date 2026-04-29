---
title: Google Cloud Datastore Spoke
description: Manage the NoSQL database services in Google Cloud Datastore from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Cloud Datastore Spoke

Manage the NoSQL database services in Google Cloud Datastore from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud Datastore spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for Google Cloud Datastore v1, but may be compatible with later versions.

## Spoke requirements

Google Cloud Datastore account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

IntegrationHub \(com.glide.hub.integrations\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Cloud Datastore spoke provides actions to automate Google Cloud Datastore tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Entity Management|Entity Export|Exports a copy of all or a subset of entities from Google Cloud Datastore to another storage system.|
|Entity Import|Imports entities into Google Cloud Datastore.|
|Index Management|Create Index|Creates the specified index.|
|Delete Index|Deletes an existing index.|
|Get Index|Gets an index.|
|Look up Index|Retrieves the list of indexes that match the specified filters.|
|Operation Management|Cancel Operation|Starts asynchronous cancellation on a long-running operation.|
|Delete Operation|Deletes a long-running operation.|
|Get Operation|Gets the latest state of a long-running operation.|
|Look up Operation|Retrieves the list of operations that match the specified filter in the request.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Cloud Datastore spoke](../task/setup-gcloud-datastore.md#).

