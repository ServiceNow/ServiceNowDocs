---
title: Reset AD User Password activity
description: The Reset AD User Password activity resets the password of a user account in Windows Active Directory.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Reset AD User Password activity

The Reset AD User Password activity resets the password of a user account in Windows Active Directory.

If the new password violates any Active Directory password requirements, such as length or character combinations, the reset activity fails and returns the appropriate error message. This error appears in the ECC Queue and when you point to the activity in the Workflow Editor.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

|Variable|Description|
|--------|-----------|
|DomainController|IP address of the domain controller machine.|
|User|The sAMAccountName of the Active Directory user account.|
|Password|The new password for the user. This password must comply with the organization's Active Directory requirements.|
|ForceChange|Makes this password temporary by forcing the user to change it at the next login.|
|Unlock|Unlock the account if the account is locked.|

## Output variables

<table id="table_oxz_bg1_ts"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

One of the following outcomes:-   **failure**
-   **success**
-   **Policy Failure**

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

|Condition|Description|
|---------|-----------|
|Success|Password was successfully reset.|
|Policy Failure|New password does not comply with the organization's Active Directory requirements.|
|Failure|An error occurred while attempting to reset the password. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

