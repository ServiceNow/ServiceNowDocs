---
title: List of Orchestration activities
description: Use Orchestration activities in a Workflow to integrate with third-party systems.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Activate Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# List of Orchestration activities

Use Orchestration activities in a Workflow to integrate with third-party systems.

Several Orchestration activities have been rewritten as Application scope activities using the [activity designer](../../orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md) and grouped into [activity packs](../concept/c_OrchestrationActivityPacks.md). Other non-scoped activities are deprecated and may or may not appear in the Workflow Editor. However, all deprecated activities still function in existing workflows that use them.

## Global activities

These activities run in the global scope only. Any activities you create in the global scope are organized in the Global category in the **Packs** and **Custom** tabs in the Workflow Editor.

|Activity|Description|
|--------|-----------|
|[Test Server Alive](../concept/global-activity-pack.md#)|Runs a command \(including shell scripts\) on a Linux or UNIX computer via SSH to validate whether the target system is alive.|

## Active Directory \(AD\) activities

All AD Orchestration activities were rewritten in the Geneva release as scoped activities and are available in the Active Directory activity pack. All previous version AD activities that were built on activity definitions are deprecated and are unavailable for use in new workflows.

|Activity|Description|
|--------|-----------|
|[Create AD Object](r_CreateADObject.md)|Creates a user account in Windows Active Directory when a user account is created in a ServiceNow instance.|
|[Disable AD User Account](r_DisableADUserAccount.md)|Marks a Windows Active Directory user account disabled, making it inactive.|
|[Enable AD User Account](r_EnableADUserAccount.md)|Enables a Windows Active Directory user account, making it active.|
|[Query AD](r_QueryAD.md)|Retrieves entries from the Windows Active Directory based on a search filter.|
|[Remove AD Object](r_RemoveADObject.md)|Deletes a user account from Windows Active Directory.|
|[Reset AD User Password](r_ResetADUserPassword.md)|Resets the password of a user account in Windows Active Directory.|
|[Change AD User Password](r_ChangeADUserPassword.md)|Changes the password of a user account in Windows Active Directory.|
|[Update AD Object](r_UpdateADObject.md)|Updates a user account in Windows Active Directory.|
|[Is AD Account Locked](r_IsADAccountLocked.md)|Determines if an Active Directory user account is locked.|
|[Unlock AD Account](r_UnlockADAccount.md)|Unlocks a locked Active Directory user account.|

## Azure AD

All these activities are scoped and part of the Azure AD activity pack. They do not have legacy versions.

|Activity|Description|
|--------|-----------|
|[Add User to Group](r_AddUserToGroupAzureADActivity.md)|Adds a user to an existing security group in Azure Active Directory.|
|[Assign User License](r_AssignUserLicenseAzureADActivity.md)|Assigns an extra Office 365 software license to the named user.|
|[Create User](r_CreateUserAzureADActivity.md)|Creates a user for the Azure Active Directory tenant.|
|[Delete User](r_DeleteUserAzureADActivity.md)|Deletes the named user's account from the Azure Active Directory tenant.|
|[Get User Info](r_GetUserInfoAzureADActivity.md)|Returns the named user's information from the Azure Active Directory.|
|[Remove User from Group](r_RemoveUserFromGroupADActivity.md)|Removes an existing user from a security group in Azure Active Directory.|
|[Remove User License](r_RemoveUserLicenseAzureADActivity.md)|Revokes the specified Office 365 software license for the named user.|
|[Reset User Password](r_ResetUserPasswordAzureADActivity.md)|Changes the named user's Azure Active Directory password.|

## F5 Network Management activities

All these activities are scoped and part of the F5 Network Management activity pack. They do not have legacy versions.

|Activity|Description|
|--------|-----------|
|[Add F5 Pool](r_AddF5PoolActivity.md)|Creates the load balancer pool.|
|[Check F5 Pool](r_CheckF5PoolActivity.md)|Checks the status of a pool to validate whether it is available to accept traffic.|
|[Delete F5 Pool](r_DeleteF5PoolActivity.md)|Deletes an F5 pool.|
|[Add F5 Pool Member](r_AddF5PoolMemberActivity.md)|Adds a member to an F5 pool.|
|[Get F5 Pool Member](r_GetF5PoolMemberActivity.md)|Returns the pool members and verifies the pool status.|
|[Delete F5 Pool Member](r_DeleteF5PoolMemberActivity.md)|Deletes an F5 pool member.|
|[Add F5 Virtual Server](r_AddF5VirtualServerActivity.md)|Adds a virtual server.|
|[Modify F5 Virtual Server](r_ModifyF5VirtualServerActivity.md)|Configures a virtual server assigned to an F5 pool with irules and a vlan.|
|[Delete F5 Virtual Server](r_DeleteF5VirtualServerActivity.md)|Deletes a virtual server from an F5 pool.|
|[Add F5 Profile to Virtual Server](r_AddF5ProfileToVirtualServerActivity.md)|Adds a profile to a virtual server assigned to an F5 pool.|

## Infoblox activities

All these activities are scoped and part of the Infoblox DDI activity pack. They do not have legacy versions.

|Activity|Description|
|--------|-----------|
|[DHCP Reserve IP v4 Address Range](../concept/c_InfobloxDHCPActivities.md#)|Reserves an IP address range for DHCP use.|
|[DHCP Delete IP Reservation](../concept/c_InfobloxDHCPActivities.md#)|Deletes IP reservations in DHCP using either an IPv4 or IPv6 address range.|
|[DHCP List IP Reservations](../concept/c_InfobloxDHCPActivities.md#)|Generates a list of all the DHCP range reservations on a specific Infoblox server.|
|[List DNS C-records](../concept/c_InfobloxDNSActivities.md#)|Retrieves all canonical \(CNAME\) records from a specified Infoblox server.|
|[Register DNS A-record](../concept/c_InfobloxDNSActivities.md#)|Creates a DNS A record on a specified Infoblox server.|
|[Register DNS C-Record](../concept/c_InfobloxDNSActivities.md#)|Creates a DNS canonical \(CNAME\) record on a specified Infoblox server.|
|[List DNS Record](../concept/c_InfobloxDNSActivities.md#)|Generates a list of all the DNS entries on a specific Infoblox server.|
|[DNS Delete](../concept/c_InfobloxDNSActivities.md#)|Deletes DNS records of any type from in Infoblox server, such as C and A records.|
|[IPAM Register IP Address](../concept/c_InfobloxIPAMActivities.md#)|Registers an IP address in a network using Infoblox IPAM.|
|[IPAM Reserve IP Address](../concept/c_InfobloxIPAMActivities.md#)|Reserves an IP address in a network using Infoblox IPAM.|
|[IPAM List IP Reservations](../concept/c_InfobloxIPAMActivities.md#)|Returns an array of all IP Address within the named Infoblox Server.|
|[IPAM Delete](../concept/c_InfobloxIPAMActivities.md#)|Deletes an IP Address within a named Infoblox server.|
|[Create Network](../concept/c_InfobloxNetworkActivities.md#)|Creates networks on a specified Infoblox server.|
|[Get Network Details](../concept/c_InfobloxNetworkActivities.md#)|Retrieves the information about a specific network on an Infoblox server.|
|[Delete Network](../concept/c_InfobloxNetworkActivities.md#)|Deletes a network from an Infoblox server.|
|[List Registered Networks](../concept/c_InfobloxNetworkActivities.md#)|Retrieves all the networks associated with an Infoblox server.|

## Microsoft Exchange activities

All Exchange Orchestration activities were rewritten in the Geneva release as scoped activities and are available in the Exchange activity pack. All previous version Exchange activities that were built on activity definitions are deprecated and are unavailable for use in new workflows.

|Activity|Description|
|--------|-----------|
|[Create Address List](r_CreateAddressListActivity.md)|Creates an address list that acts as an alias for emailing all users in the group. This alias cannot be used to manage user permissions.|
|[Delete Address List](r_DeleteAddressListActivity.md)|Removes an existing address list from an Exchange server.|
|[Get Address List](r_GetAddressListActivity.md)|Retrieves all attributes from the specified Exchange address list.|
|[Move Address List](r_MoveAddressListActivity.md)|Moves an Exchange address list to another location in the address hierarchy.|
|[Set Address List](r_SetAddressListActivity.md)|Modifies an Exchange address list.|
|[Update Address List](r_UpdateAddressListActivity.md)|Adds or removes users from the specified address list and immediately applies any cached address list changes to the server.|
|[Create Mailbox](r_CreateMailboxActivity.md)|If a user does not exist, creates a new Active Directory user and associated Exchange mailbox.|
|[Delete Mailbox](r_DeleteMailboxActivity.md)|Deletes the Exchange mailbox of an Active Directory user.|
|[Disable Mailbox](r_DisableMailboxActivity.md)|Disables the mailbox associated with a specified Active Directory account.|
|[Enable Mailbox](r_EnableMailboxActivity.md)|Creates a mailbox for an existing Active Directory user.|
|[Get Mailbox](r_GetMailboxActivity.md)|Gets the mailbox for the specified user or all mailboxes on an Exchange server.|
|[Set Mailbox](r_SetMailboxActivity.md)|Modifies the settings of an existing Exchange mailbox.|

## PowerShell activities

These PowerShell activities were rewritten as scoped activities and are available in the PowerShell activity pack. All previous version PowerShell activities that were built on activity definitions are deprecated and are unavailable for use in new workflows.

|Activity|Description|
|--------|-----------|
|[Install Windows App](r_InstallWindowsAppActivity.md#)|Installs an application on a Windows target machine.|
|[Join Domain](r_JoinDomainActivity.md)|Joins a Windows machine to a domain.|
|[Restart Windows Server](r_RestartWindowsServerActivity.md)|Restarts a Windows server using PowerShell.|
|[Uninstall Windows App](r_UninstallWindowsAppActivity.md)|Uninstalls an application from a Windows target machine.|
|[Change Service State](r_ChangeServiceState.md)|Starts or stops a Windows service on a remote system.|

## Probe activities

These probe activities were rewritten as scoped activities and are available in the Probe activity pack. All previous versions of these activities that were built on activity definitions are deprecated and are unavailable for use in new workflows.

|Activity|Description|
|--------|-----------|
|[Resolve DNS Name](../concept/probe_activity-pack.md#)|Resolves an IP address or a fully qualified domain name \(FQDN\) into one or more IP addresses.|
|[SNMP Query](../concept/probe_activity-pack.md#)|Queries an SNMP device.|

## SCCM activities

All these activities are scoped and part of the SCCM activity pack. They do not have legacy versions.

|Activity|Description|
|--------|-----------|
|[Add to Device Collection](r_AddToDeviceCollectionActivity.md)|Adds a device to a Microsoft System Center Configuration Manager \(SCCM\) device collection.|
|[Add to User Collection](r_AddToUserCollectionActivity.md)|Adds a user to a Microsoft System Center Configuration Manager \(SCCM\) user collection.|
|[Get Applications](r_GetApplicationsActivity.md)|Returns a list of all the applications available on a Microsoft System Center Configuration Manager \(SCCM\) server.|
|[Get Deployments](r_GetDeploymentsActivity.md)|Returns the list of deployments performed by Orchestration using a Microsoft System Center Configuration Manager \(SCCM\) server.|
|[Get Device Collections](r_GetDeviceCollectionsActivity.md)|Returns the list of available device collections on a Microsoft System Center Configuration Manager \(SCCM\) host.|
|[Get User Collections](r_GetUserCollectionsActivity.md)|Returns the list of available user collections on a Microsoft System Center Configuration Manager \(SCCM\) host.|
|[Remove from Device Collection](r_RemoveFmDevicCollectionActivity.md)|Removes a device from a Microsoft System Center Configuration Manager \(SCCM\) device collection.|
|[Remove from User Collection](r_RemoveFromUserCollectionActivity.md)|Removes a user from a Microsoft System Center Configuration Manager \(SCCM\) user collection.|

## SSH activities

These SSH activities were rewritten as scoped activities and are available in the SSH activity pack. The SSH activities not converted to scoped activities were moved to the Orchestration - Deprecated category, but are still available for all workflows.

|Activity|Description|
|--------|-----------|
|[File Copy](r_FileCopyActivity.md)|Copies a file on a Linux or Unix computer, via SSH.|
|[File Read](r_FileReadActivity.md)|Reads a file on a Linux or Unix computer, via SSH.|
|[File Write](r_FileWriteActivity.md)|Writes a file on a Linux or UNIX computer.|
|[File Replace String](r_FileReplaceStringActivity.md)|Finds and replaces a string in a file on a Linux or UNIX computer.|
| | |
|[Files Compare](r_FilesCompareActivity.md)|Compares two files on a Linux or Unix computer, via SSH.|
|[Reset Linux User Password](r_ResetLinuxUserPasswordActivity.md)|Resets the password for a given user on a Linux computer.|
|[Secure Copy](r_SecureCopyActivity.md)|Copies a file from one host to another, without storing the copied file on the MID Server.|

## SFTP activities

All these activities are scoped and part of the SFTP File Transfer activity pack. They do not have legacy versions.

|Activity|Description|
|--------|-----------|
|[Copy File](r_CopyFileActivity.md)|Copies a file from an SFTP server \(source host\) to another SFTP server \(target host\).|
|[Create Directory](r_CreateDirectoryActivity.md)|Creates a directory on an SFTP server.|
|[Get File List](r_GetFileListActivity.md)|Returns a list of files from a given directory and its subdirectories on an SFTP server \(source host\).|
|[Remove File or Directory](r_RemoveFileOrDirectoryActivity.md)|Removes a file or a directory on an SFTP server, including subdirectories, when configured.|
|[Rename File or Directory](r_RenameFileOrDirectoryActivity.md)|Renames a file or directory to a new name on an SFTP server.|
|[Set File Attributes](r_SetFileAttributesActivity.md)|Sets common file attributes, such as timestamps, size, permissions, and UID/GID, for a file or directory on an SFTP server.|

## Deprecated activities

These activities have been removed from the Workflow Editor and are not available for new workflows, but continue to work normally in existing workflows. You can [reactivate the deprecated activity](../task/t_ReactivateDeprecatedActivity.md) or duplicate the functionality of a deprecated activity as a scoped activity by recreating it using the [activity designer](../../orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md).

|Activity|Description|
|--------|-----------|
|[Run Probe](r_OrchestrationBasicActivities.md)|Launches a MID Server probe on behalf of a document.|
|[SOAP Request](r_OrchestrationBasicActivities.md)|Executes a SOAP request on a target server. The [SOAP Message](r_SOAPMessageActivity.md) activity replaces this activity.|
|[Run Command](../concept/c_OrchestrationSSHActivities.md#)|Runs a command \(including shell scripts\) on a Linux or UNIX computer.|
|[Run SCP](../concept/c_OrchestrationSSHActivities.md#)|Uses Secure Copy Protocol \(SCP\) to copy a file from one computer to another, including the directory in which the file resides. The [Secure Copy](r_SecureCopyActivity.md) activity replaces the Run SCP activity.|
|[Run Powershell](../concept/c_OrchestrPowerShellActivities.md#)|Executes Windows PowerShell commands on a MID Server.|

**Parent Topic:**[Activate Orchestration](../../../product/orchestration/task/t_ActivateOrchestration.md)

