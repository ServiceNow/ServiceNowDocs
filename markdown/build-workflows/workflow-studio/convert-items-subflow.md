---
title: Convert items to subflow
description: Convert consecutive items of a flow into a new subflow that preserves data pill references between the converted items. Update the original flow to replace the converted items with a call to the new subflow.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building subflows, Use, Workflow Studio, Build workflows]
---

# Convert items to subflow

Convert consecutive items of a flow into a new subflow that preserves data pill references between the converted items. Update the original flow to replace the converted items with a call to the new subflow.

## Before you begin

-   Role required: flow\_designer or admin
-   Read and write access to the source flow

## About this task

Converting actions into a subflow preserves data pill references and transform functions from the original flow. Workflow Studio creates the new subflow in the same application scope as the original flow.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Open the flow you want edit.

3.  Next to the ACTIONS header, select the **Select multiple** link.

    ![Location of the Select multiple link on a flow containing a trigger and three actions](../images/example-select-multiple.png)

    **Important:** The flow must contain at least two actions in order to display the Select multiple link.

    Workflow Studio displays a checkbox next to each action.

4.  Select one or more consecutive actions to convert.

    **Important:** You can't convert a Set Flow Variables flow logic available in one flow to a new subflow. Instead you must define and set flow variables in the subflow in which you want to use them.

5.  From Operations menu, select the Convert to subflow icon \(![Hovering over the Convert to subflow icon to display the tooltip](../images/convert-to-subflow.png)\).

    ![Operations menu when multiple items are selected.](../images/example-convert-items-to-sublfow.png)

    **Important:** You must have write access to the flow to convert items to a subflow. A read-only protected flow doesn't support converting items into a subflow.

    Workflow Studio displays the Convert to subflow dialog box.

6.  In the dialog box, enter the name of the subflow you want to create.

    ![Convert actions to subflow dialog box with a sample Subflow name of Assign to and notify network group.](../images/example-convert-items-to-sublfow-02.png)

7.  Select **OK**.

    ![New subflow containing the actions from the converted flow](../images/example-convert-items-to-subflow-03.png)

    The selected actions are removed and replaced by the Call a subflow flow logic block. Workflow Studio creates and publishes a subflow that contains the same actions, input values, references, and transform functions from the original flow.


## Result

![Original flow now only has one step to call the Assign to and notify network group subflow](../images/example-convert-items-to-subflow-04.png)

Workflow Studio updates data pill references in the original flow to their new locations. References to actions within the new subflow include their new subflow name. References to actions within the original flow include their new sequence number.

## What to do next

Review the new subflow, and update the original flow to provide the input values needed for the subflow.

**Parent Topic:**[Building subflows](../concept/subflows.md)

