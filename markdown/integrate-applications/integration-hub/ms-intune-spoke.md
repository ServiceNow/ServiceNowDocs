---
title: Microsoft Intune Spoke
description: Manage devices and applications in the Microsoft Intune account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-12"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Intune Spoke

Manage devices and applications in the Microsoft Intune account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The Microsoft Intune spoke v1.4.1 is the latest version.

**Note:** Deployment of applications on Android devices isn’t supported.

## Supported versions

This spoke was built for the Microsoft Intune Application programming Interface \(API\) version v1, but may be compatible with the later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\)](../../integrationhub/concept/microsoft-azure-ad-spoke.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. For more information on licenses, contact your account manager.

## Spoke subflows

The Microsoft Intune spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Create Software Configuration|Enables a CSD agent to create the software configuration record of the specified Microsoft Intune application.|
|Configure Group|Enables a CSD agent to create and configure the Microsoft Intune group in Intune Admin Portal.|
|Deploy Application|Adds the provided user or device to a group in the Microsoft Intune server.|
|Discover and Store Data|Discovers the data from the Microsoft Intune server and updates the records in the Application \[sn\_ms\_intune\_spoke\_application\], Group \[sn\_ms\_intune\_spoke\_group\], and Deployment \[sn\_ms\_intune\_spoke\_deployment\] tables.|
|Look up Application Details|Retrieves the additional deployment details for applications and updates the respective records in the deployment table.|
|Look up Configuration Data|Retrieves configuration data for the specified requested item or software configuration record.|
|Look up Groups|Returns the list of install groups or uninstall groups associated with given application id.|
|Revoke Application|Removes the provided user or device from the given group in the Microsoft Intune server.|

**Important:** To use these subflows, install the [Client Software Distribution 2.0 application](csd-app-2.md).

## Spoke actions

The Microsoft Intune spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_byh_ftr_fnb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Application Management

</td><td>

Get Managed Application

</td><td>

Retrieves the details of an application.

</td></tr><tr><td>

Look up Application Assignments

</td><td>

Retrieves the application assignment data from the Microsoft Intune server.

</td></tr><tr><td>

Look up Managed Applications

</td><td>

Retrieves a list of all the applications.

</td></tr><tr><td rowspan="7">

Device Management

</td><td>

Delete Managed Device

</td><td>

Deletes a managed device.

</td></tr><tr><td>

Get Managed Device

</td><td>

Retrieves the details of a managed device.

</td></tr><tr><td>

Look up Managed Devices

</td><td>

Retrieves the details of a managed device.

</td></tr><tr><td>

Look up Managed Devices By Application

</td><td>

Retrieves the details of a managed device within an application.

</td></tr><tr><td>

Sync Managed Device

</td><td>

Forces a managed device to check in with Microsoft Intune to retrieve and apply any pending actions, policies, and configuration updates.

</td></tr><tr><td>

Look up Managed Devices By User

</td><td>

Retrieves the details of a managed device for a user.

</td></tr><tr><td>

Update Managed Device

</td><td>

Updates the details of a managed device.

</td></tr><tr><td>

Metadata Retrieval

</td><td>

Look up Application ID

</td><td>

Returns the Application ID for the dynamic input of the Lookup Managed Devices By Application action.

</td></tr><tr><td rowspan="2">

Data Management**Important:** To use these actions, install the [Client Software Distribution 2.0 application](csd-app-2.md).

</td><td>

Look up Configuration Data

</td><td>

Retrieves the configuration data from a requested item or software configuration.

</td></tr><tr><td>

Prepare Software Data

</td><td>

Prepares the software data for the specified requested item that can be used for deployment or revocation.

</td></tr></tbody>
</table>## Spoke module

The Microsoft Intune spoke adds the Microsoft Intune application to your instance and includes these modules:

|Module|Description|Table|
|------|-----------|-----|
|Applications|Displays the list of applications from the Microsoft Intune server.|Application \[sn\_ms\_intune\_spoke\_application\]|
|Groups|Displays the list of groups from the Microsoft Intune server.|Group \[sn\_ms\_intune\_spoke\_group\]|
|Configurations|Stores software configuration details for the applications.|Configuration \[sn\_ms\_intune\_spoke\_sf\_config\]|
|Deployments|Displays the list of deployments on the Microsoft Intune server.|Deployment \[sn\_ms\_intune\_spoke\_deployment\]|
|Server Instances|Stores details of the provider servers.|Server Instance \[sn\_ms\_intune\_spoke\_server\]|

**Important:** To use these modules and tables, install the [Client Software Distribution 2.0 application](csd-app-2.md).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Intune spoke](../task/setup-ms-intune.md#).

