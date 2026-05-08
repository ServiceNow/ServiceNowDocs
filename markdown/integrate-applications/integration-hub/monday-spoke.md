---
title: monday.com Spoke
description: The monday.com spoke provides actions to view and analyze meaningful usage data for monday.com software subscriptions. Analyze usage for a monday.com account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# monday.com Spoke

The monday.com spoke provides actions to view and analyze meaningful usage data for monday.com software subscriptions. Analyze usage for a monday.com account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke requirements

monday.com admin account.

## Spoke version

monday.com v1.1.5 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The monday.com spoke provides actions to automate monday.com tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_w1l_m1s_2pb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="10">

Board Management

</td><td>

Add Subscribers to Board

</td><td>

Adds the specified subscribers to a board.

</td></tr><tr><td>

Archive Board

</td><td>

Archives the specified board.

</td></tr><tr><td>

Create Board

</td><td>

Creates a board.

</td></tr><tr><td>

Delete Board

</td><td>

Deletes the specified board.

</td></tr><tr><td>

Delete Subscribers from Board

</td><td>

Deletes the specified subscribers from a board.

</td></tr><tr><td>

Duplicate Board

</td><td>

Creates duplicates of the specified board.

</td></tr><tr><td>

Look up Board Activities Stream

</td><td>

Retrieves the activities of the specified board.

</td></tr><tr><td>

Look up Board by ID

</td><td>

Retrieves the details of the specified board.

</td></tr><tr><td>

Look up Boards Stream

</td><td>

Retrieves a list of the boards.

</td></tr><tr><td>

Update Board Description

</td><td>

Updates the description of the specified board.

</td></tr><tr><td rowspan="3">

Column Management

</td><td>

Create Column

</td><td>

Creates a column in the specified board.

</td></tr><tr><td>

Look up Columns by Board ID

</td><td>

Retrieves details of all columns in the specified board.

</td></tr><tr><td>

Update Column Title

</td><td>

Updates the title of the specified column.

</td></tr><tr><td>

Column Values Management

</td><td>

Look up Column Values

</td><td>

Retrieves details of the column values in the specified board and item.​

</td></tr><tr><td rowspan="4">

File Management

</td><td>

Add File to File Column

</td><td>

Adds a file to the file column of a specific item.​

</td></tr><tr><td>

Add File to Update

</td><td>

Adds a file to the specified update.

</td></tr><tr><td>

Look up File by ID

</td><td>

Retrieves details of the specified file.

</td></tr><tr><td>

Look up Files by Board ID

</td><td>

Retrieves details of files in the specified board.

</td></tr><tr><td rowspan="6">

Group Management

</td><td>

Archive Group

</td><td>

Archives the specified group.

</td></tr><tr><td>

Create Group

</td><td>

Creates an empty group in the specified board.​

</td></tr><tr><td>

Delete Group

</td><td>

Deletes the specified group.

</td></tr><tr><td>

Duplicate Group

</td><td>

Creates a duplicate of the specified group.

</td></tr><tr><td>

Look up Group by ID

</td><td>

Retrieves the group details for the specified board ID and group ID.

</td></tr><tr><td>

Look up Groups by Board ID

</td><td>

Retrieves the details of all the groups in a board.

</td></tr><tr><td rowspan="10">

Item Management

</td><td>

Archive Item

</td><td>

Archives the specified item.

</td></tr><tr><td>

Clear Item's Updates

</td><td>

Clears all updates on a specific item, including replies and likes.​

</td></tr><tr><td>

Create Item

</td><td>

Creates an item in a group.

</td></tr><tr><td>

Create Subitem

</td><td>

Creates a new subitem for the specified parent item. **Note:** For creating subitems via the API, the board should already have a subitems column, or at least one subitem created.

</td></tr><tr><td>

Delete Item

</td><td>

Deletes the specified item from a group.

</td></tr><tr><td>

Duplicate Item

</td><td>

Creates a duplicate of the specified item in a group.​

