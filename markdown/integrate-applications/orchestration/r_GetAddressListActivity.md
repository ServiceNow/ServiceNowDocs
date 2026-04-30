---
title: Get Address List activity
description: The Get AddressList activity retrieves all attributes from the specified Exchange address list.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exchange activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Get Address List activity

The Get AddressList activity retrieves all attributes from the specified Exchange address list.

This activity implements the Microsoft Exchange [Get-AddressList](https://technet.microsoft.com/en-us/library/aa996782(v=exchg.160).aspx) command.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Exchange** &gt; **Address List**.

**Note:** This activity replaces an Exchange activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [PowerShell activity designer](../../orchestration-activity-designer/concept/c_PowershellActivityDesigner.md), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variables|Description|
|---------|-----------|
|hostname|The hostname of the Exchange server with which the activity interacts. Do not enter an IP address in this variable.|
|domain|The name of the Exchange server's assigned domain.|
|domainController|Fully-qualified domain name \(FQDN\) of the domain controller that writes to Active Directory.|
|identity|Name of the address list to get attributes from. If you enter a value in this variable, leave the **container** and **searchText** variables blank.|
|organization|Organization to which the specified address list belongs.|
|searchText|Filter text that causes the activity to return only results that contain this text. This variable can only be used with Exchange 2013 servers. If you enter a value in this variable, leave the **container** and **identity** variables blank.|
|container|Parent address list of the address list from which you want to retrieve attributes. If you enter a value in this variable, leave the **identity** and **searchText** variables blank|

## Output variables

|Variables|Descriptions|
|---------|------------|
|result|Either **success** or **failure**.|
|error|Error message if the operation fails.|
|output|Raw XML payload from the Exchange server. This data includes all Exchange attributes.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in retrieving the attributes from the address list.|
|Failure|The activity failed to retrieve the attributes from the address list.|

**Parent Topic:**[Exchange activity pack](../concept/c_OrchestrationExchangeActivities.md)

