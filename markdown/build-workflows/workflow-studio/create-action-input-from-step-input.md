---
title: Create an action input from a step input
description: Create an action input based on the data type of a step input. Map the step input value to the new action input.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an action in Workflow Studio, Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create an action input from a step input

Create an action input based on the data type of a step input. Map the step input value to the new action input.

## Before you begin

Role required: admin or action\_designer

## About this task

You can use a step input as a template for an action input. Workflow Studio can create an action input of the same data type as the step input.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Action**.

3.  Create an action or open an existing action.

4.  Add a step or select an existing step.

5.  Select the Data Pill Picker icon for the step input you want to use as a template for an action input.

6.  Select the plus icon next to the **Inputs** option.

    ![Example data pill picker with a plus sign next to the Inputs option.](../images/create-action-input-from-step-input.png)


## Result

Workflow Studio creates an input named after the step and input type. For example create\_record\_table\_name, which is an input created for the Create Record step and the Table input. The action input is of the same data type as the step input, for example Table Name. The step input is mapped to the new action input, and the action input is available from the Data pane.

![Example action input named after the create record step.](../images/create-action-input-from-step-input-mapping.png)

**Parent Topic:**[Create an action in Workflow Studio](create-action.md)

