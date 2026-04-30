---
title: Oracle Block Storage Spoke
description: Manage block storage and volumes in the Oracle Block Storage account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Block Storage Spoke

Manage block storage and volumes in the Oracle Block Storage account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Block Storage spoke v1.0.4 is the latest version.

## Supported versions

This spoke was built for Oracle Block Storage API version 20160918, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Oracle Cloud IAM Spoke](oracle-iam-1.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Block Storage spoke provides actions to automate Oracle Block Storage tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Volume Backup Management|Change Volume Backup Compartment|Moves a volume backup into a different compartment within the same tenancy.|
|Create Volume Backup|Creates a new backup of the specified volume.|
|Delete Volume Backup|Deletes a volume backup.|
|Get Volume Backup|Retrieves information about the specified volume backup.|
|Look up Volume Backups|Retrieves list of the volume backups in the specified compartment.|
|Update Volume Backup|Updates the specified volume backup.|
|Volume Backup Policy Management|Create Volume Backup Policy|Creates a user defined backup policy.|
|Delete Volume Backup Policy|Deletes a user defined backup policy.|
|Get Volume Backup Policy|Retrieves details of the specified volume backup policy.|
|Look up Volume Backup Policies|Retrieves list of the volume backup policies in the specified compartment.|
|Update Volume Backup Policy|Updates a user defined backup policy.|
|Volume Group Backup Management|Change Volume Group Backup Compartment|Moves a volume group backup into a different compartment within the same tenancy.|
|Create Volume Group Backup|Creates a new backup volume group of the specified volume group.|
|Delete Volume Group Backup|Deletes the specified volume group backup.|
|Get Volume Group Backup|Retrieves details of the specified volume group backup.|
|Look up Volume Group Backups|Retrieves list of the volume group backups in the specified compartment.|
|Update Volume Group Backup|Updates the specified volume group backup.|
|Volume Group Management|Change Volume Group Compartment|Moves a volume group into a different compartment within the same tenancy.|
|Create Volume Group|Creates a new volume group in the specified compartment.|
|Delete Volume Group|Deletes the specified volume group.|
|Get Volume Group|Retrieves details of the specified volume group.|
|Look up Volume Groups|Retrieves list of the volume groups in the specified compartment.|
|Update Volume Group|Updates the specified volume group.|
|Volume Management|Attach Volume|Attaches the specified storage volume to the specified instance.|
|Change Volume Compartment|Moves a volume into a different compartment within the same tenancy.|
|Create Volume|Creates a new volume in the specified compartment.|
|Delete Volume|Deletes the specified volume.|
|Detach Volume|Detaches a storage volume from an instance.|
|Get Volume|Retrieves details of the specified volume.|
|Get Volume Attachment|Retrieves information about the specified volume attachment.|
|Look up Volume Attachments|Retrieves list of the volume attachments in the specified compartment.|
|Look up Volumes|Retrieves list of the volume in the specified compartment.|
|Update Volume|Updates the specified volume in the specified compartment.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Block Storage spoke](../task/oblk-strg-vol-decsetup.md).

