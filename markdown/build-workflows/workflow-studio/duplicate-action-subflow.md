---
title: Duplicate an action or subflow
description: Duplicate an action or subflow within a flow.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Duplicate an action or subflow

Duplicate an action or subflow within a flow.

## Before you begin

Role required: admin or flow\_designer

## About this task

This procedure can only duplicate an action or subflow within the current flow. You can't directly duplicate an action to move it from one flow to another. If you need to move content between flows, you can use one of these alternatives.

-   Create a custom action that hard-codes the values you want to duplicate between flows. For more information about creating a custom action, see [Create an action in Workflow Studio](create-action.md).
-   Convert one or more items in the current flow to a subflow. Call the subflow from each flow that needs the duplicated content. For more information about converting items to a subflow, see [Convert items to subflow](convert-items-subflow.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Flows**.

3.  Select the flow containing the action or subflow that you want to duplicate.

4.  Under Actions, point to the action or subflow that you want to duplicate, and then from the list of icons at the end of the line by the Data pane, select the duplicate action icon \(![Duplicate action icon](../images/duplicate-action-icon.png)\).

    ![Example flow where the first Look Up Record action is highlighted to display Duplicate Action.](../images/example-duplicate-action.png)


## Result

![Example flow where a second Look Up Record action has been duplicated.](../images/example-duplicate-action-result.png)

Your selected action or subflow duplicates directly under itself. All configurations, including [transform functions](../concept/transform-functions.md), are copied over to the duplicated action or subflow.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

