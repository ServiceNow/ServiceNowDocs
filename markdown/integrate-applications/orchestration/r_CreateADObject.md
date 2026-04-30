---
title: Create AD Object activity
description: The Create AD Object activity creates an object in Windows Active Directory.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Create AD Object activity

The Create AD Object activity creates an object in Windows Active Directory.

This activity fails if it finds an existing object with matching input variables.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

<table id="table_ix1_llh_dp"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

DomainController

</td><td>

IP address of the domain controller machine.

</td></tr><tr><td>

Type

</td><td>

The object type to create: user, group, or computer.

</td></tr><tr><td>

OU

</td><td>

The organizational unit to which this object belongs.

</td></tr><tr><td>

ObjectName

</td><td>

The sAMAccountName of the Active Directory object. **Object name** is also used for the **name** attribute in Active Directory. This behavior is available in **ActiveDirectory.psm1**. Whatever is passed as the **Object name** becomes both the **samAccountName** and the **name** of the new user in Active Directory.

</td></tr><tr><td>

ObjectData

</td><td>

A JSON object containing Active Directory property names and their corresponding values. For example:```
{ 
  "givenName" : "John",
  "SN" : "Doe",
  "title" : "Sr. Account Specialist",
  "allowLogin" : true
}

```

This example sets the first name \(givenName\), last name \(SN\), and title on the Active Directory user account and allows that user to log in \(allowLogin\). This field allows expression evaluation via the $\{\} variable substitution syntax.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|A Windows Active Directory object was created successfully.|
|Failure|An error occurred while attempting to create the AD object. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

