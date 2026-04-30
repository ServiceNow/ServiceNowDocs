---
title: Create Mailbox activity
description: The Create Mailbox activity creates a new Active Directory user, if that user does not already exist, and a Microsoft Exchange mailbox for that user.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create Mailbox activity

The Create Mailbox activity creates a new Active Directory user, if that user does not already exist, and a Microsoft Exchange mailbox for that user.

This activity implements the Microsoft Exchange [New-Mailbox](http://technet.microsoft.com/en-us/library/aa997663%28v=exchg.150%29.aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Mailbox**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_lgv_2hg_vs"><thead><tr><th>

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

The name of the Exchange server's assigned domain. **Important:** The MID Server must be in the same domain as the Exchange server.

</td></tr><tr><td>

first\_name

</td><td>

First name of the user.

</td></tr><tr><td>

middle\_initial

</td><td>

Middle initial of the user.

</td></tr><tr><td>

last\_name

</td><td>

Last name of the user.

</td></tr><tr><td>

alias

</td><td>

The display name for the mailbox address, the part of the email address to the left of the @ symbol. If no alias is specified, the activity uses First name.Last name as the alias. The alias is also used as the user's principal name \(UPN\) if none is specified in the optional parameters.

</td></tr><tr><td>

password

</td><td>

Password to use for the new mailbox. The password is encrypted when it is sent to the target host.

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
|output|Raw XML payload from the Exchange server. This data includes all Exchange attributes.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in creating a new mailbox for the specified user. If no Active Diectory account existed for that user, this activity succeeded in creating a new account.|
|Failure|The activity failed to create a new mailbox or an Active Directory account for the specified user.|

