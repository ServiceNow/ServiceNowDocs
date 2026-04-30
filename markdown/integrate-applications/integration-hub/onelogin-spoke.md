---
title: OneLogin Spoke
description: Manage users, passwords, roles, and groups in the OneLogin account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# OneLogin Spoke

Manage users, passwords, roles, and groups in the OneLogin account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

OneLogin v1.0.2 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The OneLogin spoke provides actions to to manage users, passwords, roles, and groups. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Group Management|Look up Groups|Retrieves the list of groups available in the OneLogin account.|
|Password Management|Get Lock Status|Retrieves the lock status of the user in OneLogin.|
|Lock User|Locks the specified user account in OneLogin.|
|Unlock User|Unlocks user in OneLogin.|
|Update Password|Updates the user’s password in OneLogin.|
|User Management|Create User|Creates a user in OneLogin.|
|Get User Details|Retrieves details of the required user in OneLogin.|
|Look up Users|Retrieves details of the required users.|
|Update User|Updates the attributes of a user in OneLogin.|
|User Role Management|Assign Role|Assigns role to user in the OneLogin account.|
|Get Roles by User|Retrieves the role IDs assigned to the user in the OneLogin account.|
|Look up Roles|Retrieves details of the roles.|
|Remove Role|Removes the specified role assigned to a user in OneLogin account.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the OneLogin spoke](../task/setup-oneloginspk.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the **** alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md)

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

