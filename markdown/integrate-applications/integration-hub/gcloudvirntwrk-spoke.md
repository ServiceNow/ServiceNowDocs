---
title: Google Cloud Virtual Network Spoke
description: Manage firewall, network, subnetwork, and IP address in Google Cloud Virtual Network from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Google Cloud Virtual Network Spoke

Manage firewall, network, subnetwork, and IP address in Google Cloud Virtual Network from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud Virtual Network spoke v1.0.4 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   [Google Persistent Disk Spoke](gpersistentdisk-spoke-1.md) \(sn\_gpdisk\_spoke\)
-   [Google Compute Engine Spoke](gcomengine-spoke-1.md) \(sn\_gcompute\_spoke\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Google Cloud Virtual Network account requirements

The Google Cloud Virtual Network spoke requires a custom app that you create in the Google Cloud Platform.

## Supported versions

This spoke was built for API version v1, but may be compatible with later versions.

## Spoke actions

The Google Cloud Virtual Network spoke provides actions to automate Google Cloud Virtual Network when events occur in ServiceNow. For the spoke actions to be performed, you must ensure that your project or organization in Google Cloud Platform has the mentioned permissions. Available spoke actions include:

|Category|Action|Description|Permissions required|
|--------|------|-----------|--------------------|
|Address Management|Create IP Address For Region|Creates an address resource in the specified project by using the data included in the request.|compute.addresses.create|
|Delete IP Address|Deletes the specified address resource.|compute.addresses.delete|
|Get IP Address|Retrieves details of the specified address resource.|compute.addresses.get|
|Firewall Management|Create Firewall For Egress|Creates a firewall for egress rule in the specified project.|compute.firewalls.create|
|Create Firewall For Ingress|Creates a firewall for an ingress rule in the specified project.|compute.firewalls.create|
|Delete Firewall|Deletes the specified firewall.|compute.firewalls.delete|
|Get Firewall|Retrieves details of the specified firewall.|compute.firewalls.get|
|Update Firewall For Egress|Updates a firewall for the egress rule in the specified project.|compute.firewalls.update|
|Update Firewall For Ingress|Updates a firewall for the ingress rule in the specified project.|compute.firewalls.update|
|Metadata Retrieval Management|List Addresses|Retrieves a list of addresses contained within the specified region.|compute.addresses.list|
|List Firewalls|Retrieves a list of firewalls available to the specified project.|compute.firewalls.list|
|List Networks|Retrieves a list of networks available to the specified project.|compute.networks.list|
|List Subnetworks|Retrieves a list of subnetworks available to the specified project.|compute.subnetworks.list|
|Network Management|Create Network|Creates a network in the specified project.|compute.networks.create|
|Delete Network|Deletes the specified network.|compute.networks.delete|
|Get Network|Retrieves details of the specified network.|compute.networks.get|
|Subnetwork Management|Create Subnetwork|Creates a subnetwork in the specified project.|compute.subnetworks.create|
|Delete Subnetwork|Deletes the specified subnetwork.|compute.subnetworks.delete|
|Expand IP CIDR Range|Expands the IP CIDR range of the subnetwork to a specified value.|compute.subnetworks.expandIpCidrRange|
|Get IAM Policy|Retrieves details of the access control policy for a resource.|compute.subnetworks.getIamPolicy|
|Get Subnetwork|Retrieves details of the specified subnetwork.|compute.subnetworks.get|
|Set IAM Policy|Sets the access control policy on the specified resource.|compute.subnetworks.setIamPolicy|

For more information about the required permissions, see [IAM permissions reference](https://cloud.google.com/iam/docs/permissions-reference).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Cloud Virtual Network spoke](../task/setup-gvirnetwork.md).

