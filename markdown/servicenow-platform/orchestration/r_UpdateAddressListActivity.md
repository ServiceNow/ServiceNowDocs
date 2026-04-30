---
title: Update Address List activity
description: The Update Address List activity adds or removes users from the specified address list and immediately applies any cached address list changes to the server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update Address List activity

The Update Address List activity adds or removes users from the specified address list and immediately applies any cached address list changes to the server.

Use the optional parameters variable to specify which users to add or remove. This activity implements the Microsoft Exchange [Update-AddressList](https://technet.microsoft.com/en-us/library/aa997982%28v=exchg.160%29.aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Address List**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|hostname|The hostname of the Exchange server with which the activity interacts. Do not enter an IP address in this variable.|
|domain|The name of the Exchange server's assigned domain.|
|identity|Name of the address list to update.|
|domainController|Fully-qualified domain name \(FQDN\) of the domain controller that writes to Active Directory.|
|whatif|A check box that indicates if the activity should stage the changes without applying them. Use this variable to test your activity settings before using the activity in a live workflow. When this variable is selected, the Exchange server does not make any changes but indicates if the command would succeed or fail. You can review any messages from the Exchange server using the ECC queue.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Either **Success** or **Failure**.|
|error|Error message if the operation fails.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in adding or removing users from the specified address list.|
|Failure|The activity failed to add or remove users from the specified address list.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

