---
title: Microsoft Azure SQL Database Spoke
description: Configure and manage the Microsoft Azure SQL databases from within the ServiceNow instance. When you install the Microsoft Azure SQL database spoke, you also get the Microsoft Azure SQL Resource Management spoke. The Microsoft Azure Resource Manager provides a management layer that enables you to create, update, and delete the resources in your Microsoft Azure subscription.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Azure SQL Database Spoke

Configure and manage the Microsoft Azure SQL databases from within the ServiceNow instance. When you install the Microsoft Azure SQL database spoke, you also get the Microsoft Azure SQL Resource Management spoke. The Microsoft Azure Resource Manager provides a management layer that enables you to create, update, and delete the resources in your Microsoft Azure subscription.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure SQL Database spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for the API version 2021-11-01, but may be compatible with the later versions.

## Spoke requirements

User with full access to Microsoft Azure Azure Cloud Computing.

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

The provides actions to automate Microsoft Azure Microsoft Azure SQL tasks when events occur in the ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Database Management|Create Generic Database|Creates a generic database in Microsoft Azure.|
|Create Hyperscale Database|Creates a Hyperscale database in Microsoft Azure.|
|Create VCore Database|Creates a VCore database in Microsoft Azure.|
|Delete Database|Deletes the required database in a server.|
|Look up Database|Retrieves details of a database.|
|Look up Databases Stream by Elastic Pool|Retrieves a list of databases in an elastic pool.|
|Look up Databases Stream by Server|Retrieves a list of databases in a server.|
|Look up Operational Status|Generates the operational status of a database that is created or updated.|
|Rename Database|Renames a database.|
|Update Database|Updates the SKU or the properties of a database.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Set up the Microsoft Azure SQL Database Spoke

To execute the actions of the Microsoft Azure SQL Database Spoke, you must first install and configure the Microsoft Azure Resource Management Spoke. No separate configuration of the Microsoft Azure SQL Database Spoke is necessary. To view the procedure to set up the Microsoft Azure Resource Management Spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

