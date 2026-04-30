---
title: Choice data
description: Store choice list values for a specific choice field.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Choice data

Store choice list values for a specific choice field.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options for Choice variables

<table id="table_pmk_lfj_dlb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr id="advanced-data-name"><td>

Name

</td><td>

Displays the name used to identify the data variable in script calls.

</td></tr><tr><td>

Max length

</td><td>

Specifies the maximum length a user can enter for a choice value. Use this option to restrict the length of input values stored during action design.

</td></tr><tr><td>

Hint

</td><td>

Provides guidance to flow or action designers on how to configure the data.

</td></tr><tr><td>

Choice

</td><td>

Specifies whether the choice list has a value for no selection. Options include:-   Dropdown with --None--
-   Dropdown without --None--

 **Note:** The Dropdown with --None-- option requires selecting a default choice.

</td></tr><tr><td>

Default

</td><td>

Specifies the choice used when a flow or action designer does not select a choice.

</td></tr><tr><td>

Choices

</td><td>

Specify the choices available to select. Use the add button \(![Add button](../images/green-add-button.png)\) to create a choice. Each choice must have a **Name**, **Value**, and **Order**. See [Choice list field type](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information about choice lists.

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

