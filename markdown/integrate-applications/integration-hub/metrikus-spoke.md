---
title: Metrikus spoke
description: Metrikus spoke provides actions to retrieve data from various sensors \(such as occupancy sensor, air quality sensor, temperature sensor etc.\) that are found at a workplace.Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Metrikus spoke

Metrikus spoke provides actions to retrieve data from various sensors \(such as occupancy sensor, air quality sensor, temperature sensor etc.\) that are found at a workplace.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Metrikus spoke - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Metrikus Beta v1.0.

## Key features

Metrikus Spoke integrates with Flow Designer Integration Hub. It fetches the occupancy sensor data from Metrikus and provides the following:

-   Get event data. For example, when an employee enters a meeting room,when an employee occupies a desk\).Get occupancy data for Workplace Connectors space records from Metrikus.
-   Get occupancy data.
-   The occupancy data is used for configuring automatic reservation check in.
-   Workplace Service Delivery Location Directory shows Occupancy state for a selected location or space.

## Spoke requirements

-   Ensure that you have Metrikus login credentials.
-   Metrikus provided Client ID and Client Secret key.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \[com.glide.hub.integration.runtime\]
-   ServiceNow IntegrationHub Action Step - OpenAPI \[com.glide.hub.action\_step.openapi\]
-   Metrikus Spoke \[com.sn.wsd.metrikus.spoke\]

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Metrikus Spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Actions|Description|
|-------|-----------|
|Look up Space Tree|Get all the spaces along with the location hierarchy from Metrikus.|
|Look up Space Occupancy Batches|Gets batches of spaces \(for example, 2000\) and get occupancy data from Metrikus for all batches to combine and map it.|
|Look up Latest Desk Occupancy|Gets occupancy data for desks in a batch \( for example, 2000.\)|
|Look up Latest Space Occupancy|Gets occupancy data for spaces in a batch \(for example, 2000\)|
|Look up Desks Occupancy Batches|Gets batches of desks \(for example, 2000\) and get occupancy data to combine and map it with Metrikus Spoke.|

## Spoke subflows

The Metrikus Spoke provides sample subflows to demonstrate automating Workplace Connectors tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Get All occupancy by Ids|Retrieves occupancy data of both Workplace Connectors spaces and desks.|
|Get Occupancy by desks by Ids|Retrieves occupancy data of all desks. Invoked by **Get All Occupancy by Ids**sub flow.|
|Get Occupancy by spaces|Retrieves occupancy of all spaces. Invoked by the **Get All Occupancy by Ids** sub flow.|

## Spoke user roles

The Metrikus spoke provides the System Administrator user role to control access to data:

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.



