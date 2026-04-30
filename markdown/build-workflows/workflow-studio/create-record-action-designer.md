---
title: Create Record step
description: Creates a record on any table. You can dynamically add and configure fields for the record.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create Record step

Creates a record on any table. You can dynamically add and configure fields for the record.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Table in which to create record.

-   **Fields**

    Data type: **Template Values**

    Field values to set for the record. For example, to set the short description to a certain value, select **Short description** and set the desired value.

    **Important:** The system does not support updating multiple journal fields such as the additional comments or work notes of a task record.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Table**

    Data type: **Table Name**

    Table where record was created.

-   **Record**

    Data type: **Record**

    Reference to record created.


## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

