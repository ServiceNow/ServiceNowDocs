---
title: Variables.\[Table\] data type
description: Store a reference to a specific table of Glide variables such as a decision input variable.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Variables.\[Table\] data type

Store a reference to a specific table of Glide variables such as a decision input variable.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options for Variables

|Option|Description|
|------|-----------|
|Data Definition|Specifies the table that stores Glide variables. Each variable type has its own source table to store variables and their associated data as name-value pairs. Some tables that store variables don't support directly adding or editing variable records. For example, the variables of an action or subflow are defined when you create the action or subflow. Edit the action or subflow to change the variables, rather than directly editing the table that stores the variables.|
|Depends-On Another Input|Specifies whether the data definition value is determined by another input. Use this option to dynamically set the data definition rather than hard-code it to a specific value.|

## Log decision input variables

This example logs a decision input variable. Create an action with a single input of type variable. Select the Decision Input \[sys\_decision\_input\] table as the source of the variable.

![input variable of type variable where the source table is Decision Input](../images/example-variable-sys_decision_input.png "Example action input with variable data type")

Add a log step to store the results of your variable selection. Test the action to see a choice list of available decision inputs. Select a decision input type to see its variables. For example, select the Callback Topic Policy to display three variables.

-   portal
-   channel\_id
-   provider\_application\_id

![Variables for the Callback Topic Policy decision input](../images/example-test-variable-sys_decision_input.png "Example variables for the Callback Topic Policy decision input")

Each decision input that you select displays a different set of variables.

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

