---
title: Microsoft Active Directory v2 Spoke
description: Create, delete, and manage objects in Microsoft Active Directory, such as users, groups, and computers.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Active Directory v2 Spoke

Create, delete, and manage objects in Microsoft Active Directory, such as users, groups, and computers.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Active Directory v2 spoke v2.5.3 is the latest version.

## Supported versions

This spoke was built for Microsoft Active Directory.

## Spoke requirements

Ensure that Active Directory Web Services \(ADWS\) is deployed in the same server where Microsoft Active Directory is installed. The MID server can access the Active Directory Web Services \(ADWS\) at port 9389. For more information about ADWS deployment, see Microsoft documentation.

In the MID Server and Microsoft Active Directory v2 server, run the following PowerShell commands to install the Active Directory module:

```
PS> Import-Module ServerManager
PS> Install-WindowsFeature -Name RSAT-AD-PowerShell
```

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   ServiceNow IntegrationHub Action Step - PowerShell \(com.glide.hub.action\_step.powershell\)

**Note:** If used outside the spoke implementation, some of these plugins are licensable features and require licenses.

## Spoke actions

The Microsoft Active Directory v2 spoke provides actions to automate the tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_exp_mnx_54b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="13">

Group Management

</td><td>

Add Computer to Groups

</td><td>

Adds the computer account to one or more groups in the Active Directory \(AD\).

</td></tr><tr><td>

Add Computers to Group

</td><td>

Adds one or more computer accounts to the group in the Active Directory \(AD\).

</td></tr><tr><td>

Add User to Groups

</td><td>

Adds a user to one or more groups in the Active Directory \(AD\).

</td></tr><tr><td>

Add Users to Group

</td><td>

Adds one or more user accounts to the group in the Active Directory \(AD\).

</td></tr><tr><td>

Create Group

</td><td>

Creates the group in the Active Directory \(AD\).

</td></tr><tr><td>

Delete Group

</td><td>

Deletes the group from the Active Directory \(AD\).

</td></tr><tr><td>

Does Group Exists

</td><td>

Checks whether the group exists in the Active Directory \(AD\).

</td></tr><tr><td>

Is User in Group

</td><td>

Checks if an existing user is already a member of a group in the Active Directory \(AD\).

</td></tr><tr><td>

Look up Group

</td><td>

Retrieves the group from the Active Directory \(AD\).

</td></tr><tr><td>

Remove Computer from Groups

</td><td>

Removes the computer account from one or more groups in the Active Directory \(AD\).

</td></tr><tr><td>

Remove Computers from Group

</td><td>

Removes one or more computers from the group in the Active Directory \(AD\).

</td></tr><tr><td>

Remove User from Groups

</td><td>

Removes a user from one or more groups in the Active Directory \(AD\).

</td></tr><tr><td>

Remove Users from Group

</td><td>

Removes one or more users from the group in the Active Directory \(AD\).

</td></tr><tr><td rowspan="6">

User Authentication

</td><td>

Change User Password

</td><td>

Changes the user's password in the Active Directory \(AD\). The password has to match the AD password requirements.

</td></tr><tr><td>

Look up User Password Expiration Details

</td><td>

Retrieves the password expiration details for the user from the Active Directory \(AD\).

</td></tr><tr><td>

Generate Random Password

</td><td>

Generates the random password according to the Active Directory \(AD\) password policy.

</td></tr><tr><td>

Is User Locked

</td><td>

Checks the locked status of the user account in the Active Directory \(AD\).

</td></tr><tr><td>

Reset User Password

</td><td>

Resets the password of the user in the Active Directory \(AD\).

</td></tr><tr><td>

Unlock User

</td><td>

Unlocks the user account in the Active Directory \(AD\).

</td></tr><tr><td rowspan="8">

Computer Management

</td><td>

Create Computer

</td><td>

Creates a computer account in the Active Directory \(AD\).

</td></tr><tr><td>

Disable Computer

</td><td>

Disables the computer account in the Active Directory \(AD\).

</td></tr><tr><td>

Does Computer Exists

</td><td>

Checks the status of the computer account in the Active Directory.

</td></tr><tr><td>

Is Computer Disabled

</td><td>

Checks the status of the computer account in the Active Directory \(AD\).

</td></tr><tr><td>

