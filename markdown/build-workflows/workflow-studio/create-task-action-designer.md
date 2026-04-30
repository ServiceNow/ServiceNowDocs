---
title: Create Task step
description: Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create Task step

Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Extension of the Task table in which to create a record. For example, Catalog Task \[sc\_task\] or Incident Task \[incident\_task\].

-   **Field Values**

    Data type: **Template Values**

    Field values to set for the record. For example, to set the short description to a certain value, select **Short description** and set the desired value.

-   **Wait**

    Data type: **True/False**

    Flag indicating whether to pause the flow until the Task record is no longer active. You can add a wait condition by dragging-and-dropping a True/False data pill into this input. The flow only waits for the Task record to complete when the condition field is true.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Table**

    Data type: **Table Name**

    Table where the Task record was created.

-   **Task**

    Data type: **Record**

    Reference to the Task record created.


## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

