---
title: Create a flow variable
description: Create a flow variable to store and retrieve a value throughout a flow.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Flow variables, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow variable

Create a flow variable to store and retrieve a value throughout a flow.

## Before you begin

Role required: flow\_designer or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **New** &gt; **Flow**.

3.  On the Flow Properties form, fill in the fields.

    For more information, see [Create a flow in Workflow Studio](create-flow.md).

4.  Click **Submit**.

5.  Click the more actions icon \(![More actions menu](../images/more-actions-menu-icon.png)\) and select **Flow Variables**.

6.  In the upper-right side of the Flow Variables form, click the plus icon \(![Plus icon.](../../../build/app-engine-studio/image/plus-icon.png)\) to create a variable.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Unique label for the variable. It can consist of any text. The label is visible to the user.|
    |Name|Unique name for the variable. Displays the name used to identify the variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters. The name is not visible to the user, it's what the system uses behind-the-scenes.|
    |Type|Data type for the variable.|

8.  Click **Save**.


## Result

The Data panel displays the variable in the Flow Variables section. It appears as a data pill, with its name and type.

## What to do next

To assign a value to the variable, use the [Set Flow Variables flow logic](../concept/flow-logic-set-flow-variables.md). If you don't assign a value, the default value is null.

**Parent Topic:**[Flow variables](../concept/flow-variables.md)

