---
title: Pass a variable from a workflow to a subflow
description: Use this process to pass variables from a parent workflow to a subflow.Define the input variables for a workflow to request from parent workflows when it is launched as a subflow.Use this procedure to add a subflow to a workflow.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflows used as subflows, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Pass a variable from a workflow to a subflow

Use this process to pass variables from a parent workflow to a subflow.

## Before you begin

Role required: workflow\_admin, workflow\_creator, or admin

## About this task

**Note:** You can also use the **Return Value** activity in the subflow to return values to the parent workflow. Make sure to have a **Return Value** on every ending transition path.

## Procedure

1.  Prepare the subflow to accept variables from the parent workflow by defining the inputs.

2.  Include the subflow in the parent workflow and connect the inputs to the parent workflow variables.

    **Note:** You cannot pass variables to a subflow that runs on the Requested Item \[sc\_req\_item\] table.


**Parent Topic:**[Workflows used as subflows](../reference/workflows-as-subflows.md)

## Define inputs for a subflow

Define the input variables for a workflow to request from parent workflows when it is launched as a subflow.

### About this task

All inputs are stored in the Variables \[var\_dictionary\] table.

### Procedure

1.  In the editor, open and check out the workflow.

2.  In the title bar, click the menu icon and select **Edit Inputs**.

3.  In the Workflow Inputs window, click **New**.

4.  Populate the record with the definition of the variable, including the column name, the label that is displayed to the user, and the type of field.

5.  Click **Submit**.


## Invoke a subflow in a workflow

Use this procedure to add a subflow to a workflow.

### Procedure

1.  In the Workflow Editor, open and check out the parent workflow.

2.  Drag the subflow from the **Workflows** tab to the parent workflow.

3.  In the New Activity dialog box, define the variables defined by the subflow's **Inputs**.

    These fields can accept both static values or variables in the following format:

    `${variable_name}`

4.  Click **Submit**.

    The workflow triggers the subflow at the appropriate time and passes the variables as indicated by the **Inputs** definition.


