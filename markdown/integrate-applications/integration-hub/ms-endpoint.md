---
title: Microsoft Endpoint Configuration Manager Spoke
description: The Microsoft Endpoint Configuration Manager \(MECM\) spoke automates actions to manage user collections, device collections, devices, and application deployments.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-02-23"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Endpoint Configuration Manager Spoke

The Microsoft Endpoint Configuration Manager \(MECM\) spoke automates actions to manage user collections, device collections, devices, and application deployments.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Endpoint Configuration Manager spoke v1.9 is the latest version.

## Supported versions

This spoke was built for Configuration Manager 2006, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step – PowerShell \(com.glide.hub.action\_step.powershell\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step – JDBC \(com.glide.hub.action\_step.jdbc\)
-   ServiceNow IntegrationHub Action Step – REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and need appropriate licenses, if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke subflows

The Microsoft Endpoint Configuration Manager spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

<table id="table_pg2_xz3_srb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Collection

</td><td>

Creates a collection in Microsoft Endpoint Configuration Manager and creates corresponding records for the new collection in the MECM Collections table.**Note:** This subflow is executed by AI agents.

</td></tr><tr><td>

Delete Collection

</td><td>

Deletes the specified collection from Microsoft Endpoint Configuration Manager server and removes the corresponding records from the MECM Collections table.**Note:** This subflow is executed by AI agents.

</td></tr><tr><td>

Add Target Collection to Application

</td><td>

Adds a target collection to the specified application in Microsoft Endpoint Configuration Manager and creates a corresponding record in the MECM Deployments table accordingly.**Note:** This subflow is executed by AI agents.

</td></tr><tr><td>

Remove Target Collection from Application

</td><td>

Removes a target group from the specified application on Microsoft Endpoint Configuration Manager server and removes the corresponding records from the MECM Deployments table accordingly.**Note:** This subflow is executed by AI agents.

</td></tr><tr><td>

Configure Collection

</td><td>

Creates a collection and configure it with specified Application ID in the Microsoft Endpoint Configuration Manager Portal.

</td></tr><tr><td>

Create Software Configuration

</td><td>

Creates the software configuration record of the specified Microsoft Endpoint Configuration Manager application.

</td></tr><tr><td>

Look Up Collections

</td><td>

Returns the list of all instal or uninstall Collections associated with the given Microsoft Endpoint Configuration Manager Application ID.

</td></tr><tr><td>

Revoke Application

</td><td>

Adds a user or device to an uninstalled collection and then removes it from the installed collection in the MECM server.

</td></tr><tr><td>

Look up Configuration Data

</td><td>

Retrieves the configuration data for the requested item.

</td></tr><tr><td>

Deploy Application

</td><td>

Adds a user or a device to an installed collection and then removes it from the uninstalled collection in the MECM server.

</td></tr><tr><td>

Discover and Store Data

</td><td>

Finds the data from the server and then updates the records in the Application, Collection, and Deployment tables.

</td></tr></tbody>
</table>**Note:** These subflows are available only when the [Client Software Distribution 2.0 application](csd-app-2.md) is installed.

## Spoke actions

The Microsoft Endpoint Configuration Manager spoke provides actions to automate tasks when events happen on your ServiceNow instance. Available actions include:

<table id="table_rg2_xz3_srb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Advanced Actions

</td><td>

Look up Device Collections Stream \(Database\)

</td><td>

Retrieves the device collection data from the MECM server using the Java Database Connectivity \(JDBC\) connection.

</td></tr><tr><td>

Look up User Collections Stream \(Database\)

</td><td>

Retrieves the user collection data from the MECM server using the JDBC connection.

</td></tr><tr><td>

Applications

</td><td>

Look up Applications

</td><td>

Retrieves the application data from the MECM server.

</td></tr><tr><td rowspan="7">

Device Management

</td><td>

Look up CMPivot Response by Operation ID

</td><td>

Retrieves CMPivot response from the MECM server.

</td></tr><tr><td>

Look up Device by ID

</td><td>

Retrieves the device data from the MECM server.

</td></tr><tr><td>

Run CMPivot Query

</td><td>

Runs the CMPivot query and retrieves the operation IDs from the MECM server.

</td></tr><tr><td>

Run MECM Script

</td><td>

Runs the MECM script and returns the operation ID from the MECM server.

</td></tr><tr><td>

Look up MECM Script by Name

</td><td>

Retrieves the Globally Unique Identifier \(GUID\) of the MECM script from the MECM server.

</td></tr><tr><td>

Look up MECM Script Response by Operation ID

</td><td>

Retrieves the MECM script response from the MECM server.

</td></tr><tr><td>

Look up MECM Script Execution Response

</td><td>

Retrieves the MECM Script Execution Response from the MECM server.

</td></tr><tr><td rowspan="4">

Data Management**Note:** These actions are available only when the [Client Software Distribution 2.0 application](csd-app-2.md) is installed.

</td><td>

Look up Configuration Data

</td><td>

Retrieves the configuration data from the requested item or software configuration.

</td></tr><tr><td>

Prepare Deployment Data

</td><td>

Prepares the deployment data for the requested item.

</td></tr><tr><td>

Prepare Revocation Data

</td><td>

Prepares the revocation data for the requested item.

</td></tr><tr><td>

Store Discovered Data

</td><td>

Stores the applications and deployment data in the corresponding tables.

</td></tr><tr><td rowspan="5">

Deployments

</td><td>

Add device collection to application

</td><td>

Adds a Device Collection to a targeted application in Microsoft Endpoint Configuration Manager. **Note:** The application must have at least one deployment type and content distributed to a distribution point before deployment.

</td></tr><tr><td>

Look up Deployments

</td><td>

Retrieves the deployment data from the MECM server.

</td></tr><tr><td>

Remove User Collection from Application

</td><td>

Removes a user collection from an application in the MECM.

</td></tr><tr><td>

Add User Collection to Application

</td><td>

Adds a user collection to a targeted application in MECM. **Note:** The application must have at least one deployment type and content distributed to a distribution point before deployment.

</td></tr><tr><td>

Remove Device Collection from Application

</td><td>

Removes a device collection from an application in MECM.

</td></tr><tr><td rowspan="6">

Device Collections

</td><td>

Add to Device Collection

</td><td>

Adds the named device to the collection specified.

</td></tr><tr><td>

Is Device in Collection

</td><td>

Checks if a device exists in the device collection in the MECM server.

</td></tr><tr><td>

Look up Device Collections

</td><td>

Retrieves the device collection data from the MECM server.

</td></tr><tr><td>

Remove from Device Collection

</td><td>

Removes the specified device from the collection in the MECM server.

</td></tr><tr><td>

Create Device Collection

</td><td>

Creates a new device collection in MECM with a unique collection name.**Note:** Provide values for the following input fields:

-   **Collection Name**: Mandatory input. Name of the collection that is a group of devices or users that you manage together.
-   **Limiting Collection Name**: Optional input. An existing collection that will define which device can be the member of this new collection. Only the devices which are the member of Limiting collection can be added in this new collection. For device collections, default limiting collection is "All Systems".

</td></tr><tr><td>

Delete Device Collection

</td><td>

Deletes a device collection from Microsoft Endpoint Configuration Manager \(MECM\) by Collection ID, avoiding ambiguity from duplicate collection names.

</td></tr><tr><td rowspan="6">

User Collections

</td><td>

Add to User Collection

</td><td>

Adds a user to a collection.

</td></tr><tr><td>

Is User in Collection

</td><td>

Checks if a user exists in a user collection in the MECM server.

</td></tr><tr><td>

Look up User Collections

</td><td>

Retrieves the user collection data from the MECM server.

</td></tr><tr><td>

Remove from User Collection

</td><td>

Removes a user from a collection in the MECM server.

</td></tr><tr><td>

Create User Collection

</td><td>

Creates a new user collection in MECM with a unique collection name.**Note:** Provide values for the following input fields:

-   **Collection Name**: Mandatory input. Name of the collection that is a group of devices or users that you manage together.
-   **Limiting Collection Name**: Optional input. An existing collection that will define which device can be the member of this new collection. Only the devices which are the member of Limiting collection can be added in this new collection. For device collections, default limiting collection is "All Systems".

</td></tr><tr><td>

Delete User Collection

</td><td>

Deletes a user collection from MECM by Collection ID, avoiding ambiguity from duplicate collection names.

</td></tr><tr><td>

Software Management

</td><td>

Create Catalog Item

</td><td>

Creates a catalog item of the specified MECM Application.

</td></tr></tbody>
</table>## Spoke module

The MECM spoke adds the MECM application to your instance. The application includes the following modules and data accessed through the spoke modules stored in the respective tables:

|Module|Description|Table|
|------|-----------|-----|
|Applications|Displays the list of applications from the Microsoft Endpoint Configuration Manager server.|Application \[sn\_ms\_epcfgmgr\_spk\_application\]|
|Configurations|Stores the software configuration details for the applications.|Configuration \[sn\_ms\_epcfgmgr\_spk\_sf\_config\]|
|Server Instances|Stores the details of the servers provided.|Server Instance \[sn\_ms\_epcfgmgr\_spk\_server\]|
|Deployments|Displays the list of deployments from the Microsoft Endpoint Configuration Manager server.|Deployment \[sn\_ms\_epcfgmgr\_spk\_deployment\]|
|Collections|Displays the list of collections from the Microsoft Endpoint Configuration Manager server.|Collection \[sn\_ms\_epcfgmgr\_spk\_collection\]|

**Note:** These modules are available only when the [Client Software Distribution 2.0 application](csd-app-2.md) is installed.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Configure Microsoft Endpoint Configuration Manager and set up the spoke](csd2-conf-sccm.md#).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For information, see MID Server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

