---
title: Microsoft Azure Resource Management Spoke
description: Azure Resource Management enables you to create, update, and delete the resources in your Microsoft Azure subscription from within ServiceNow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Azure Resource Management Spoke

Azure Resource Management enables you to create, update, and delete the resources in your Microsoft Azure subscription from within ServiceNow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

These spokes depend on the installation of the Microsoft Azure Resource Management spoke plugin and its setup for the execution of their actions.

-   Microsoft Azure SQL Database spoke
-   Microsoft Azure Virtual Network spoke
-   Microsoft Azure Managed Storage spoke
-   Microsoft Azure Cosmos DB spoke
-   Microsoft Azure Notification Hub spoke
-   Microsoft Azure Traffic Manager spoke
-   Microsoft Azure Automation spoke
-   Microsoft Azure Virtual Machine spoke

## Spoke version

Microsoft Azure Resource Management spoke v2.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for the API version 2021-04-01, but may be compatible with the later versions.

## Spoke actions

The Microsoft Azure Resource Management spoke provides actions to automate the resource management tasks when events occur in the ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Metadata Retrieval|Look up Databases|Retrieves a list of databases in a server.|
|Look up Elastic Pools|Retrieves a list of elastic pools in Microsoft Azure.|
|Look up Locations|Retrieves a list of locations.|
|Look up Operational Status of Resource|Returns the operational status of the resource \(virtual machine, network, disk, and so on\) that is created or updated.|
|Look up Resource Groups|Retrieves a list of resource groups.|
|Look up SQL Servers|Retrieves a list of servers in a resource group.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

