---
title: Okta Spoke
description: Use Okta to manage users, passwords, and groups.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 12
keywords: [AI Agents, Agentic AI]
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Okta Spoke

Use Okta to manage users, passwords, and groups.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Okta spoke v4.7.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   com.glide.cobject:sys,com.glide.script.vtable
-   com.snc.remote\_directory\_sync
-   XML Parser for ServiceNow IntegrationHub \(com.glide.hub.action\_step.xmlparser\)
-   Flow Designer Model \(com.glide.hub.designer\_backend.model\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

API version v1.

## Spoke flows

The Okta spoke provides sample flows in the draft state to demonstrate automating user and group management tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Add User to Okta Group|When a user is created, it adds the user to the specified group.|
|Onboard User in Okta|When a user is created in ServiceNow, creates and activates the user in Okta.|
|Remove Okta Group Membership on Deactivation|When a user is deactivated, it removes the user from all Okta groups.|

**Note:** Okta has the ServiceNow\_UD application to provision users in ServiceNow. ServiceNow can also be configured to provision users at Okta. Therefore, ServiceNow administrators must confirm that circular user creation doesn’t occur.

## Spoke subflows

The Okta spoke provides sample subflows to demonstrate automating Okta tasks. Available subflows are:

<table id="table_ed3_sxs_mpb"><thead><tr><th>

Subflow category

</th><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Webhook management

</td><td>

Check Activate Application Event Hook

</td><td>

Verifies if an event hook for the application-lifecycle-activate exists in Okta.

</td></tr><tr><td>

Inbound Integration from Okta to ServiceNow

</td><td>

Allows inbound integration from Okta to a ServiceNow instance. Verifies if an event hook exists for an application. If the event hook doesn’t exist, a new event hook is created. **Note:** Make sure that **Configuration URI** field value is in this format: `https://<instance-name>.service-now.com/api/sn_okta_spoke/oktawebhook`

</td></tr><tr><td>

Group Management

</td><td>

Get Groups

</td><td>

Updates an existing group or creates a group at Okta.

</td></tr><tr><td>

Application Management

</td><td>

Create or Update Okta Applications Record

</td><td>

Creates an Okta application record or updates an existing Okta application record.

</td></tr></tbody>
</table>## Available sample conversational subflows

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Conversational subflow|Description|
|----------------------|-----------|
|Expire User Password - Sample|Expires the user's password in Okta.|
|Reset to Temporary Password - Sample|Resets the user's password in Okta to a temporary password.|
|Look up Group Details - Sample|Retrieves details of the required group in Okta.|
|Look up User Profile - Sample|Retrieves details of the required user profile in Okta.|
|Add User to Group - Sample|Adds user to the required group.|
|Look up Group Members - Sample|Retrieves details of users in the required group in Okta.|
|Is User in Group - Sample|Specifies if the user is a member of the provided group.|
|Look up Users by Application - Sample|Retrieves details of users that have access to the specific application.|

## Spoke module

The Okta spoke adds the Okta application to your ServiceNow instance and includes these modules:

|Module|Description|
|------|-----------|
|Okta Applications|Shows the list of applications.|
|Okta groups|Shows the list of user groups at Okta.|
|Okta Users|Shows the list of users at Okta.|
|Okta Webhook Registry|Shows the list of webhook registries.|

## Spoke actions

The Okta spoke provides actions to authenticate and manage users and groups. Available actions include:

<table id="table_p2h_x34_3fb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="14">

User Management

</td><td>

Activate User

</td><td>

Starts the process of activating a user at Okta by enabling new or returning users to configure their Okta account from an activation URL. This action can either have Okta send the activation URL to the user as an email, or it can return the activation URL as a data pill for use in a later action to send an email or notification.

</td></tr><tr><td>

Clear User Session

</td><td>

Clears all active sessions you have with Okta, which forces the user to log back in the next time they use Okta.

</td></tr><tr><td>

Create User

</td><td>

Creates the specified user at Okta with the specified standard, optional, and mandatory field values.**Note:** Okta has the ServiceNow\_UD application to provision users in ServiceNow. ServiceNow can also be configured to provision users at Okta. Therefore, ServiceNow administrators must confirm that circular user creation doesn’t occur.

</td></tr><tr><td>

Deactivate User

</td><td>

Deactivates the specified user at Okta, which removes the user's groups and application assignments, and changes the user status to DEACTIVATED. This action is commonly used when a user departs the company indefinitely.

 **Note:** Don’t perform this action on users with a DEPROVISIONED status.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the specified user within Okta, which completely removes the user. This action is commonly used to clean up your user base after compliance regulations have been met.

</td></tr><tr><td>

Is User Account Locked

</td><td>

Determines if a user account is locked.

</td></tr><tr><td>

Lookup Okta User ID

</td><td>

Retrieves the Okta user ID for the specified Okta login ID or login short name.

</td></tr><tr><td>

Lookup User Account Details by User ID

</td><td>

Retrieves user details for the specified Okta user ID.

</td></tr><tr><td>

Lookup User Profile by User ID

</td><td>

Retrieves user profile details for the specified Okta user ID.

</td></tr><tr><td>

Restart User Activation

</td><td>

Restarts the specified user's activation within Okta. Use this action if the user didn’t complete their activation with the activation code or link provided by the **Activate User** Action.

</td></tr><tr><td>

Suspend User

</td><td>

Suspends the specified user within Okta by changing the user status from ACTIVE to SUSPENDED. For example, use this action to suspend access for users who are on temporary leave. To reactivate a suspended user, use the **Unsuspend** action.

</td></tr><tr><td>

Unsuspend User

</td><td>

Unsuspends the specified user at Okta.

</td></tr><tr><td>

Update User Profile

</td><td>

Updates the user profile details for the specified user at Okta.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves users from Okta based on the filter value.

</td></tr><tr><td rowspan="6">

Password Management

</td><td>

Change User's Password

</td><td>

Changes the specified user's password after validating the user's current password.

</td></tr><tr><td>

Expire User Password

</td><td>

Expires the specified user's password within Okta. This action is commonly used as a reaction to stop breaching attempts.

</td></tr><tr><td>

Reset to Temporary Password

</td><td>

Resets the specified user's password within Okta to a temporary password. This action is commonly used to get a user logged in who has forgotten their password.

</td></tr><tr><td>

Reset User Factors

</td><td>

Resets all of the multi-factor access devices for the specified user within Okta. This action is commonly used when a user loses their multi-factor authentication device or method.

</td></tr><tr><td>

Set User Password

</td><td>

Sets the specified user's password in Okta.

</td></tr><tr><td>

Unlock User

</td><td>

Unlocks the specified user in Okta.

</td></tr><tr><td rowspan="9">

Group Management

</td><td>

Add User To Group

</td><td>

Adds the specified user to the specified group in Okta.

</td></tr><tr><td>

Create Group

</td><td>

Creates the specified group in Okta.

</td></tr><tr><td>

Get Groups

</td><td>

Retrieves all new and updated groups in Okta.

</td></tr><tr><td>

Is User In Group

</td><td>

Determines if the specified user is a member of the specified group in Okta.

</td></tr><tr><td>

Lookup Group Details by Group ID

</td><td>

Retrieves group details for the specified Okta group ID.

</td></tr><tr><td>

Lookup Group ID By Name

</td><td>

Retrieves group details and group ID for the specified Okta group name.

</td></tr><tr><td>

Remove User From Group

</td><td>

Removes the specified user from the specified Okta group ID.

</td></tr><tr><td>

Update Group

</td><td>

Updates the group details for the specified Okta group ID.

</td></tr><tr><td>

Look up Groups Stream

</td><td>

Retrieves groups from Okta, based on the filter criteria.

</td></tr><tr><td rowspan="2">

Group Membership Management

</td><td>

Look up Group Members Stream

</td><td>

Retrieves users from the specified Okta group.

</td></tr><tr><td>

Look up User Groups Stream

</td><td>

Retrieves the group information from Okta to which the user belongs to.

</td></tr><tr><td rowspan="3">

Application Access Management

</td><td>

Look up Users by Application ID Stream

</td><td>

Retrieves users who have access to the specified application.

</td></tr><tr><td>

Look up Groups by Application ID Stream

</td><td>

Retrieves groups who have access to the specified application.

</td></tr><tr><td>

Revoke User Application Access

</td><td>

Revokes access to an application for the required user.

</td></tr><tr><td rowspan="3">

Application Management

</td><td>

Look up Applications Stream

</td><td>

Retrieves applications from Okta, based on the filter criteria. For more information about the criteria you can specify in the **Filter** input, see [List applications](https://developer.okta.com/docs/reference/api/apps/#list-applications) in [Okta Developer Documentation](https://developer.okta.com/docs/).

</td></tr><tr><td>

Look up Application by Application ID

</td><td>

Retrieves details of the specified application ID in Okta.

</td></tr><tr><td>

Look up App Launcher Applications Stream

</td><td>

Retrieves applications that are either active or are assigned to users.

</td></tr><tr><td>

Logs Management

</td><td>

Look up Okta Logs Stream

</td><td>

Retrieves the logs in Okta that are filtered by the given filter value and within the specified time duration. For more information about the event types and system logs, see [Event Types](https://developer.okta.com/docs/reference/api/system-log/#event-types) in [Okta Developer Documentation](https://developer.okta.com/docs/).

</td></tr><tr><td rowspan="4">

Metadata Retrieval

</td><td>

Look up Additional Fields for User

</td><td>

Retrieves the metadata of the additional fields for a user in Okta.

</td></tr><tr><td>

Look up Applications Metadata

</td><td>

Retrieves the metadata of applications in Okta.

</td></tr><tr><td>

Look up Event Hooks Metadata

</td><td>

Retrieves the metadata of the event hooks in Okta.**Note:** Make sure that you use this action along with the actions that use Event Hook ID as a dynamic input.

</td></tr><tr><td>

Look up Groups Metadata

</td><td>

Retrieves the metadata details of the groups in Okta.

</td></tr><tr><td rowspan="7">

Webhook Management

</td><td>

Activate Event Hook

</td><td>

Changes the status of the specified event hook to active in Okta.

</td></tr><tr><td>

Create Event Hook

</td><td>

Creates an active event hook in Okta. **Note:** Make sure that **Configuration URI** field value is in this format: `https://<instance-name>.service-now.com/api/sn_okta_spoke/oktawebhook`

</td></tr><tr><td>

Deactivate Event Hook

</td><td>

Sets the status of the specified Okta event hook to inactive.

</td></tr><tr><td>

Look up Event Hook by ID

</td><td>

Retrieves details of the Okta event hook for the specified ID.

</td></tr><tr><td>

Look up Event Hooks

</td><td>

Retrieves details of all the event hooks in Okta.

</td></tr><tr><td>

Update Event Hook

</td><td>

Updates the specified event hook in Okta. **Note:** Make sure that **Configuration URI** field value is in this format: `https://<instance-name>.service-now.com/api/sn_okta_spoke/oktawebhook`

</td></tr><tr><td>

Verify Event Hook

</td><td>

Verifies and retrieves an external service endpoint configured for an event hook in Okta.

</td></tr></tbody>
</table>## Available conversational actions

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

Available conversation action is Create Group that creates a group in Okta with the provided details.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Okta group management AI agent|Automates group-related tasks in Okta using Integration Hub such as those related to managing of groups, handling user memberships, and retrieving group details.|
|Okta password management AI agent|Automates password-related workflows in Okta from Integration Hub. Automate actions such as reset password to temporary values, set new password, expire passwords, unlock user accounts, reset user authentication factors, and change user passwords.|
|Okta group membership management AI agent|Automates group-related workflows in Okta from Integration Hub. Automate actions such as Look up User Groups Stream’, and 'Look up Group Members Stream'.|
|Okta user management AI agent|Automates user management workflows in Okta from Integration Hub. Automate actions such as manage user accounts, sessions, and statuses.|
|Okta application access management AI agent|Automates access management workflows in Okta from Integration Hub. Automate actions such as look up users and groups by application ID stream, and revoking user application access.|
|Okta application management AI agent|Automates application management-related workflows in Okta from Integration Hub. Automate actions such as look up applications, retrieve application details by ID, and create or update Okta application records.|
|Okta logs management AI agent|Automates log management-related workflows in Okta from Integration Hub. Automate actions such as 'Look up Okta Logs Stream’.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Okta account requirements

The Okta spoke requires generating and configuring your Okta account to use a web API key.

## Credential and connection alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

This spoke uses the Okta Connection &amp; Credential Alias record to authorize actions. For information about setting up the spoke, see [Set up Okta spoke](../task/set-up-okta-v1.1.1.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Okta alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

