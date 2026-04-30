---
title: Microsoft Azure Artifacts Spoke
description: Manage Microsoft Azure Artifacts from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Azure Artifacts Spoke

Manage Microsoft Azure Artifacts from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure Artifacts spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Microsoft Azure Artifacts 6.0-preview.1, but may be compatible with later versions.

## Spoke requirements

Azure Devops Account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Azure Artifacts spoke provides actions to automate Microsoft Azure Artifacts tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Artifact Management|Get Package Details|Retrieves details of the specified package.|
|Get Package Version Details|Retrieves version details of the specified package.|
|Look up Package Versions|Retrieves a list of package versions.|
|Look up Packages|Retrieves a list of packages.|
|Change Tracking Management|Get Feed Change|Retrieves details of the current state of a feed.|
|Look up Feed Changes|Retrieves a list of changes of a feed.|
|Look up Package Changes|Retrieves a list of packages that changed in a feed.|
|Feed Management|Create Feed|Creates a feed to handle various package types.|
|Delete Feed|Removes the feed and all the related packages.|
|Get Feed Details|Retrieves the details of the feed.|
|Look up Feeds|Retrieves a list of feeds.|
|Update Feed|Updates the specified feed.|
|Metadata Retrieval|Look up Package IDs|Retrieves the metadata of a list of package IDs.|
|Look up Package Version IDs|Retrieves the metadata of a list of package version IDs.|
|Look up Projects|Retrieves a list of all project within an organization.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Microsoft Azure Artifacts spoke](../task/setup-azure-artifacts.md#).

