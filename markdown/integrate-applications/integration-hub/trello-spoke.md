---
title: Trello Spoke
description: Manage Trello Enterprise subscriptions using your ServiceNow instance. Analyze data usage for Trello enterprise and reclaim idle subscriptions.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Trello Spoke

Manage Trello Enterprise subscriptions using your ServiceNow instance. Analyze data usage for Trello enterprise and reclaim idle subscriptions.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Trello spoke v1.4.0 is the latest version.

## Spoke requirements

-   Trello Enterprise admin access
-   Ensure that your Trello subscription is linked to Atlassian account.
-   Ensure that your authorized account has both Trello Enterprise admin and Atlassian account admin access.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Trello spoke provides the Upsert Trello Board flow to check if a new board has been created in the Trello Boards table, or if an existing board has been updated and accordingly synchronizes it in Trello. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The Trello spoke provides the Process Trello Webhook subflow to retrieve data based on the changes happening in Trello. The subflow is executed when the webhook is triggered. To customize the sample flow, copy it to the required application scope.

## Spoke actions

The Trello spoke provides actions to automate Trello tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Retrieve Actions|Look up Action by ID|Retrieves details of the required action.|
|Look up Actions by Board ID|Retrieves details of actions from the specified board.|
|Look up Actions by Card ID|Retrieves details of the actions from the specified card.|
|Look up Actions by List ID|Retrieves details of the actions from the specified card.|
|Look up Actions by Organization ID|Retrieves details of actions from the specified organization.|
|Update Action|Updates content of a comment for an action.|
|Attachment Management|Create Attachment on Card|Attaches a file to the required card.|
|Delete Attachment by ID|Deletes the specified attachment.|
|Look up Attachment by ID|Retrieves details of the required attachment.|
|Look up Attachments by Card ID|Retrieve attachments on card.|
|Board Management|Create Board|Creates a board with the provided details.|
|Delete Board by ID|Deletes the specified board.|
|Look up Board by ID|Retrieves details of the required board.|
|Look up Boards by Organization ID|Retrieves details of boards from the specified organization.|
|Update Board|Updates details of the specified board.|
|Card Management|Create Card|Creates a card with the provided details.|
|Delete Card by ID|Deletes the specified card.|
|Look up Card by ID|Retrieves details of the required card.|
|Update Card|Updates details of the card.|
|Checklist Management|Create Checklist|Creates a checklist with the provided details.|
|Look up Checklist by ID|Retrieves details of the required checklist.|
|Custom Field Management|Create Custom Field|Creates a custom field with the provided details.|
|Look up Custom Field by ID|Retrieves details about the required custom field.|
|Label Management|Look up Label by ID|Retrieves details of the required label.|
|List Management|Create List|Creates a list with the provided details.|
|Look up List by ID|Retrieves details of the specified list.|
|Organization Management|Look up Organization by ID|Retrieves details of the required organization.|
|Sticker Management|Add Sticker to Card|Adds a sticker to the required card.|
|Delete Sticker by ID|Deletes the specified sticker.|
|Look up Sticker by ID|Retrieves details of the required sticker.|
|Look up Stickers by Card ID|Retrieves details of stickers on a card.|
|Update Sticker|Updates details of the specific sticker.|
|User Management|Look up Enterprise ID|Retrieves the organization ID of the authenticated user account.|
|Look up Enterprise Members Stream |Retrieves details of all members in an enterprise organization.|
|Update Active Status of Enterprise Member|Updates the active status of the specified member in an enterprise.|
|Update License Status of Enterprise Member|Updates whether the provided member should use one of the enterprise's available licenses or not.|
|Webhook Management|Create Webhook|Creates a webhook with the provided details.|
|Delete Webhook by ID|Deletes the specified webhook.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Spoke modules

The Trello spoke adds the Trello Spoke application to ServiceNow instance. The Trello Spoke application includes these modules:

<table id="table_hwl_1v1_pxb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boards

</td><td>

Enables you to create boards in Trello. When you create a record here, the Upsert Trello Board flow is triggered and creates or updates the board details in Trello.

</td></tr><tr><td colspan="2">

Remote Table

</td></tr><tr><td>

Users

</td><td>

Enables you to access the Trello user details.

</td></tr><tr><td colspan="2">

Webhook

</td></tr><tr><td>

Routing Policies

</td><td>

Stores the routing policies of the Trello webhook. A default record is available along with the spoke. You can customize the default routing policy as per your requirement.

</td></tr><tr><td>

Webhook Registries

</td><td>

Stores the webhook registries. The webhook registry registers a Trello webhook in ServiceNow to notify ServiceNow when certain events occur in Trello. You can create a webhook for the required board. When any changes occur in the board, the webhook is triggered, the Process Trello Webhook subflow is executed, and the board changes can be viewed in the subflow logs.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Generate Trello API key and token](../../../product/software-asset-management2/task/trello-setup.md#) and [Create a Trello connection](../../../product/software-asset-management2/task/trello-setup.md#).