Enable Computer

</td><td>

Enables the computer account in the Active Directory \(AD\).

</td></tr><tr><td>

Look up Computer

</td><td>

Retrieves a computer account from the Active Directory \(AD\).

</td></tr><tr><td>

Update Computer

</td><td>

Updates a computer account in the Active Directory \(AD\).

</td></tr><tr><td>

Delete Computer

</td><td>

Deletes a computer account from the Active Directory \(AD\).

</td></tr><tr><td rowspan="5">

Object Management

</td><td>

Create Object

</td><td>

Creates an object account in the Active Directory \(AD\).

</td></tr><tr><td>

Update Object OU

</td><td>

Updates the Organizational Unit \(OU\) of an object account in the Active Directory \(AD\).

</td></tr><tr><td>

Update Object Expiration

</td><td>

Updates the account expiration date of the object account in the Active Directory \(AD\).

</td></tr><tr><td>

Look up Object by Filter

</td><td>

Retrieves object accounts based on a search filter in the Active Directory \(AD\).

</td></tr><tr><td>

Delete Object

</td><td>

Deletes an object account from the Active Directory \(AD\).

</td></tr><tr><td rowspan="9">

User Management

</td><td>

Delete User

</td><td>

Deletes the user from Active Directory \(AD\).

</td></tr><tr><td>

Create User

</td><td>

Creates a user account in the Active Directory \(AD\) and sets a password.**Note:** From Microsoft Active Directory v2 spoke v2.1.1 onwards, these changes are applicable:

-   **Sam Account Name** is available in the **Additional Fields** drop-down.
-   When a user is created, the User Principal Name \(UPN\) is generated in this format: `<username>@<DNS-domain-name>`.

</td></tr><tr><td>

Disable User \(Conversational -ready\)

</td><td>

Disables a user account in Active Directory \(AD\).

</td></tr><tr><td>

Does User Exists

</td><td>

Checks whether the user account exists in Active Directory \(AD\).

</td></tr><tr><td>

Update User

</td><td>

Updates a user account in the Active Directory \(AD\).

</td></tr><tr><td>

Enable User \(Conversational -ready\)

</td><td>

Enables a user account in Active Directory \(AD\).

</td></tr><tr><td>

Look up User \(Conversational -ready\)

</td><td>

Retrieves a user account from the Active Directory \(AD\).**Note:** Now Assist for Conversational Spokes plugin is required to use the conversational ability of the action.

</td></tr><tr><td>

Is User Disabled

</td><td>

Checks if the user account is inactive in Active Directory \(AD\).

</td></tr><tr><td>

Get User Additional Fields \(Metadata\)

</td><td>

Retrieves information from the additional fields in a user account from the Active Directory \(AD\).

</td></tr></tbody>
</table>**Note:** This spoke isn't tested with a load balancer.

## Available conversational actions

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Action|Usage|
|------|-----|
|Disable User|In the Ask Now Assist to... field, enter the phrase that asks Now Assist to perform the action and press **Enter**. `Disable user "Jack" in Active Directory.`|
|Enable User|In the Ask Now Assist to... field, enter the phrase that asks Now Assist to perform the action and press **Enter**. For example, `Enable user "Jack" in Active Directory.`|
|Look up User|In the Ask Now Assist to... field, enter the phrase that asks Now Assist to perform the action and press **Enter**. For example, `Look up user "Jack" in Active Directory.`|

![Lookup User action conversational ability in Now Assist panel](../image/ad-v2-na-lookup-user-action.jpg)

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Microsoft Active Directory object manager|Manages object accounts in the Active Directory \(AD\) and retrieves their details.|
|Microsoft Active Directory user authenticator|Manages user accounts and passwords in the Active Directory \(AD\) and retrieves their details.|
|Microsoft Active Directory group manager|Manages groups in the Active Directory \(AD\) and retrieves their details.|
|Microsoft Active Directory computer manager|Manages computers in the Active Directory \(AD\) and retrieves their details.|
|Microsoft Active Directory user manager|Manages users in the Active Directory \(AD\) and retrieves their details.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the Microsoft Active Directory v2 spoke](../task/setup-ms-ad-v2.md#).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For more information about the MID Server, see MID Server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

**Note:** You must install the MID Server and Microsoft Active Directory on different servers.

