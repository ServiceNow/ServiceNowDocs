---
title: Remove AD Object activity
description: The Remove AD Object activity deletes an object from Windows Active Directory.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Active Directory activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Remove AD Object activity

The Remove AD Object activity deletes an object from Windows Active Directory.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

**Note:** This activity replaces an AD activity by the same name available in prior releases. If you have a workflow that uses the deprecated activity, your workflow will continue to work normally after upgrading to Instanbul. However, all new workflows must use the custom version of this activity, which was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md).

## Input variables

<table id="table_pm1_lph_dp"><thead><tr><th>

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

Type

</td><td>

The object type to remove: -   **user**
-   **group**
-   **computer**

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|AD object was successfully removed.|
|Failure|An error occurred while attempting to remove the AD object. Additional details may be available in the workflow log.|

**Parent Topic:**[Active Directory activity pack](../concept/c_OrchActiveDirectoryActivities.md)

