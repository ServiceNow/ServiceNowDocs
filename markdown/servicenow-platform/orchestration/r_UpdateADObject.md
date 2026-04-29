---
title: Update AD Object activity
description: The Update AD Object activity updates an object in Windows Active Directory.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update AD Object activity

The Update AD Object activity updates an object in Windows Active Directory.

This activity only replaces existing values with new values. It cannot add new values to AD records such as adding a new group member to an AD group. For complex AD operations, use the [Run PowerShell activity](../concept/c_OrchestrPowerShellActivities.md#) instead. The activity fails if it cannot find an existing account with matching object name and data.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

<table id="table_yss_srh_dp"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DomainController

</td><td>

IP address of the domain controller machine.

</td></tr><tr><td>

ObjectName

</td><td>

The sAMAccountName of the Active Directory object.

</td></tr><tr><td>

ObjectData

</td><td>

A JSON object containing Active Directory properties and their values. For example, to set the first name, last name, and title of a user, clear the user's manager, and set the VIP flag to true, the Object Data specifies:```
{ "givenName" : "John", "SN" : "Doe", "title" : "Sr. Account Specialist", "manager" : null, "msTSAllowLogon" : false }
```

</td></tr><tr><td>

Type

</td><td>

The object type to update: user, group, or computer.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|AD object was successfully updated.|
|Failure|An error occurred while attempting to update an AD object. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

