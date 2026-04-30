---
title: Google Cloud VPC Access Spoke
description: Manage connector and operations in your Google Cloud VPC Access account from ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Google Cloud VPC Access Spoke

Manage connector and operations in your Google Cloud VPC Access account from ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The current Google Cloud VPC Access spoke version is 1.0.1.

## Supported versions

This spoke was built for the Google Cloud VPC Access API version v1, but may be compatible with later versions.

## Google Cloud VPC Access spoke requirements

The Google Cloud VPC Access spoke requires a custom app that you create in Google Cloud Platform.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Google Identity and Access Spoke](gidentityaccess-spoke-1.md)
-   [Google Cloud Virtual Network Spoke](gcloudvirntwrk-spoke-1.md)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Cloud VPC Access spoke provides actions to automate Google Cloud VPC Access tasks when events occurs in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Connector Management|Create Connector|Creates a connector in the specified project.|
|Delete Connector|Deletes the specified VPC Access connector.|
|Get Connector|Retrieves the specified VPC Access connector.|
|Look up Connectors|Retrieves the list of VPC Access connectors available in the specified location.|
|Location Management|Look up Locations|Retrieves the list of locations available in the specified project.|
|Operation Management|Get Operation|Retrieves details of the specified operation.|
|Look up Operations|Retrieves a list of operations available with in the specified location.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Cloud VPC Access spoke](../task/setup-gcloud-vpc.md#).

