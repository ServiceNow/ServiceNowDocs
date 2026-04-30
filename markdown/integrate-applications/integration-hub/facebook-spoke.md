---
title: Workplace from Facebook Spoke
description: Manage users, groups, and notifications in Workplace from Facebook account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workplace from Facebook Spoke

Manage users, groups, and notifications in Workplace from Facebook account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

**Note:** Workplace from Facebook is compatible with ServiceNow version, Paris with Patch 3 and later.

## Spoke version

Workplace from Facebook spoke v4.2.0is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke subflows

The Workplace from Facebook spoke provides a sample subflow, Fetch Workplace from Facebook Groups that demonstrates automating group management tasks. To customize the sample flow, copy it to the required application scope.

## Spoke actions

The Workplace from Facebook spoke provides actions to manage users, groups, and notifications. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Group Management|Add User To Group|Adds a user to a group in Workplace from Facebook.|
|Create Group|Creates a group in Workplace from Facebook.|
|Deactivate Groups|Deactivates groups that have not been updated during the last execution of the Fetch Workplace from Facebook Groups subflow.|
|Lookup Group ID|Retrieves the group ID for a given group name in Workplace from Facebook.|
|Lookup Groups|List all groups in Workplace from Facebook.|
|Remove User From Group|Removes a user from a group in Workplace from Facebook.|
|Group Post Management|Post Message|Posts a message to a Workplace from Facebook group.|
|Post Picture|Posts an image and message to a Workplace from Facebook group.|
|Post Change Details|Posts change request details in a Workplace from Facebook group.|
|Post Incident Details|Posts incident details in a Workplace from Facebook group.|
|Post Problem Details|Posts problem details in a Workplace from Facebook group.|
|User Management|Lookup User ID|Retrieves the user ID from a registered email in Workplace from Facebook.|
|Look up Organization Members Stream|Retrieves a list of  users in  Workplace from Facebook.|
|Deactivate a User|Deactivates a Workplace from Facebook user.|
|Create User|Creates a user in Workplace from Facebook.|
|Look up User|Retrieves user details based on the user's registered email in Workplace from Facebook.|
|Event Management|Look up Events Stream|Retrieves events of the Workplace from Facebook community.|
|Knowledge Library Category Management|Look up Knowledge Library Categories Stream|Retrieves the knowledge library categories created in Workplace from Facebook.|
|Message Management|Look up Conversations Stream|Retrieves conversations of the specified user.|
|Look up Feeds Stream|Retrieves feeds on the specified group.|
|Send Change Details|Sends change details to user in a Workplace from Facebook group.|
|Send Image|Sends an image or file to users in Workplace from Facebook.|
|Send Incident Details|Sends incident details to user in a Workplace from Facebook group.|
|Send Message|Sends messages to users in Workplace from Facebook.|
|Send Problem Details|Sends problem details to user in a Workplace from Facebook group.|

## Spoke modules

The Workplace from Facebook spoke adds a Workplace from Facebook application to your ServiceNow instance and includes these modules:

<table id="table_s4g_hlj_smb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Credentials

</td><td>

Displays the credentials records created for the Workplace from Facebook spoke. You can create credential records as per your requirement. For example, a credential record for each Workplace from Facebook instance.

</td></tr><tr><td>

Install on your Workplace

</td><td>

Displays the default credential record to set up the Workplace from Facebook spoke. For more information, see [Set up Workplace from Facebook spoke](../task/set-up-fb-wp.md#).

</td></tr><tr><td>

Groups Cache

</td><td>

Displays details of the groups in Workplace from Facebook.When you click **Synchronise Cache**, the Fetch Workplace from Facebook Groups subflow is triggered and the groups details are retrieved.

</td></tr></tbody>
</table>For information about setting up the spoke, see [Set up Workplace from Facebook spoke](../task/set-up-fb-wp.md#).

