---
title: Change AD User Password activity
description: The Change AD User Password activity changes the password for an Active Directory user account.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Change AD User Password activity

The Change AD User Password activity changes the password for an Active Directory user account.

This activity requires the user's current password to run, unlike the [**Reset AD User Password**](r_ResetADUserPassword.md) activity. If the new password violates any Active Directory password requirements, such as length or character combinations, the activity fails and returns the appropriate error message. This error message appears in the ECC queue and in hint text when a user points to the activity in the Workflow Editor.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

|Variable|Description|
|--------|-----------|
|DomainController|IP address of the domain controller machine.|
|User|The sAMAccountName of the Active Directory user account.|
|New\_password|The new password to assign this user.|
|Old\_password|The user's current password.|

## Output variables

<table id="table_zqz_ftt_ss"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

One of the following outcomes:-   **failure**
-   **success**
-   **Policy Failure**
-   **Incorrect old password**

</td></tr><tr><td>

errorMessage

</td><td>

The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).

</td></tr><tr><td>

hresult

</td><td>

Powershell command result.

</td></tr></tbody>
</table>## Conditions

The activity provides the following conditions:

|Condition|Description|
|---------|-----------|
|Success|Password successfully reset.|
|Policy Failure|Password does not comply with the organization's Active Directory requirements.|
|Incorrect old password|Password being changed was not entered correctly.|
|Failure|An error occurred while attempting to change the password. Additional details may be available in the workflow log.|

## Active Directory credentials with LDAP

If you are using an LDAP Server with MID Servers, note that Orchestration and Active Directory activities do not use the user name and password configured on LDAP Servers. You must create a [Windows type orchestration credential record](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). The username and password in the credentials record is used for LDAP queries that Orchestration and workflow activities perform.

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

