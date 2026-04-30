---
title: Move Address List activity
description: The Move Address List activity moves a Microsoft Exchange address list to another location in the address hierarchy.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Move Address List activity

The Move Address List activity moves a Microsoft Exchange address list to another location in the address hierarchy.

This activity implements the Microsoft Exchange [Move-AddressList](https://technet.microsoft.com/en-us/library/bb124520%28v=exchg.160%29.aspx) command.

The Exchange server caches the changes from this activity but does not immediately apply them. Use the [Update Address List](r_UpdateAddressListActivity.md) activity after this activity to apply the changes or wait for the Exchange server to automatically apply cached changes.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Address List**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variables|Description|
|---------|-----------|
|hostname|The hostname of the Exchange server with which the activity interacts. Do not enter an IP address in this variable.|
|domain|The name of the Exchange server's assigned domain.|
|identity|Name of the address list to move.|
|target|Path to the address list's new location.|
|domainController|Fully-qualified domain name \(FQDN\) of the domain controller that writes to Active Directory.|
|whatif|Check box that indicates if the activity should stage the changes without applying them. Use this variable to test your activity settings before using the activity in a live workflow. When this variable is selected, the Exchange server does not make any changes but indicates if the command would succeed or fail. You can review any messages from the Exchange server using the ECC queue.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **success** or **failure**.|
|error|Error message if the operation fails.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in moving the address list to another location.|
|Failure|The activity failed to move the address list to another location.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

