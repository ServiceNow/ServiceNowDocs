---
title: Set Mailbox activity
description: The Set Mailbox activity modifies the settings of an existing Microsoft Exchange mailbox.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set Mailbox activity

The Set Mailbox activity modifies the settings of an existing Microsoft Exchange mailbox.

Use the optional parameters variable to pass specific values to the Exchange server. This activity implements the Microsoft Exchange [Set-Mailbox](https://technet.microsoft.com/en-us/library/bb123981%28v=exchg.160%29.aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Mailbox**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_klf_tfv_qt"><thead><tr><th>

Variable

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

user

</td><td>

Active Directory user whose mailbox you want to modify. The activity passes this value to Exchange as the Identity Exchange variable.

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

|Conditions|Description|
|----------|-----------|
|Success|The activity succeeded in modifying the settings of the specified mailbox.|
|Failure|The activity failed to modify the settings of the specified mailbox.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

