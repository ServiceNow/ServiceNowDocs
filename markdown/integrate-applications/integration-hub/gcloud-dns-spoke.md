---
title: Google Cloud DNS Spoke
description: Manage public zones and private managed DNS zones in using Google Cloud DNS account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Google Cloud DNS Spoke

Manage public zones and private managed DNS zones in using Google Cloud DNS account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Google Cloud DNS API version v1, but may be compatible with later versions.

## Spoke version

Google Cloud DNS Spoke version is 1.0.2.

## Spoke requirements

The Google Cloud DNS spoke requires a custom app that you create in Google Cloud Platform.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   [Google Cloud Virtual Network Spoke](gcloudvirntwrk-spoke.md)
-   [Google Identity and Access Spoke](gidentityaccess-spoke.md)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Cloud DNS spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Change Management|Create Change|Updates the resource record set collection.|
|Get Change|Retrieves the details of an existing change.|
|Look up Changes|Retrieves list of changes to a resource record set collection available with in the specified managed zone.|
|DNS Key Management|Get DNS Key|Retrieves details about an existing DNS key.|
|Look up DNS Keys|Retrieves list of DNS keys to a resource record set collection available with in the specified managed zone.|
|Managed Zone Management|Create Managed Zone For Private|Creates a managed private zone with private DNS records.|
|Create Managed Zone For Public|Creates a managed public zone.|
|Delete Managed Zone|Deletes the specified existing managed zone.|
|Get Managed Zone|Retrieves the details of the specified managed zone.|
|Look up Managed Zones|Retrieves list of managed zones available in the specified project.|
|Update Managed Zone For Private|Updates the details of the specified managed zone.|
|Update Managed Zone For Public|Updates the details of the specified managed zone.|
|Operation Management|Get Operation|Retrieves the details of an existing operation.|
|Look up Operations|Retrieves list of operations available with in the specified managed zone.|
|Policy Management|Create Policy|Creates a policy.|
|Delete Policy|Deletes the specified policy.|
|Get Policy|Retrieves the details about the specified policy.|
|Look up Policies|Retrieves list of policies available with in the specified project.|
|Update Policy|Updates details of the specified policy.|
|Project Management|Get Project|Retrieves the details about the specified project.|
|Resource Record Set Management|Look up Resource Record Sets|Retrieves list of resource record set collections available with in the specified managed zone.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Cloud DNS spoke](../task/setup-gcloud-dns.md#).

