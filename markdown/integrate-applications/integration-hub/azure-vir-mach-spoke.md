---
title: Microsoft Azure Virtual Machine Spoke
description: Manage the Microsoft Azure Virtual Machine \(VM\) from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure Virtual Machine Spoke

Manage the Microsoft Azure Virtual Machine \(VM\) from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The Microsoft Azure Virtual Machine spoke v2.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Step - Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Microsoft Azure Resource Management Spoke v2.0. After installing, you must configure the connection for the Microsoft Azure Resource Management Spoke v2.0 connection record to request OAuth tokens from the Microsoft Azure portal.

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for the Application Programming Interface \(API\) version 2024-03-01, but may be compatible with the later versions.

## Spoke requirements

-   Microsoft Azure Resource Management spoke \(com.sn.ms.azure.resource.mgmt.spoke\)
-   Microsoft Azure Virtual Network spoke \(com.sn.ms.azure.virtual.network.spoke\)
-   Microsoft Azure Managed Storage spoke \(com.sn.ms.azure.managed.storage.spoke\)

## Spoke flows and subflows

This spoke has no flows or subflows.

## Spoke actions

The Microsoft Azure Virtual Machine spoke provides actions to automate the Microsoft Azure Virtual Machine tasks when events occur in the ServiceNow instance. Available actions include:

<table id="table_ejh_j5z_wlb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Image Management

</td><td>

Create Image from Virtual Machine

</td><td>

Creates an image from an existing virtual machine.

</td></tr><tr><td>

Delete Image

</td><td>

Deletes an image.**Note:** Use the Look up Operational Status of Resource' action from Azure Resource Management spoke to find the status of the operation.

</td></tr><tr><td>

Look up Image

</td><td>

Retrieves image information from a specified resource group.

</td></tr><tr><td>

Look up Images Stream by Resource Group

</td><td>

Retrieves the list of images under a Resource Group.

</td></tr><tr><td>

Look up Images Stream by Subscription ID

</td><td>

Retrieves the list of images in the subscription.

</td></tr><tr><td>

Set Tags on Image

</td><td>

Sets the tags on image.**Note:** Use the Look up Operational Status of Resource' action from Azure Resource Management spoke to find the status of the operation.

</td></tr><tr><td rowspan="16">

Virtual Machine Management

</td><td>

Attach Disk

</td><td>

Attaches data disk to the virtual machine.

</td></tr><tr><td>

Create virtual machine.

</td><td>

Creates a virtual machine.

</td></tr><tr><td>

Create Virtual Machine from Image

</td><td>

Creates virtual machines from an image.

</td></tr><tr><td>

Deallocate Virtual Machine

</td><td>

Shuts down the virtual machine and releases the compute resources.

</td></tr><tr><td>

Delete Virtual Machine

</td><td>

Deletes a virtual machine.

</td></tr><tr><td>

Detach Disk

</td><td>

Detaches data disk from the virtual machine.**Note:** Use the Look up Operational Status of Resource' action from Azure Resource Management spoke to find the status of the operation.

</td></tr><tr><td>

Generalize Virtual Machine

</td><td>

Sets the OS state of the virtual machine to generalized.

</td></tr><tr><td>

Look up Virtual Machine

</td><td>

Retrieves information about a virtual machine.

</td></tr><tr><td>

Look up Virtual Machine Runtime Details

</td><td>

Retrieves the information about the run-time state of a virtual machine.

</td></tr><tr><td>

Look up Virtual Machines Stream by Resource Group

</td><td>

Retrieves the list of virtual machines under a Resource Group.

</td></tr><tr><td>

Look up Virtual Machines Stream by Subscription ID

</td><td>

Retrieves all virtual machines in the specified subscription.

</td></tr><tr><td>

Power Off Virtual Machine

</td><td>

Powers off a virtual machine or stops it.

</td></tr><tr><td>

Redeploy Virtual Machine

</td><td>

Shuts down the virtual machine, moves it to a new node, and powers it back on.

</td></tr><tr><td>

Resize Virtual Machine

</td><td>

Resizes the specified virtual machine. **Note:** This operation can take a while to complete.

</td></tr><tr><td>

Restart Virtual Machine

</td><td>

Restarts a virtual machine.

</td></tr><tr><td>

Start Virtual Machine

</td><td>

Starts a virtual machine.

</td></tr><tr><td>

Virtual Machine Image Resource Management

</td><td>

Look up Virtual Machine Image

</td><td>

Gets a virtual machine image.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

## Set up the Microsoft Azure Virtual Machine Spoke

To execute the actions of the Microsoft Azure Virtual Machine Spoke, you must first install and configure the Microsoft Azure Resource Management Spoke. No separate configuration of the Microsoft Azure Virtual Machine Spoke is necessary. To view the procedure to set up the Microsoft Azure Resource Management Spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#).