</td></tr><tr><td>

Look up Items

</td><td>

Retrieves details of the items in the specified board and group.​

</td></tr><tr><td>

Look up Items by IDs

</td><td>

Retrieves details of the specified items.

</td></tr><tr><td>

Look up Items Stream by Board ID

</td><td>

Retrieves the items for the specified board.

</td></tr><tr><td>

Move Item to Group

</td><td>

Moves an item between groups in the same board.

</td></tr><tr><td>

Notification Management

</td><td>

Create Notification

</td><td>

Creates a notification with the specified details.

</td></tr><tr><td rowspan="4">

Tag Management

</td><td>

Create or Look up Tag

</td><td>

Creates a tag when the specified type of tag does not exist. If the tag already exists, the details of the tag are retrieved.

</td></tr><tr><td>

Look up Shareable or Private Tags

</td><td>

Retrieves details of the board-specific private or and shareable tags.​

</td></tr><tr><td>

Look up Tag by ID

</td><td>

Retrieves details of the specified public tag that is displayed on the main boards. By default, the main boards are accessible to all member-level and viewer-level users.

</td></tr><tr><td>

Look up Tags

</td><td>

Retrieves details of all the public tags that are displayed on the main boards. By default, the main boards are accessible to all member-level and viewer-level users.​

</td></tr><tr><td rowspan="2">

Team Management

</td><td>

Look up Team by ID

</td><td>

Retrieves details of the specified team.​

</td></tr><tr><td>

Look up Teams

</td><td>

Retrieves details of the teams.​

</td></tr><tr><td rowspan="3">

Update Management

</td><td>

Create an Update

</td><td>

Adds an update to the specified item.

</td></tr><tr><td>

Delete an Update

</td><td>

Deletes the specified update of an item.

</td></tr><tr><td>

Look up Updates Stream

</td><td>

Retrieves the list of updates.​

</td></tr><tr><td rowspan="3">

User Management

</td><td>

Look up Users

</td><td>

Retrieves details of the specified type of users.​

</td></tr><tr><td>

Look up Users by IDs

</td><td>

Retrieves details of the specified users.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves the list of the users.​

</td></tr><tr><td rowspan="2">

Webhook Management

</td><td>

Create Webhook

</td><td>

Creates a webhook subscription based on the specified event.​

</td></tr><tr><td>

Delete Webhook

</td><td>

Deletes the specified webhook.

</td></tr><tr><td rowspan="5">

Workspace Management

</td><td>

Add Teams to Workspace

</td><td>

Adds the specified teams to the required workspace.​

</td></tr><tr><td>

Add Users to Workspace

</td><td>

Adds the specified users to the required workspace and defines if the users will be added as regular subscribers or as owners of the workspace.​

</td></tr><tr><td>

Create Workspace

</td><td>

Creates a workspace.

</td></tr><tr><td>

Delete Teams from Workspace

</td><td>

Deletes the specified teams from the required a workspace.​

</td></tr><tr><td>

Delete Users from Workspace

</td><td>

Deletes the specified users from a workspace.​

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Spoke module

The monday.com spoke adds Monday Spoke application to your instance and includes the following modules:

|Module|Description|
|------|-----------|
|Users|Displays the list of users in monday.com.|
|Boards|Displays the list of all boards from monday.com.|
|Routing Policies|Displays the list of routing policies for monday.com spoke.|
|Webhook Registry|Displays the list of webhook registries for monday.com spoke.|

## Spoke subflows

The monday.com spoke provides subflows in the Published state to integrate with monday.com application.

|Category|Subflow|Description|
|--------|-------|-----------|
|Webhook Management|Process Monday Webhooks|Runs when an associated subscribed event triggers in monday.com|

## Spoke table

The monday.com spoke adds the following table:

|Table|Description|
|-----|-----------|
|Monday Boards|Stores all the boards present in your monday.com account.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the monday.com spoke](../task/setup-monday.md#).

