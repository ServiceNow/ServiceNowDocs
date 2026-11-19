---
title: Create Task action
description: Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/create-task-flow-designer.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Actions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Create Task action

Create a task record in an extension of the Task table. After you choose the task table, you can dynamically select the fields to configure the action. Defining the Parent field associates the task to a parent record.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

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


## Create an incident task from an incident

\[Omitted image "example-create-task-action.png"\] Alt text: Create Task action configured to create an Incident Task.

In this example, a flow starts when a high priority network incident is created. The flow creates an Incident Task record where the Parent field is set to the trigger incident, the Short Description inherits the incident short description, and the Assignment group is set to Network. Since there are no more actions in the flow, there's no need to select the Wait option to pause the flow until the Incident Task is complete.

**Parent Topic:**[Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/flow-actions.md)

