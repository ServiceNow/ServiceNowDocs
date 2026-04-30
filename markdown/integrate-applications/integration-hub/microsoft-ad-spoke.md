---
title: Microsoft Active Directory Spoke
description: Create, delete, and manage objects in Microsoft Active Directory, such as users, groups, and computers.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Active Directory Spoke

Create, delete, and manage objects in Microsoft Active Directory, such as users, groups, and computers.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

**Important:**

-   Starting with the Vancouver release, Microsoft Active Directory Spoke is being prepared for future deprecation. It is hidden and no longer activated on new instances but will continue to be supported. Microsoft Active Directory v2 Spoke provides the latest experience for this functionality. For details, see the Deprecation Process \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] article in the Now Support Knowledge Base.
-   This spoke is available as part of the family release. This spoke can be used to handle the computer objects.

## Spoke requirements

Confirm that the Active Directory web services \(ADWS\) is deployed on the server that has Microsoft AD installed. For information on deploying ADWS, see [https://learn.microsoft.com/en-us/services-hub/unified/health/remediation-steps-ad/configure-the-active-directory-web-services-adws-to-start-automatically-on-all-servers](https://learn.microsoft.com/en-us/services-hub/unified/health/remediation-steps-ad/configure-the-active-directory-web-services-adws-to-start-automatically-on-all-servers) for information about deploying ADWS.

Since your instance must have a MID Server set up and configured to use the PowerShell, the MID Server must be able to access the ADWS at port 9389.

In the MID Server and Microsoft AD server, run these PowerShell commands to install the Active Directory module:

```
PS> Import-Module ServerManager
PS> Install-WindowsFeature -Name RSAT-AD-PowerShell
```

## Spoke flows

The Microsoft Active Directory spoke provides sample flows in the draft state to demonstrate automating Active Directory tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|User Offboarding|Disables an AD user account and removes the user from any AD groups when a ServiceNow user record is deactivated.|
|User Onboarding|Creates and enables an AD user account when a ServiceNow user record is activated.|

## Spoke subflows

This spoke has no sample subflows.

## Spoke actions

The Microsoft AD spoke provides actions to automate Microsoft Active Directory tasks when events occur in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Computer Management|Create Computer|Creates a Computer Account in Active Directory.|
|Delete Computer|Deletes a computer from Active Directory.|
|Disable Computer|Disables a computer account in Active Directory.|
|Enable Computer|Enables a computer account in Active Directory.|
|Get Computer OU|Gets the Organizational Unit \(OU\) of a Computer Account.|
|Is Computer Enabled|Checks the status of the specified computer account in Active Directory.|
|Move Computer to OU|Changes the Organizational Unit \(OU\) of a Computer Account in Active Directory.|
|Group Management|Add User To Group|Adds an existing Active Directory user to an Active Directory group.|
|Create Group|Creates a group in Active Directory.|
|Delete Group|Deletes a group from Active Directory.|
|Lookup Group|Gets the details of a given group in Active Directory, including the group category, scope, and distinguished name.|
|Remove User From Group|Removes an existing user from a group in Active Directory.|
|Password Management|Change User Password|Changes the user password in AD. The password input must comply with Active Directory password requirements.|
|Is User Account Locked|Checks the locked status of the specified user account in Active Directory.|
|Reset AD User Password|Resets a user's password in Active Directory.|
|User Management|Create User|Creates a user with no password in Active Directory. To enable a user to set a password, log in to AD, create a default password for the user, and enable password reset.|
|Delete User|Deletes a user from Active Directory.|
|Disable User|Disables a user account in Active Directory.|
|Enable User|Enables a user account in Active Directory.|
|Is User Enabled|Checks the status of a user account in Active Directory.|
|Is User In Group|Checks if an existing Active Directory user is a member of an Active Directory group.|
|Lookup User|Gets the details of a given user in Active Directory.|
|Unlock AD Account|Unlocks a user account in Active Directory.|
|Update User|Updates user attributes in Active Directory.|
|Update User Home Location|Updates the Home Directory for a User in Active Directory.|
|Object Management|Create AD Object|Creates an object of any type supported in Active Directory.|
|Delete AD Object|Deletes an object of any type from Active Directory.|
|Query AD|Queries AD for objects specified by a search filter.|
|Update AD Object OU|Changes the Organizational Unit \(OU\) of an object in Active Directory.|
|Update AD Object Expiration|Update the account expiration date of an object in Active Directory.|

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use the PowerShell. For more information about running actions on the MID Server, see [Integration steps](integration-steps.md). For information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** MID and Microsoft Active Directory must be installed on different servers.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the AD alias record to authorize actions in Microsoft Active Directory.

|Connection alias|Description|Connection URL|
|----------------|-----------|--------------|
|AD|Connection to Microsoft Active Directory.|The URL of the host machine where Microsoft Active Directory is installed.|

For information about setting up the spoke, see [Set up Microsoft Active Directory spoke](../../integrationhub-store-spokes/task/set-up-ad.md#).

