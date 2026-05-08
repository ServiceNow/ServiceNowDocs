---
title: Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\)
description: Manage users, applications, groups, devices, tenants, service principals, and passwords. Apply licenses and provision users in Office 365.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Entra ID Spoke \(formerly Microsoft Azure Active Directory spoke\)

Manage users, applications, groups, devices, tenants, service principals, and passwords. Apply licenses and provision users in Office 365.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Entra ID spoke \(formerly known as Microsoft Azure Active Directory spoke\) v4.7.4 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   ServiceNow IntegrationHub Action Step - PowerShell \(com.glide.hub.action\_step.powershell\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Remote Directory Sync

## Spoke flows

The Microsoft Entra ID spoke provides sample flows in the draft state to demonstrate automating Microsoft Entra tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|User Offboarding|Disables an Entra ID user account and removes the user from the Entra ID groups when a ServiceNow user record is deactivated.|
|User Onboarding|Creates and enables an Entra ID user account when a ServiceNow user record is activated.|

## Spoke subflows

The Microsoft Entra ID spoke provides sample subflows in the draft state to demonstrate automating Entra tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Add User to Group|Looks up the groups that a ServiceNow User record belongs to, and adds the associated Entra ID user account to the same Entra ID groups.|

## Available sample conversational subflows

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](conv-spokes-na.md).

|Conversational subflow|Description|
|----------------------|-----------|
|Look up Groups - Sample|Retrieves information about the specified groups in the Entra ID.|
|Look up Group Members - Sample|Retrieves information about the specified group members in the Entra ID.|
|Look up Users - Sample|Retrieves information about users in the Entra ID.|
|Look up Direct Reports - Sample|Retrieves information about the direct reports in the Entra ID.|
|Add User to Group using Email Address - Sample|Adds the specified Entra ID user to the specified Entra ID group using the user's email address.|
|Add User to a group - Sample|Adds the specified Entra ID user to the specified Entra ID group.|

## Spoke actions

The Microsoft Entra ID spoke provides actions to automate Entra tasks when events occur in ServiceNow. Available actions include:

**Note:**

-   One of the mentioned permissions is required to call the API.
-   Ensure that you are aware of these considerations:
    -   Select the Delegated permission if you intend to use the **Authorization Code** grant type while registering Entra ID as an OAuth provider.
    -   Select the Application permission if you intend to use the **Client Credentials** grant type while registering Entra ID as an OAuth provider.

<table id="table_khs_njf_kfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th colspan="2">

Permissions Required \(from least to most privileged\)

</th></tr></thead><tbody><tr><td rowspan="3">

Audit Logs

</td><td rowspan="3">

Look up Sign Ins Stream

</td><td rowspan="3">

Retrieve the list of sign ins.

</td><td>

Delegated \(work or school account\)

</td><td>

AuditLog.Read.All, Directory.Read.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported

</td></tr><tr><td>

Application

</td><td>

AuditLog.Read.All , Directory.Read.All

</td></tr><tr><td rowspan="51">

Group Management

</td><td rowspan="3">

Add Owner to Group

</td><td rowspan="3">

Add an owner to an existing group in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Add User to Group

</td><td rowspan="3">

