---
title: Delete Address List activity
description: The Delete Address List activity removes an existing address list from an Exchange server.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Delete Address List activity

The Delete Address List activity removes an existing address list from an Exchange server.

This activity implements the Microsoft Exchange [Remove-AddressList](https://technet.microsoft.com/en-us/library/bb124342%28v=exchg.160%29.aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Address List**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|hostname|The hostname of the Exchange server with which the activity interacts. Do not enter an IP address in this variable.|
|domain|The name of the Exchange server's assigned domain.|
|identity|Name of the address list to remove.|
|domainController|Fully-qualified domain name \(FQDN\) of the domain controller that writes to Active Directory.|
|recursive|Check box that indicates if the activity should delete Active Directory elements that are children of the specified address list.|
|whatif|Check box that indicates if the activity should stage the changes without applying them. Use this variable to test your activity settings before using the activity in a live workflow. When this variable is selected, the Exchange server does not make any changes but indicates if the command would succeed or fail. You can review any messages from the Exchange server using the ECC queue.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|error|Error message if the operation fails.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in removing the address list from the Exchange server.|
|Failure|The activity failed to remove the address list from the Exchange server.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

