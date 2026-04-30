---
title: Automation Anywhere Spoke
description: Manage workflows and robotics processes in Automation Anywhere instance from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Automation Anywhere Spoke

Manage workflows and robotics processes in Automation Anywhere instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Automation Anywhere spoke v1.2.1 is the latest version

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Automation Anywhere spoke provides actions to automate Automation Anywhere tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Bot Management|Deploy Bot|Deploys a bot in the bot runner devices.|
|Get Bot|Retrieves details of the specific bot.|
|Look up Bots|Retrieves information about all the bots.|
|Device Management|Get Device Details|Retrieves details of the specific device.|
|Look up Devices|Retrieves details of all the devices.|
|Look up Pool|Retrieves details of the specified pool.|
|Folder Management|Get Folder|Retrieves details of the requested folder.|
|Look up Folders|Retrieves information about all the folders.|
|Queue Management|Look up Queues Stream|Retrieves all queues for the Enterprise Control Room.|
|Look up Work Items in Queue|Retrieves details of all the work items in a queue.|
|User Management|Look up User|Retrieves details of the requested user.|
|Look up Users Stream|Retrieves details of all the users.|

**Note:** Only users with bot runner or admin role can execute the spoke actions.

## Spoke module

The Automation Anywhere spoke adds the Automation Anywhere application to your instance and includes the Authentication module. In this module, you should provide details in the default credential record to authentication the ServiceNow requests. See [Create a Credential record for the Automation Anywhere spoke](../task/cred-automation-anywhr-1.md) for more information.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Automation Anywhere spoke](../task/setup-auto-anywhr.md#).

