---
title: Disable Mailbox activity
description: The Disable Mailbox activity disables the mailbox associated with a specified Active Directory account.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Disable Mailbox activity

The Disable Mailbox activity disables the mailbox associated with a specified Active Directory account.

This activity implements the Microsoft Exchange [Disable-Mailbox](https://technet.microsoft.com/en-us/library/aa997210%28v=exchg.160%29.aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Mailbox**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_swz_rx5_qt"><thead><tr><th>

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

Active Directory user who's mailbox should be disabled. The activity passes this value to Exchange as the Identity Exchange variable.

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

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in disabling the specified mailbox.|
|Failure|The activity failed to disable the specified mailbox.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

