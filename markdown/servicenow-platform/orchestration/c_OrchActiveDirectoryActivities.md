---
title: Active Directory activity pack
description: The Active Directory \(AD\) activity pack enables an administrator to create, delete, and manage objects in Windows Active Directory, such as users, groups, and computers, using a ServiceNow Orchestration workflow.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Active Directory activity pack

The Active Directory \(AD\) activity pack enables an administrator to create, delete, and manage objects in Windows Active Directory, such as users, groups, and computers, using a ServiceNow Orchestration workflow.

Activities in this pack can reset a password automatically from a user request or manage any user account in Active Directory, whether or not it was created by a Orchestration workflow.

Domain controllers are identified by the IP address of the host machine. To use the hostname of the domain controller, add the Resolve DNS Name activity to resolve the hostname into an IP, and then pass the IP into the Active Directory activity.

Your instance must have access to a MID Server configured to use PowerShell to run these activities.

**Note:** All Active Directory activities pass through error messages returned from Active Directory. To view these error messages, point to the failed activity in the workflow canvas or select the **Workflow Log** tab in a [Workflow Context](https://www.servicenow.com/docs/access?context=r_AdministeringWorkflowContexts&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) record.

## Custom Active Directory activities

Orchestration provides custom Active Directory activities that were created with the Orchestration [Create a PowerShell activity](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#), starting with the Geneva release. These activities perform the same functions as AD activities by the same name from previous releases and replace those activities for all new workflows. Existing workflows from earlier versions that were created with legacy AD activities continue to function normally after an upgrade to Istanbul. However, all new workflows must use these custom AD activities. The Powershell activity template gives workflow administrators the ability to store input and output variables from the [Query AD](../reference/r_QueryAD.md) activity in the [Databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

**Note:** To use the Active Directory custom activities, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - Active Directory plugin.

## Active Directory credentials with LDAP

If you are using an LDAP Server with MID Servers, note that Orchestration and Active Directory activities do not use the user name and password configured on LDAP Servers. You must create a [Windows type orchestration credential record](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). The username and password in the credentials record is used for LDAP queries that Orchestration and workflow activities perform.

## Connection port used by AD Orchestration activities

All Active Directory activities use port 389 for LDAP access. If you are using AD activities with Oracle Virtual Directory \(OVD\) as a proxy, set up pass-through on port 389 only.

-   **[Add User to Group AD activity](../reference/r_AddUserToGroupADActivity.md)**  
The Add User to Group activity adds a user to a group in Windows Active Directory.
-   **[Change AD User Password activity](../reference/r_ChangeADUserPassword.md)**  
The Change AD User Password activity changes the password for an Active Directory user account.
-   **[Create AD Object activity](../reference/r_CreateADObject.md)**  
The Create AD Object activity creates an object in Windows Active Directory.
-   **[Disable AD User Account activity](../reference/r_DisableADUserAccount.md)**  
The Disable AD User Account activity disables a Windows Active Directory user account, making it inactive.
-   **[Enable AD User Account activity](../reference/r_EnableADUserAccount.md)**  
The Enable AD User Account activity enables a Windows Active Directory user account, making it active.
-   **[Is AD Account Locked activity](../reference/r_IsADAccountLocked.md)**  
The Is AD Account Locked activity determines whether an Active Directory user account is locked.
-   **[Query AD activity](../reference/r_QueryAD.md)**  
The Query AD activity retrieves entries from the Windows Active Directory based on an LDAP search filter and stores the results as a JSON string that can be used in the data bus.
-   **[Remove AD Object activity](../reference/r_RemoveADObject.md)**  
The Remove AD Object activity deletes an object from Windows Active Directory.
-   **[Remove User from Group AD activity](../reference/r_RemoveUserFromGroupADActivity.md)**  
The Remove User from Group activity removes a user from a group in Windows Active Directory.
-   **[Reset AD User Password activity](../reference/r_ResetADUserPassword.md)**  
The Reset AD User Password activity resets the password of a user account in Windows Active Directory.
-   **[Unlock AD Account activity](../reference/r_UnlockADAccount.md)**  
The Unlock AD Account activity unlocks a locked Active Directory user account.
-   **[Update AD Object activity](../reference/r_UpdateADObject.md)**  
The Update AD Object activity updates an object in Windows Active Directory.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

