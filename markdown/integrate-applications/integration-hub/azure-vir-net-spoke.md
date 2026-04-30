---
title: Microsoft Azure Virtual Network Spoke
description: Manage Microsoft Azure Virtual Network \(VNet\) from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Azure Virtual Network Spoke

Manage Microsoft Azure Virtual Network \(VNet\) from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure Virtual Network spoke v2.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - Get Connection Info
-   Azure Resource Management spoke \(sn\_azure\_rm\_spoke\) v 2.0.0 is installed and a connection alias is created on your instance.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For more information on the licenses, contact your account manager.

## Supported Versions

This spoke was built for API version 2023-09-01 for List Network Interface Names by ResourceGroup and Look Up Network Interfaces By Resource Group, 2019-11-01 for other actions but may be compatible with later versions.

## Spoke requirements

-   Microsoft Azure Resource Management spoke \(com.sn.ms.azure.resource.mgmt.spoke\)
-   Microsoft Azure subscription with access to Azure Virtual Network service

## Spoke flows and subflows

This spoke has no flows and subflows.

## Spoke actions

The Microsoft Azure Virtual Network spoke provides actions to automate Microsoft Azure Virtual Network tasks when events occur in ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Network Interface Management|Create Network Interface|Creates a network interface.|
|Delete Network Interface|Deletes the specified network interface.|
|Look up Network Interface|Retrieves specified network interface information in a specified resource group.|
|Look up Network Interfaces Stream by Resource Group|Lists all the network interfaces in the specified resource group. Page size is fixed to 100 as per Microsoft.|
|Look up Network Interfaces Stream by Subscription ID|Lists all the network interfaces in the specified Subscription ID. Page size is fixed to 100 as per Microsoft.|
|Update Network Interface Tags|Updates tags on network interface.|
|Public IP Address Management|Create Public IP Address|Creates a public IP address as per the provided Resource Group.|
|Delete Public IP Address|Deletes the specified public IP address in a specified resource group.|
|Look up Public IP Address|Retrieves specified the public IP address information in a specified resource group.|
|Look up Public IP Addresses Stream by Resource Group|Lists all the public IP addresses in the specified resource group. Page size is fixed to 100 as per Microsoft.|
|Look up Public IP Addresses Stream by Subscription ID|Lists all the public IP addresses in the specified subscription. Page size is fixed to 100 as per Microsoft.|
|Update Public IP Address Tags|Updates tags on Public IP Address.|
|Subnet Management|Create Subnet|Creates a subnet in the specified virtual network.|
|Delete Subnet|Delete the specified subnet in a specified virtual network and resource group.|
|Look up Subnet|Retrieves specified subnet information in a specified virtual network and resource group.|
|Look up Subnets Stream|Lists all the subnets in the specified virtual network. Page size is fixed to 100 as per Microsoft.|
|Virtual Network Management|Create Virtual Network|Creates a virtual network in the specified resource group.|
|Create Virtual Network with Subnet|Creates a virtual network with provided Subnet in the specified resource group.|
|Delete Virtual Network|Deletes the specified virtual network in a specified resource group.|
|Look up Virtual Network|Retrieves specified virtual network information in a specified resource group.|
|Look up Virtual Network Usage Status Stream|Lists the virtual network usage status in a specified resource group. Page size is fixed to 100 as per Microsoft.|
|Look up Virtual Networks Stream by Resource Group|Lists all the virtual networks in the specified resource group. Page size is fixed to 100 as per Microsoft.|
|Look up Virtual Networks Stream by Subscription ID|Lists all the virtual networks in the specified Subscription. Page size is fixed to 100 as per Microsoft.|
|Update Virtual Network Tags|Updates tags on virtual network.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

## Set up the Microsoft Azure Virtual Network Spoke

To execute the actions of the Microsoft Azure Virtual Network Spoke, you must first install and configure the Microsoft Azure Resource Management Spoke. No separate configuration of the Microsoft Azure Virtual Network Spoke is necessary. To view the procedure to set up the Microsoft Azure Resource Management Spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

