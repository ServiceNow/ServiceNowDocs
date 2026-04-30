---
title: Create Catalog Task action
description: Creates a record in the Catalog Task \[sc\_task\] table associated to a requested item in the Requested Items \[sc\_req\_item\] table. Adds the catalog task record as data to be used in the flow.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Create Catalog Task action

Creates a record in the Catalog Task \[sc\_task\] table associated to a requested item in the Requested Items \[sc\_req\_item\] table. Adds the catalog task record as data to be used in the flow.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Table**

    Data type: **Table Name**

    Extension of the Task table in which to create a record. For example, Catalog Task \[sc\_task\] or Incident Task \[incident\_task\].

-   **Requested Item \[Requested Item\]**

    Data type: **Record**

    The requested item record from the Requested Item \[sc\_req\_item\] table that this catalog task fulfills.

-   **Short Description**

    Data type: **String**

    The short description for the catalog task.

-   **Fields**

    Data type: **Template Value**

    The field values that you want to set in the catalog task. If adding the action to a subflow, you can allow flow designers to dynamically set field values. See [Create a template value input](../task/template-value.md).

-   **Wait**

    Data type: **True/False**

    Flag indicating whether to pause the flow until the Task record is no longer active. You can add a wait condition by dragging-and-dropping a True/False data pill into this input. The flow only waits for the Task record to complete when the condition field is true.

-   **Template Catalog Item \[Catalog Item\]**

    Data type: **Record**

    The Catalog Item \[sc\_cat\_item\] record you want to use to populate the catalog variables slush bucket. This input does not support any data pill values.

-   **Catalog Variables**

    Data type: **Slush Bucket**

    The list of catalog variables that you want to show on the catalog task. These variables provide more information to the catalog task fulfiller.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Catalog Task**

    Data type: **Record**

    Reference to Catalog Task record created.


## Use a flow to process a catalog item request

![Configuration of the Create Catalog Task action](../images/example-create-catalog-task-action.png)

In this example, the Service Catalog Item request flow first requests manager and department head approval. Only approved requests ever run the Create Catalog Task action. The Requested Item input uses the requested item that triggered the flow to run. The Fields input sets the value of the task short description, assign group, and description. Since the wait input is selected, the flow will pause while the catalog task is being fulfilled. Also since there is no template catalog item selected, there are no catalog variables available to this task.

![Execution details of Create Catalog Task](../images/example-create-catalog-task-action-execution-details.png)

In this example, the flow execution details show the requested item record number and the catalog task record number. The action state is listed as waiting since the Wait input was selected. The flow waits until the catalog task is closed before continuing.

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

