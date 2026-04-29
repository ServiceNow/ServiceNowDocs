---
title: Asana Spoke
description: The Asana spoke provides actions to view and analyze meaningful usage data for Asana software subscriptions based on stories created by the user. Use this data to determine which licenses are stale so that you can reclaim these licenses and realize potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Asana Spoke

The Asana spoke provides actions to view and analyze meaningful usage data for Asana software subscriptions based on stories created by the user. Use this data to determine which licenses are stale so that you can reclaim these licenses and realize potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Asana spoke v1.0.2 is the latest version.

## Spoke requirements

Asana account with an Admin role.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream Inputs \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses if used outside the spoke implementation.

## Spoke actions

The Asana spoke provides actions to automate Asana tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Workspace Management|Look up Workspaces|Retrieves details of all workspaces.|
|Get Workspaces \(metadata\)|Retrieves the list of the workspaces for the user. This action is used to create dynamic choices for the input **Workspace** in other spoke actions.|
|Task Management|Look up Workspaces Tasks|Retrieves list of all workspace tasks.|
|Look up Stories Stream|Retrieves details of the stories.|
|User Management|Look up Users Stream|Retrieves details of all users.|
|Remove User from Workspace|Removes a user from a workspace.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

