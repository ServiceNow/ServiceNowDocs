---
title: Google Cloud Functions Spoke
description: Manage functions that are attached to events, using your Google Cloud Functions account from ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-05-19"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Google Cloud Functions Spoke

Manage functions that are attached to events, using your Google Cloud Functions account from ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Cloud Functions v1.0.3 is the latest version.

## Supported versions

This spoke was built for the Google Cloud Functions API version v1, but may be compatible with later versions.

## Google Cloud Functions spoke requirements

The Google Cloud Functions spoke requires a custom app that you create in Google Cloud Platform.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Google Identity and Access Spoke](gidentityaccess-spoke.md)
-   [Google Cloud VPC Access Spoke](gcloud-vpc-access.md)
-   [Google Cloud Storage Spoke](gcloudstorage-spoke.md)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Google Cloud Functions spoke provides actions to automate Google Cloud Functions tasks when events occurs in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Function Management|Create Function For Event|Creates a function for an event.|
|Create Function For HTTP|Create a function to process an HTTP request.|
|Delete Function|Deletes the specified function.|
|Generate Download URL|Retrieves details of a signed URL to download source code of the deployed function.|
|Generate Upload URL|Retrieves details of a signed URL for uploading source code of the deployed function.|
|Get Function|Retrieves information about the specified function.|
|Get IAM Policy|Retrieves details of IAM access control policy for a function.|
|Look up Functions|Retrieves a list of functions available in the specified location.|
|Set IAM Policy|Sets the IAM access control policy for the specified function.|
|Update Function|Updates details of the specified function.|
|Location Management|Look up Locations|Retrieves a list of locations available in the specified project.|
|Operation Management|Get Operation|Retrieves details of the specified operation.|
|Look up Operations|Retrieves the list of operations available in the specified project.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Cloud Functions spoke](../task/gcloud-func-setup.md#).