Add an existing user to a group in Microsoft Entra ID.**Note:** Adding a user to a mail-enabled security group is not supported by the Microsoft Graph Security API. For more information, see [https://learn.microsoft.com/en-us/graph/api/resources/groups-overview?view=graph-rest-1.0&amp;tabs=http](https://learn.microsoft.com/en-us/graph/api/resources/groups-overview?view=graph-rest-1.0&tabs=http).

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All and Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Create Office 365 Group

</td><td rowspan="3">

Creates an Office 365 group that can be shared with the other members in the group.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.Create, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Group Membership Stream by Directory

</td><td rowspan="3">

Retrieve the list of group membership.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Directory.Read.All, Group.Read.All, Group.ReadWrite.All, GroupMember.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.Read.All, Directory.Read.All, Group.Read.All, Group.ReadWrite.All, GroupMember.ReadWrite.All

</td></tr><tr><td rowspan="3">

Create Security Group

</td><td rowspan="3">

Creates a security group when you want to grant access permissions to a group of users.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.Create, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Group

</td><td rowspan="3">

Returns the Group information found based on the search criteria.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Group Members Stream

</td><td rowspan="3">

Retrieves the list of members of the specified group.

</td><td>

Application

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="3">

Look up Group Membership Stream

</td><td rowspan="3">

Retrieves the list of groups for the specified user as a complex object.

</td><td>

Delegated \(work or school account\)

</td><td>

User.Read, GroupMember.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Group Transitive Membership Stream

</td><td rowspan="3">

Retrieves list of groups for the specified user as a complex object.

</td><td>

Delegated \(work or school account\)

</td><td>

Not supported.

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Groups.Read.All, User.Read.All, Sites.FullControl.All, Sites.Selected

</td></tr><tr><td rowspan="3">

Delete Group

</td><td rowspan="3">

Deletes the specified group from Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All

</td></tr><tr><td rowspan="3">

Add Owners to Group

</td><td rowspan="3">

Adds the specified users as owners to the specified group in the Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Remove Owner from Group

</td><td rowspan="3">

Removes the owner from a group in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Remove User from Group

</td><td rowspan="3">

Removes an existing user from a group in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Groups Stream by Directory

</td><td rowspan="3">

Retrieves the list of groups in the directory integration.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Groups Stream

</td><td rowspan="3">

Lists all the groups in an organization.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.Read.All, Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Add Users to Group

</td><td rowspan="3">

Add existing users to a group in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All and Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Update Office 365 Group

</td><td rowspan="3">

Updates the specified office 365 group.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="12">

License Management

</td><td rowspan="3">

Look up Subscribed SKU

</td><td rowspan="3">

Retrieves the details of the specified subscribed SKU.

</td><td>

Delegated \(work or school account\)

</td><td>

Organization.Read.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Organization.Read.All, Directory.Read.All, Directory.ReadWrite.All, Organization.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Subscribed SKUs

</td><td rowspan="3">

Retrieves the list of commercial subscriptions that an organization has acquired.

</td><td>

Delegated \(work or school account\)

</td><td>

Organization.Read.All, Directory.Read.All, Directory.ReadWrite.All, Organization.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Organization.Read.All, Directory.Read.All, Directory.ReadWrite.All, Organization.ReadWrite.All

</td></tr><tr><td rowspan="3">

Assign User License

</td><td rowspan="3">

Onboards an existing user in the Microsoft Entra ID to Office 365 and grant access to services.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Remove User License

</td><td rowspan="3">

Removes a license from a user in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="18">

Application Management

</td><td rowspan="3">

Look up App Roles Assignments Stream

</td><td rowspan="3">

Retrieves the list of the app roles that have been assigned to a user.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadBasic.All, Directory.Read.All, AppRoleAssignment.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported

</td></tr><tr><td>

Application

</td><td>

Directory.Read.All, AppRoleAssignment.ReadWrite.All

</td></tr><tr><td rowspan="3">

Create Application Assignment

</td><td rowspan="3">

Creates an assignment for a specified application in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td rowspan="3">

Delete Application Assignment

</td><td rowspan="3">

Deletes the specified application assignment in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Application Assignments Stream

</td><td rowspan="3">

Lists all application assignments for the specified application in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

DeviceManagementConfiguration.Read.All, DeviceManagementConfiguration.ReadWrite.All, DeviceManagementApps.Read.All, DeviceManagementApps.ReadWrite.All

</td></tr><tr><td rowspan="3">

Revoke User Application Access

</td><td rowspan="3">

Removes an app role assignment that has been granted to a user.

</td><td>

Delegated \(work or school account\)

</td><td>

AppRoleAssignment.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

AppRoleAssignment.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Applications Stream

</td><td rowspan="3">

Retrieves the list of applications.

</td><td>

Delegated \(work or school account\)

</td><td>

Application.Read.All, Application.ReadWrite.All, Directory.Read.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Application.Read.All and User.Read, Application.ReadWrite.All and User.Read

</td></tr><tr><td>

Application

</td><td>

Application.Read.All, Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="15">

Device Management

</td><td rowspan="3">

Add Device to Group

</td><td rowspan="3">

Adds an existing device to a group in the Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported

</td></tr><tr><td>

Application

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All and Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Is Device in Group

</td><td rowspan="3">

Checks if an existing device is a member of a group in Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Device.Read.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Device.Read.All, Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Add Devices to Group

</td><td rowspan="3">

Adds the specified devices to the specified group in Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Devices Stream

</td><td rowspan="3">

Lists all the devices in an organization or devices that satisfy the specified filter query, if any.

</td><td>

Delegated \(work or school account\)

</td><td>

Device.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Device.Read.All, Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Remove Device from Group

</td><td rowspan="3">

Remove an existing device from a group in the Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Organization Management

</td><td rowspan="3">

Look up Tenant

</td><td rowspan="3">

Retrieves details of the currently authenticated tenant.

</td><td>

Delegated \(work or school account\)

</td><td>

DeviceManagementServiceConfig.Read.All, DeviceManagementServiceConfig.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

DeviceManagementServiceConfig.Read.All, DeviceManagementServiceConfig.ReadWrite.All

</td></tr><tr><td>

User Authentication

</td><td>

Revoke User SignIn Sessions

</td><td>

Revokes the user signin sessions so that administrators can automate invalidating all the sign in session of a specified user.

</td><td>

 

</td><td>

 

</td></tr><tr><td rowspan="6">

Service Principal Management

</td><td rowspan="3">

Look up App Role Assigned to Service Principal Stream

</td><td rowspan="3">

Retrieves the list of service principal assignments.

</td><td>

Delegated \(work or school account\)

</td><td>

Application.Read.All, Directory.Read.All, Application.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Application.Read.All, Directory.Read.All, Application.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Service Principals Stream

</td><td rowspan="3">

Retrieves the list of service principals.

</td><td>

Delegated \(work or school account\)

</td><td>

Application.Read.All, Application.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Application.Read.All, Application.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="12">

Password Management

</td><td rowspan="3">

Reset Password

</td><td rowspan="3">

Resets the password of the Entra ID user account.**Note:** This spoke action resets the password of users created in Entra ID only and does not reset the password of the federated users.

</td><td>

Delegated \(work or school account\)

</td><td>

Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Not supported.

</td></tr><tr><td rowspan="3">

Look up Password Expiration

</td><td rowspan="3">

Retrieves Password expiration details for the provided user from Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Change Password

</td><td rowspan="3">

Changes the password of a user in Microsoft Entra ID. Ensure that the password meets the Entra ID password requirements.

</td><td>

Delegated \(work or school account\)

</td><td>

Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Not supported.

</td></tr><tr><td rowspan="3">

Generate Random Password

</td><td rowspan="3">

Generates the random password as per the default Entra ID password policy.**Note:** You must install the KMF plugin before executing this action.

</td><td>

Delegated \(work or school account\)

</td><td rowspan="3">

None.

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td></tr><tr><td>

Application

</td></tr><tr><td rowspan="42">

User Management

</td><td rowspan="3">

Look up User

</td><td rowspan="3">

Retrieves a user account from Entra.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Users Stream by Directory

</td><td rowspan="3">

Retrieves the list of users from a directory.

</td><td>

Application

</td><td>

User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="3">

Revoke User SignIn Sessions

</td><td rowspan="3">

Invalidates all signed in sessions of a user.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

Not supported.

</td></tr><tr><td rowspan="3">

Create User

</td><td rowspan="3">

Creates a user with the given details.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Delete User

</td><td rowspan="3">

Deletes a user from Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All

</td></tr><tr><td rowspan="3">

Disable User

</td><td rowspan="3">

Disables a user in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite, User.ReadWrite.All, User.ManageIdentities.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

User.ReadWrite

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Enable User

</td><td rowspan="3">

Enables a user account in the Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite, User.ReadWrite.All, User.ManageIdentities.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

User.ReadWrite

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All, User.ManageIdentities.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Fetch Latest Delta Token for Users

</td><td rowspan="3">

Returns the latest delta token for the users.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Is User Enabled

</td><td rowspan="3">

Checks whether the specified user account is enabled in Microsoft Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

User.Read, User.ReadWrite

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Is User in Group

</td><td rowspan="3">

Checks whether the specified user account is a member of the specified group in Entra.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadBasic.All, User.Read.All, Directory.Read.All, User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.ReadBasic.All, User.Read.All, Directory.Read.All, User.ReadWrite.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Look up Users Stream

</td><td rowspan="3">

Lists all the users in an organization or users satisfying the specified search query, filter and next token if any.

</td><td>

Application

</td><td>

User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="3">

Update User

</td><td rowspan="3">

Updates user properties in Entra ID with the provided details.**Note:** Entra ID does not allow updating values to null. Null or empty values are discarded in Entra ID when null is passed as an input.

</td><td>

Delegated \(work or school account\)

</td><td>

User.ReadWrite, User.ReadWrite.All, User.ManageIdentities.All, Directory.ReadWrite.All, Directory.AccessAsUser.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

User.ReadWrite

</td></tr><tr><td>

Application

</td><td>

User.ReadWrite.All, User.ManageIdentities.All, Directory.ReadWrite.All

</td></tr><tr><td rowspan="3">

Does User owns Group

</td><td rowspan="3">

Checks if an existing user is a owner of a group in Entra ID.

</td><td>

Delegated \(work or school account\)

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

GroupMember.Read.All, Group.Read.All, GroupMember.ReadWrite.All, Group.ReadWrite.All, Directory.Read.All

</td></tr><tr><td rowspan="3">

Look up Incremental Changes for Users Stream

</td><td rowspan="3">

Retrieves the list of users in Entra ID. By using Delta Token, enables you discover changes to users without having to fetch the entire set of users.

</td><td>

Delegated \(work or school account\)

</td><td>

User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr><tr><td>

Delegated \(personal Microsoft account\)

</td><td>

Not supported.

</td></tr><tr><td>

Application

</td><td>

User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Microsoft Entra ID user management AI agent|Automates user and group management tasks in Microsoft Entra ID. The AI agent creates, enables and disables users, manages security and office groups, and performs advanced queries such as, retrieving incremental changes or direct reports.|
|Microsoft Entra ID group management AI agent|Automates user and group management tasks in Microsoft Entra ID. The AI agent retrieves group details, manages group memberships, creates security groups, and automates user provisioning into Office 365.|
|Microsoft Entra ID license management AI agent|Automates the management of users, security groups, and office groups in Microsoft Entra ID. The AI agent retrieves details about the subscribed SKUs, assigns user licenses, and remove user licenses.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Microsoft Entra ID account requirements

The Microsoft Entra ID spoke requires creating a custom app on your Microsoft Entra account to generate OAuth 2.0 tokens. See: [Create an Microsoft Entra ID application](../../integrationhub-store-spokes/task/set-up-azure.md#).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the AzureAD alias record to authorize actions on Microsoft Entra ID.

|Connection alias|Description|Connection URL|
|----------------|-----------|--------------|
|AzureAD|Connection to Microsoft Entra ID.|https://graph.microsoft.com|

For information about setting up the spoke, see [Set up Microsoft Entra ID spoke](../../integrationhub-store-spokes/task/set-up-azure.md#).

