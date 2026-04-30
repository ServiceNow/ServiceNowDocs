---
title: Google Persistent Disk Spoke
description: Manage disks, snapshots, and images in Google Persistent Disk from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Persistent Disk Spoke

Manage disks, snapshots, and images in Google Persistent Disk from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Persistent Disk spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for API version v1, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   [Google Cloud Virtual Network Spoke](gcloudvirntwrk-spoke.md) \(sn\_gcp\_vpc\_spoke\)
-   [Google Compute Engine Spoke](gcomengine-spoke.md) \(sn\_gcompute\_spoke\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Google Persistent Disk account requirements

The Google Persistent Disk spoke requires a custom app that you create in the Google Cloud Platform.

## Spoke actions

The Google Persistent Disk spoke provides actions to automate Google Persistent Disk when events occur in ServiceNow. For the spoke actions to be performed, you must ensure that your project or organization in Google Cloud Platform has the mentioned permissions. Available spoke actions include:

|Category|Action|Description|Permissions Required|
|--------|------|-----------|--------------------|
|Disk Management|Create Disk|Creates a persistent disk in the specified project.|compute.disks.create|
|Delete Disk|Deletes the specified persistent disk.|compute.disks.delete|
|Get Disk|Retrieves details of the specified persistent disk.|compute.disks.get|
|Get Disk Type by Zone|Retrieves the details of the specified disk type by zone.|compute.diskTypes.get|
|Resize Disk|Resizes the specified persistent disk.|compute.disks.resize|
|Image Management|Create Image for Disk|Creates an image in the specified project.|compute.images.create|
|Create Image for Image|Creates an image in the specified project.|compute.images.create|
|Create Image for Snapshot|Creates an image in the specified project.|compute.images.create|
|Delete Image|Deletes the specified image.|compute.images.delete|
|Get Image|Retrieves details of the specified image.|compute.images.get|
|Metadata Retrieval Management|List Disk Types by Zone|Retrieves a list of disk types available to the specified project.|compute.diskTypes.list|
|List Disks|Retrieves a list of persistent disks contained within the specified zone.|compute.disks.list|
|List Images|Retrieves the list of images available to the specified project.|compute.images.list|
|List Snapshots|Retrieves the list of snapshot resources contained within the specified project.|compute.snapshots.list|
|Snapshot Management|Create Snapshot|Creates a snapshot of a specified persistent disk.|compute.snapshots.create|
|Delete Snapshot|Deletes the specified snapshot resource.|compute.snapshots.delete|
|Get Snapshot|Retrieves details of the specified snapshot.|compute.snapshots.get|

For more information about the required permissions, see [IAM permissions reference](https://cloud.google.com/iam/docs/permissions-reference).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Persistent Disk spoke](../task/setup-gdisk.md).

