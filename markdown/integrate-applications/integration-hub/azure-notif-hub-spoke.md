---
title: Microsoft Azure Notification Hub Spoke
description: Integrate ServiceNow instance with Microsoft Azure Notification Hub. Manage Azure notification hubs from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure Notification Hub Spoke

Integrate ServiceNow instance with Microsoft Azure Notification Hub. Manage Azure notification hubs from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure Notification Hub spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for Azure Notification Hub version 2023-09-01, but may be compatible with later versions.

## Spoke requirements

-   Storage account in your Microsoft Azure portal for integration with your ServiceNow instance.
-   Register the application in the Microsoft Azure portal and record the access keys and directory IDs.

## Spoke dependencies

If you’re having trouble installing the app, verify that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Flow Designer Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   Microsoft Azure Resource Management Spoke is installed and the connection record configured on your ServiceNow instance.
-   Microsoft Azure Notification Hub SAS connection and credential alias record is configured on your ServiceNow instance.

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Azure Notification Hub Spoke provides actions to automate Azure Notification Hub tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_mzn_ysh_qmb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Installation Management

</td><td>

Create or Update Installation

</td><td>

Creates or updates an installation.

</td></tr><tr><td>

Delete Installation

</td><td>

Deletes an installation.

</td></tr><tr><td>

Look up Installation

</td><td>

Retrieves installation based on the Installation ID.

</td></tr><tr><td>

Update Installation

</td><td>

Partially updates an installation using the JSON-Patch.

</td></tr><tr><td>

Look up Namespaces Stream by Resource Group

</td><td>

Returns the list of available namespaces within a resource group.

</td></tr><tr><td>

Look up Namespaces Stream by Subscription ID

</td><td>

Returns the list of available namespaces within the subscription.

</td></tr><tr><td rowspan="4">

Namespace Management

</td><td>

Look up Namespace

</td><td>

Returns the details of the specified namespace.

</td></tr><tr><td>

Create or Update Namespace

</td><td>

Creates or updates a Notification Hub namespace. **Note:** This operation is idempotent.

</td></tr><tr><td>

Delete Namespace

</td><td>

Deletes an existing namespace. This operation also removes all associated Notification Hubs under the namespace.

</td></tr><tr><td>

Update Namespace

</td><td>

Patches the existing namespace.

</td></tr><tr><td rowspan="4">

Notification Hub Management

</td><td>

Create or Update Notification Hub

</td><td>

Creates or updates a Notification Hub in a namespace.

</td></tr><tr><td>

Delete Notification Hub

</td><td>

Deletes a notification hub associated with a namespace.

</td></tr><tr><td>

Look up Notification Hub

</td><td>

Returns the details of the specified notification hub.

</td></tr><tr><td>

Look up Notification Hubs Stream by Namespace

</td><td>

Returns the list of available notification hubs associated with a namespace.

</td></tr><tr><td rowspan="8">

Registration Management

</td><td>

Create APNS Registration

</td><td>

Creates a registration for an Apple Push Notification service \(APNS\) device. This method generates a registration ID that you can use to retrieve, update, and delete this registration.

</td></tr><tr><td>

Create GCM Registration

</td><td>

Creates a registration for Google Cloud Messaging \(GCM\) device. This method generates a registration ID that you can use to retrieve, update, and delete this registration.

</td></tr><tr><td>

Create Registration ID

</td><td>

Returns a registration ID \(without creating a registration\).

</td></tr><tr><td>

Delete Registration

</td><td>

Deletes a registration.

</td></tr><tr><td>

Look up Registration

</td><td>

Retrieves information about a registration.

</td></tr><tr><td>

Update APNS Registration

</td><td>

Updates an existing APNS registration.

</td></tr><tr><td>

Update GCM Registration

</td><td>

Updates an existing GCM registration.

</td></tr><tr><td>

Look up Registrations Stream

</td><td>

Retrieves all registrations.

</td></tr><tr><td rowspan="3">

Notification Management

</td><td>

Send APNS Native Notification

</td><td>

Sends an APNS native notification through a Notification Hub.

</td></tr><tr><td>

Send GCM Native Notification

</td><td>

Sends a GCM native notification through a Notification Hub.

</td></tr><tr><td>

Send Notification to Device Handle

</td><td>

Sends a notification directly to a device handle \(a valid token as expressed by the Notification type\). **Note:** Users of this API don’t need to use Registrations or Installations.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Azure Notification Hub spoke](../task/setup-azure-notif-hub.md#).

