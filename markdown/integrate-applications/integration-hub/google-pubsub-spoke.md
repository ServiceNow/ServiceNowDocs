---
title: Google Cloud Pub Sub Spoke
description: Manage Google Cloud Pub/Sub messaging service from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Cloud Pub Sub Spoke

Manage Google Cloud Pub/Sub messaging service from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Google Cloud Pub Sub v1, but may be compatible with later versions.

## Spoke version

Google Cloud Pub Sub spoke v1.0.4 is the latest version.

## Spoke requirements

Google Cloud account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   Google Identity And Access Spoke \(sn\_gcp\_id\_acc\_spk\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Google Cloud Pub Sub Spoke provides sample subflows to demonstrate automating Google Cloud Pub/Sub tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Google PubSub Messages|Receives messages from a sub topic and displays the messages in logs.|

## Spoke actions

The Google Cloud Pub Sub Spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Snapshot Management|Create Snapshot|Creates a snapshot from the requested subscription.|
|Delete Snapshot|Removes the specified existing snapshot.|
|Get Snapshot IAM Policy|Retrieves the IAM policy of the snapshot.|
|Look up Snapshots|Retrieves a list of existing snapshots.|
|Set Snapshot IAM Policy|Assigns the access control policy to the specified snapshot.|
|Update Snapshot|Updates an existing snapshot.|
|Subscription Management|Acknowledge|Acknowledges the messages associated with the acknowledge IDs in the acknowledge request.|
|Acknowledge Deadline|Updates the acknowledge deadline in seconds for a specific message.|
|Create Pull Subscription|Creates a pull subscription to the specified topic.|
|Create Push Subscription|Creates a push subscription to the specified topic.|
|Delete Subscription|Deletes an existing subscription for the specified project.|
|Get Subscription|Retrieves the configuration details of the specified subscription.|
|Get Subscription IAM Policy|Retrieves the access control policy for the specified subscription.|
|Look up Subscriptions|Retrieves a list of subscriptions.|
|Pull Messages|Pulls message asynchronously for the specified project.|
|Seek Subscription|Seeks an existing subscription to a point in time or to a specified snapshot.|
|Set Subscription IAM Policy|Assigns the access control policy to the specified subscription.|
|Update Push Configuration|Updates the push configuration for the specified subscription.|
|Update Subscription|Updates the specified existing subscription.|
|Topic Management|Create Topic|Creates a topic with the specified name.|
|Delete Topic|Deletes the specified topic.|
|Get IAM Policy|Retrieves the specified access control policy of a resource.|
|Get Topic|Retrieves the configuration details of the specified topic.|
|Look up Topics|Retrieves a list of topics.|
|Publish Messages|Adds one or more messages to the specified topic.|
|Set IAM Policy|Assigns the access control policy to the specified resource.|
|Update Topic|Updates the specified topic.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Cloud Pub Sub Spoke](../task/setup-google-pubsub.md#).

