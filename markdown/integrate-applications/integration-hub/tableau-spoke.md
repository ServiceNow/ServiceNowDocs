---
title: Tableau spoke
description: The Tableau spoke provides actions to view and analyze meaningful usage data for software subscriptions so that you can reclaim stale licenses.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Tableau spoke

The Tableau spoke provides actions to view and analyze meaningful usage data for software subscriptions so that you can reclaim stale licenses.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Tableau API version v3.21, but might be compatible with later versions.

## Spoke requirements

-   Tableau Cloud account
-   Tableau Cloud Role required: Site administrator
-   JSON Web Token \(JWT\) Connected App or Personal access token \(PAT\) to authenticate the ServiceNow instance.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Tableau spoke provides actions to automate Tableau tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|User Management|Look up Users Stream|Retrieves users from the Tableau Cloud application.|
|Remove User|Revokes a user license in the Tableau Cloud application.|
|Organization Management|Get Access Token|Gets the access token to authenticate the API calls.|

## Spoke user roles

The Tableau spoke provides the following user role to control access to data:

|User role|Description|
|---------|-----------|
|Tableau Admin \(sn\_tableau\_spoke.tableau\_admin\)|Creates connections for the Tableau Cloud application.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For more information about setting up the spoke, see [Set up the Tableau spoke](../task/set-up-tableau-spoke.md).

