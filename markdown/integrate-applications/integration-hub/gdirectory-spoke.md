---
title: Google Directory Spoke
description: Manage groups, members, and users in Google Directory from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Directory Spoke

Manage groups, members, and users in Google Directory from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

**Note:**

-   In this version, the alias type is changed to the **Connection and Credential**. The alias type supports multiple connections.
-   If you’re upgrading to Google Directory spoke v1.1.2, you must reconfigure the alias record.

## Spoke version

Google Directory spoke v1.5.2 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Google Directory account requirements

The Google Directory spoke requires a custom app that you create in the Google Developers Console.

## Supported versions

This spoke was built for API version v1, but may be compatible with later versions.

## Spoke subflows

The Google Directory spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope. These webhook subflows perform specific tasks when webhooks execute user resource changes in the Google Directory. Available sample subflows include:

<table id="table_z3x_yx3_dzb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Google Directory User Webhook Subflow

</td><td>

When you update the details of a user in the Google Directory, a webhook notifies your ServiceNow instance. Now, when you execute the `Create Directory User Webhook Subflow`, it creates a subscription and an entry to the `Google Directory Webhook Registries table`.**Note:** To execute the subflow, you must provide the webhook URL that ServiceNow exposes for incoming webhooks in the Test Subflow window. The webhook URL format is`https://<instance-name>.service-now.com/api/sn_googledir_spoke/google_directory_webhook_callbacks/wh_entry`.

</td></tr><tr><td>

Process Google Directory User Webhook Subflow

</td><td>

Processes Google Directory webhooks when user details are updated in the Google directory. The Google Directory provides sample subflows to demonstrate automating Google Directory webhook flows.

</td></tr></tbody>
</table>## Spoke actions

The Google Directory spoke provides actions to automate Google Directory when events occur in ServiceNow. Available actions include:

<table id="table_htp_mmq_glb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Group Management

</td><td>

Create Group

</td><td>

Creates a group.

</td></tr><tr><td>

Delete Group

</td><td>

Deletes a group.

</td></tr><tr><td>

Look up Group Details by Group Email or ID

</td><td>

Retrieves details of the specified groups based on group email or ID.

</td></tr><tr><td>

Look up All Groups Stream

</td><td>

Retrieves the details of all groups.

</td></tr><tr><td>

Look up Groups Stream by Filtering Criteria

</td><td>

Retrieves details of the specified groups based on the provided filter criteria.

</td></tr><tr><td>

Update Group Details

</td><td>

Updates details of the specified group.

</td></tr><tr><td rowspan="6">

Member Management

</td><td>

Add Member To A Group

</td><td>

Adds member to the specified group.

</td></tr><tr><td>

Check Membership of a Group

</td><td>

Checks if the given user is a member of the group email or ID.

</td></tr><tr><td>

Look up Member Details from a Group

</td><td>

Retrieves the details of the required member in the specified group.

</td></tr><tr><td>

Look up Members of a Group by Group Email or ID

</td><td>

Retrieves the details of all member in the specified group.

</td></tr><tr><td>

Remove Member from a Group

</td><td>

Removes the specified member from a group.

</td></tr><tr><td>

Update Member

</td><td>

Updates details of the specified member in a group.

</td></tr><tr><td rowspan="12">

User Management

</td><td>

Create User

</td><td>

Creates a user.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the specified user.

</td></tr><tr><td>

Generate Random Password

</td><td>

Generates a random password with the specified length.

</td></tr><tr><td>

Grant Admin To User

</td><td>

Grants admin privileges to the specified user.

</td></tr><tr><td>

Look up All Users Stream by Customer ID

</td><td>

Retrieves a paginated list of all users in a domain, including deleted users if **showDeleted** is set to `true`.

</td></tr><tr><td>

Look up User Details by User Email or ID

</td><td>

Retrieves details of the given user.

</td></tr><tr><td>

Look up Users Stream by Filtering Criteria

</td><td>

Searches for users matching the filter criteria. This action accepts the query parameter which is a search query combining one or more search clauses.

</td></tr><tr><td>

Reactivate User

</td><td>

Reactivates the specified user.**Note:** Exercise caution while using this action, as it may affect the other user’s account.

</td></tr><tr><td>

Reset User Password

</td><td>

Resets the password of the user.**Note:** Exercise caution while using this action, as it may affect the other user’s account. By default, the **Force Change Password** option is enabled and the user is forced to change the password on the first login.

</td></tr><tr><td>

Revoke Admin from User

</td><td>

Revokes the admin privileges of the specified user.

</td></tr><tr><td>

Suspend User

</td><td>

Suspends the specified user.**Note:** Exercise caution while using this action, as it may affect the other user’s account.

</td></tr><tr><td>

Update User Details

</td><td>

Updates details of the specified user.

</td></tr><tr><td rowspan="2">

Webhook Management

</td><td>

Create Subscription Channel

</td><td>

Creates a subscription channel that watches for changes in the users list.

</td></tr><tr><td>

Stop Subscription Channel

</td><td>

Stops watching resources through the given channel before the expiry of the subscription.

</td></tr><tr><td rowspan="2">

Schema Management

</td><td>

Look up Schema by ID

</td><td>

Retrieves details of the specified schema.

</td></tr><tr><td>

Look up schemas

</td><td>

Retrieves details of all schemas for a customer.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Google Directory spoke](../task/setup-gdirectory.md#).

