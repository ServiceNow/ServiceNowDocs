---
title: Microsoft Azure Blob Storage Spoke
description: Manage Azure blobs and containers from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Azure Blob Storage Spoke

Manage Azure blobs and containers from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Azure Blob Storage spoke v2.0.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Step - JSON Parser \(com.glide.hub.action\_step.jsonparser\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Supported versions

This spoke was built for API version 2023-11-03, but may be compatible with later versions.

## Spoke requirements

-   Storage account in your Microsoft Azure portal for integration with your ServiceNow instance.

    **Note:** Verify that you have the Storage Blob Data Owner role.

    To assign the role:

    1.  Log in to your storage account and navigate to Access Control\(IAM\).
    2.  Select the Add a role assignment and select the Storage Blob Data Owner role.
    3.  Assign access to the required Azure AD user, group, or service principle option. Select the email address of the Azure account and save the changes.

        ![Add the Storage Blob Data Owner role](../image/azure-blob-role.png)

    For more information, see [Use the Azure portal to assign an Azure role for access to blob and queue data](https://docs.microsoft.com/en-us/azure/storage/common/storage-auth-aad-rbac-portal).

-   Record and save the access keys and Directory ID for later use.

## Spoke subflows

The Azure Blob Storage spoke provides sample subflows to demonstrate automating the Azure Blob Storage tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Subflow|Description|
|-------|-----------|
|Move Blob|Moves a blob from source container to destination container.|
|Rename Blob|Renames the specified blob.|
|Look up Blobs Stream|Retrieves the details of all blobs in a container.|
|Look up Containers Stream|Retrieves a list of containers under the specified storage account.|

## Spoke actions

The Azure Blob Storage spoke provides actions to automate Azure Blob Storage tasks when events occur in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Blob Management|Attach Blob to ServiceNow Record|Attaches a blob to the ServiceNow record.|
|Copy Blob|Copies a blob from one container to another container.|
|Delete Blob|Deletes the specified blob.|
|Lease Blob|Creates a lock on a blob for write and delete operations.|
|Look up Blob|Retrieves details of the specified blob.|
|Look up Blobs|Retrieves details of all blobs in a container.|
|Release Lease on Blob|Releases a lock on a blob.|
|Snapshot Blob|Creates a snapshot for the specified blob.|
|Upload Attachment to Container|Uploads a blob in specified container.|
|Container Management|Create Container|Creates a container under the specified account.|
|Delete Container|Deletes a container.|
|Lease Container|Creates a lock on the container for delete operations.|
|Look up Container|Retrieves details of the specified container.|
|Look up Containers|Retrieves list of the containers under the specified storage account.|
|Release Lease on Container|Releases a lock on a container.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft Azure Blob Storage Spoke](../task/setup-blob-spoke.md#).

