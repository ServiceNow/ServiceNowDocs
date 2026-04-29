---
title: Microsoft Azure Traffic Manager Spoke
description: Integrate ServiceNow instance with Azure Traffic Manager. Manage DNS-based traffic distribution and load balancing from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure Traffic Manager Spoke

Integrate ServiceNow instance with Azure Traffic Manager. Manage DNS-based traffic distribution and load balancing from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Azure Traffic Manager spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for Azure Traffic Manager 2022-04-01, but may be compatible with later versions.

## Spoke requirements

Client ID and Client Secret of the Azure Traffic Manager registered in the Azure portal.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Azure Resource Management spoke \(sn\_azure\_rm\_spoke\) v 2.0.0 is installed and a connection alias is created on your instance.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For more information on the licenses, contact your account manager.

## Spoke actions

The Azure Traffic Manager Spoke provides actions to automate DNS-based traffic load-balancing tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Endpoint Management|Create Endpoint|Creates a Traffic Manager Endpoint.|
|Delete Endpoint|Deletes a Traffic Manager Endpoint.|
|Look up Endpoint|Retrieves the details of a Traffic Manager Endpoint.|
|Update Endpoint|Updates a Traffic Manager Endpoint.|
|Profile Management|Create Profile|Creates a Traffic Manager Profile.|
|Delete Profile|Deletes a Traffic Manager Profile.|
|Look up DNS Name Availability|Checks the availability of a Traffic Manager Relative DNS name.|
|Look up Profile|Look up a Traffic Manager Profile.|
|Look up Profiles by Resource Group|Look up Traffic Manager Profiles by Resource Group.|
|Look up Profiles by Subscription ID|Look up Traffic Manager Profiles by Subscription ID.|
|Update Profile|Updates a Traffic Manger Profile.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Set up the Microsoft Azure Traffic Manager Spoke

To execute the actions of the Microsoft Azure Traffic Manager Spoke, you must first install and configure the Microsoft Azure Resource Management Spoke. No separate configuration of the Microsoft Azure Traffic Manager Spoke is necessary. To view the procedure to set up the Microsoft Azure Resource Management Spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

