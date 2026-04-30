---
title: Set Address List activity
description: The Set Address List activity modifies a Microsoft Exchange address list.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Set Address List activity

The Set Address List activity modifies a Microsoft Exchange address list.

Use the Optional parameters variable to pass specific values to the Microsoft Exchange server. This activity implements the Microsoft Exchange [Set-AddressList](https://technet.microsoft.com/en-us/library/aa998847%28v=exchg.160%29.aspx) command.

The Exchange server caches the changes from this activity but does not immediately apply them. Use the [Update Address List](r_UpdateAddressListActivity.md) after this activity to apply the changes or wait for the Exchange server to automatically apply cached changes.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Address List**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_ofg_2q5_qt"><thead><tr><th>

Variables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hostname

</td><td>

The hostname of the Exchange server with which the activity interacts. Do not enter an IP address in this variable.

</td></tr><tr><td>

domain

</td><td>

The name of the Exchange server's assigned domain.

</td></tr><tr><td>

identity

</td><td>

Name of the address list to modify.

</td></tr><tr><td>

parameters

</td><td>

Optional parameters to pass to the Exchange server written in JavaScript Object Notation \(JSON\). Exchange activities cannot pass parameters that reference an object, such as a PSCredential object. Plain text is automatically converted to SecureString objects for parameters that require that data type.Attempting to save an activity that specifies duplicate parameters, including parameters from activity variables, or incorrectly formatted JSON causes a warning message to appear.

**Note:** When passing a switch parameter, such as ForceUpgrade, you must use the format **"parameter":"true"**.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|error|Error message if the operation fails.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|The activity succeeded in modifying the specified address list.|
|Failure|The activity failed to modify the specified address list.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

