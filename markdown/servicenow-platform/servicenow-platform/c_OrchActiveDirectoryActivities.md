---
title: Active Directory activity pack
description: The Active Directory \(AD\) activity pack enables an administrator to create, delete, and manage objects in Windows Active Directory, such as users, groups, and computers, using a ServiceNow Orchestration workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Active Directory activity pack

The Active Directory \(AD\) activity pack enables an administrator to create, delete, and manage objects in Windows Active Directory, such as users, groups, and computers, using a ServiceNow Orchestration workflow.

Activities in this pack can reset a password automatically from a user request or manage any user account in Active Directory, whether or not it was created by a Orchestration workflow.

Domain controllers are identified by the IP address of the host machine. To use the hostname of the domain controller, add the Resolve DNS Name activity to resolve the hostname into an IP, and then pass the IP into the Active Directory activity.

Your instance must have access to a MID Server configured to use PowerShell to run these activities.

**Note:** All Active Directory activities pass through error messages returned from Active Directory. To view these error messages, point to the failed activity in the workflow canvas or select the **Workflow Log** tab in a Workflow Context record.

## Custom Active Directory activities

Orchestration provides custom Active Directory activities that were created with the Orchestration [Create a PowerShell activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_CreateAPowershellActivity.md), starting with the Geneva release. These activities perform the same functions as AD activities by the same name from previous releases and replace those activities for all new workflows. Existing workflows from earlier versions that were created with legacy AD activities continue to function normally after an upgrade to Istanbul. However, all new workflows must use these custom AD activities. The Powershell activity template gives workflow administrators the ability to store input and output variables from the [Query AD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/r_QueryAD.md) activity in the [Databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/c_OrchestrationDatabus.md).

**Note:** To use the Active Directory custom activities, you must [request activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_ActivateAnActivityPack.md) of the Orchestration - Active Directory plugin.

## Active Directory credentials with LDAP

If you are using an LDAP Server with MID Servers, note that Orchestration and Active Directory activities do not use the user name and password configured on LDAP Servers. You must create a [Windows type orchestration credential record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_WindowsCredentialsForm.md) [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_WindowsCredentialsForm.md). The username and password in the credentials record is used for LDAP queries that Orchestration and workflow activities perform.

## Connection port used by AD Orchestration activities

All Active Directory activities use port 389 for LDAP access. If you are using AD activities with Oracle Virtual Directory \(OVD\) as a proxy, set up pass-through on port 389 only.

