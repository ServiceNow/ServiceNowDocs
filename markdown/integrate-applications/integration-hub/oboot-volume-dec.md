---
title: Oracle Boot Volume Spoke
description: Manage boot volumes, backups, and KMS keys in Oracle Boot Volume account from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Oracle Boot Volume Spoke

Manage boot volumes, backups, and KMS keys in Oracle Boot Volume account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Boot Volume v1.0.6 is the latest version.

## Supported versions

This spoke was built for Oracle Boot Volume API version 20160918, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Oracle Cloud IAM Spoke](oracle-iam-1.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Boot Volume spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Boot Volume Backup Management|Change Boot Volume Backup Compartment|Moves a boot volume backup to a different compartment within the same tenancy.|
|Copy Boot Volume Backup|Creates a boot volume backup copy in specified region.|
|Create Boot Volume Backup|Creates a boot volume backup of the specified boot volume.|
|Delete Boot Volume Backup|Deletes a boot volume backup.|
|Get Boot Volume Backup|Gets information for the specified boot volume backup.|
|Look up Boot Volume Backups|Lists the boot volumes backup in the specified compartment.|
|Update Boot Volume Backup|Updates specified boot volume backup.|
|Boot Volume KMS Key Management|Delete Boot Volume KMS Key|Removes the specified boot volume's assigned Key Management encryption key.|
|Get Boot Volume KMS Key|Gets the Key Management encryption key assigned to the specified boot volume.|
|Update Boot Volume KMS Key|Updates the specified volume with a new Key Management encryption key.|
|Boot Volume Management|Attach Boot Volume|Attaches the specified boot volume to the specified instance.|
|Change Boot Volume Compartment|Moves a boot volume to a different compartment within the same tenancy.|
|Create Boot Volume|Creates a boot volume in the specified compartment.|
|Delete Boot Volume|Deletes the specified boot volume.|
|Detach Boot Volume|Detaches a boot volume from an instance.|
|Get Boot Volume|Gets information for the specified boot volume.|
|Get Boot Volume Attachment|Gets information about the specified boot volume attachment.|
|Look up Boot Volume Attachments|Lists the boot volume attachments in the specified compartment.|
|Look up Boot Volumes|Lists the boot volumes in the specified compartment.|
|Update Boot Volume|Updates the specified boot volume.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Boot Volume spoke](../task/oboot-vol-setup-dec.md).

