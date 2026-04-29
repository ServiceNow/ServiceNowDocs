---
title: Google Compute Engine Spoke
description: Launch and manage virtual machines in Google Compute Engine spoke from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Compute Engine Spoke

Launch and manage virtual machines in Google Compute Engine spoke from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Compute Engine spoke v1.0.5 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   [Google Persistent Disk Spoke](gpersistentdisk-spoke.md) \(sn\_gpdisk\_spoke\)
-   [Google Cloud Virtual Network Spoke](gcloudvirntwrk-spoke.md) \(sn\_gcp\_vpc\_spoke\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Google Compute Engine spoke account requirements

The Google Compute Engine spoke requires a custom app that you create in Google Cloud Platform.

## Supported versions

This spoke was built for API version v1, but may be compatible with later versions.

## Spoke actions

The Google Compute Engine spoke provides actions to automate Google Compute Engine when events occur in ServiceNow. For the spoke actions to be performed, you must ensure that your project or organization in Google Cloud Platform has the mentioned permissions. Available spoke actions include:

|Category|Action|Description|Permissions Required|
|--------|------|-----------|--------------------|
|Instance Template Management|Create Instance Template|Creates an instance template.|compute.instanceTemplates.create|
|Create Instance Template From Instance|Creates an instance template from instance.|compute.instanceTemplates.create|
|Delete Instance Templates|Deletes the specified instance template.|compute.instanceTemplates.delete|
|Get Instance Template|Retrieves details of the specified instance template.|compute.instanceTemplates.get|
|Machine Types Management|Get Machine Type By Zone|Retrieves details of the specified machine type by zone.|compute.machineTypes.get|
|Metadata Retrieval Management|List Instance Templates|Retrieves a list of instance templates available to the specified project.|compute.instanceTemplates.list|
|List Machine Types By Zone|Retrieves a list of machine types available to the specified project.|compute.machineTypes.list|
|List Regions|Retrieves a list of regions available to the specified project.|compute.regions.list|
|List VM Instances By Zone|Retrieves a list of VM instances available to the specified project.|compute.instances.list|
|List Zones|Retrieves a list of zones available to the specified project.|compute.zones.list|
|Region Management|Get Region|Retrieves the specified region resource.|compute.regions.get|
|VM Instance Management|Attach Disk|Attaches an existing Disk resource to an instance.|compute.instances.attachDisk|
|Create Instance|Creates an instance resource in the specified project.|compute.instances.create|
|Delete Instance|Deletes the specified instance.|compute.instances.delete|
|Detach Disk|Detaches a disk from an instance.|compute.instances.detachDisk|
|Get IAM Policy|Retrieves the access control policy for a resource.|compute.instances.getIamPolicy|
|Get Instance By Zone|Retrieves the specified Instance by zone.|compute.instances.get|
|Reset Instance|Performs a reset on instance.|compute.instances.reset|
|Set IAM Policy|Sets the access control policy on the specified resource.|compute.instances.setIamPolicy|
|Set Labels On Instance|Sets labels on an instance.|compute.instances.setLabels|
|Set Tags On Instance|Sets tags for the specified instance.|compute.instances.setTags|
|Start Instance|Starts an instance.|compute.instances.start|
|Stop Instance|Stops an instance.|compute.instances.stop|
|Zone Management|Get Zone|Retrieves information about the specified zone.|compute.zones.get|

For more information about the required permissions, see [IAM permissions reference](https://cloud.google.com/iam/docs/permissions-reference).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Compute Engine spoke](../task/setup-gcompute.md#).

