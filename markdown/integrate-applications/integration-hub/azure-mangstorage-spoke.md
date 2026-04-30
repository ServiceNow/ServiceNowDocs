---
title: Microsoft Azure Managed Storage Spoke
description: Manage the Microsoft Azure managed disks from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Azure Managed Storage Spoke

Manage the Microsoft Azure managed disks from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The Microsoft Azure Managed Storage spoke v2.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Microsoft Azure Resource Management spoke \(com.sn.ms.azure.resource.mgmt.spoke\) is installed and configured on your ServiceNow instance.
-   ServiceNow Integration Hub Action Template - Data Stream
-   ServiceNow Integration Hub Action Step - get Connection Info
-   Microsoft Azure Virtual Network spoke is installed and configured on your ServiceNow instance.

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for the API version 2023-10-02, but may be compatible with the later versions.

## Spoke requirements

-   User account with full access to the Microsoft Azure managed disks.
-   Microsoft Azure Resource Management spoke

## Spoke flows and subflows

This spoke has no flows or subflows.

## Spoke actions

The Microsoft Azure Managed Storage spoke provides actions to automate the Microsoft Azure disks and disk snapshots when events occur in the ServiceNow instance. Available actions include:

<table id="table_etd_y55_wlb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="12">

Disk Management

</td><td>

Revoke Access from Disk

</td><td>

Revokes access from the specified disk.

</td></tr><tr><td>

Create Managed Upload Disk

</td><td>

Creates a disk with the specified upload size.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Update Disk Size

</td><td>

Updates the size of the specified disk.

</td></tr><tr><td>

Set Disk Tags

</td><td>

Updates the tags of the specified disk. The provided tags will replace any existing tags on the disk.

</td></tr><tr><td>

Grant Access to Disk

</td><td>

Grants access to the specified disk.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Update Disk Storage Account

</td><td>

Updates the details of the storage account associated with the specified disk.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Delete Disk

</td><td>

Deletes the specified disk.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Create Managed Disk

</td><td>

Creates a disk with the specified disk size in GB.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Look up Disk

</td><td>

Retrieves information about the specified disk in the specified resource group.

</td></tr><tr><td>

Look up Disks Stream by Resource Group

</td><td>

Retrieves the list of disks in the specified Resource Group.

</td></tr><tr><td>

Create Managed Disk from Snapshot

</td><td>

Creates a disk using a snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Look up Disks Stream by Subscription ID

</td><td>

Retrieves the list of disks in the specified Azure Subscription.

</td></tr><tr><td rowspan="10">

Disk Snapshot Management

</td><td>

Grant Access to Snapshot

</td><td>

Grants access to the specified snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Look up Snapshots Stream by Resource Group

</td><td>

Retrieves the list of snapshots in the specified Resource Group.

</td></tr><tr><td>

Update Snapshot Size

</td><td>

Updates the size of the specified snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Update Snapshot Storage Account

</td><td>

Updates tags of the specified snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Look up Snapshots Stream by Subscription ID

</td><td>

Retrieves the list of snapshots in the specified Azure Subscription.

</td></tr><tr><td>

Create Snapshot

</td><td>

Creates a snapshot from a disk.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Delete Snapshot

</td><td>

Deletes the specified snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Revoke Access from Snapshot

</td><td>

Revokes access to the specified snapshot.**Tip:** Find the current status of an operation by using the 'Look up Operational Status of Resource' action from Azure Resource Management spoke.

</td></tr><tr><td>

Look up Snapshot

</td><td>

Retrieves specified snapshot information in the specified resource group.

</td></tr><tr><td>

Set Snapshot Tags

</td><td>

Updates tags of the specified snapshot. The provided tags will replace any existing tags on the snapshot.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Azure Resource Management spoke](../task/setup-res-mngmt.md#) and .

