---
title: Universal Task form
description: Universal Task form to create a task record.
locale: en-US
release: zurich
product: Universal Task
classification: universal-task
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Universal Task, Employee Service Management]
---

# Universal Task form

Universal Task form to create a task record.

<table id="table_adv_fm3_xnb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td colspan="2">

Unique number that is generated for the Universal Task. The Universal Task number starts with UNT.

</td></tr><tr><td>

Parent

</td><td colspan="2">

Number of the parent case or request.

</td></tr><tr><td>

Parent Assignment Group

</td><td colspan="2">

Group assigned to the parent case or request.

</td></tr><tr><td>

Parent Assigned to

</td><td colspan="2">

Agent primarily responsible for working on the parent case or request.

</td></tr><tr><td rowspan="8">

Type

</td><td colspan="2">

Type of task being assigned. The available options are:-   Submit Catalog Item
-   Upload Documents
-   Upload Documents
-   Mark When Complete
-   Checklist
-   Collect Employee Input

</td></tr><tr><td>

Submit Catalog Item

</td><td>

In the **Catalog item** field, select a catalog item.

</td></tr><tr><td>

Upload Documents

</td><td>

Use the **Description** field to provide instructions or details of documents to be uploaded.

</td></tr><tr><td>

Mark When Complete

</td><td>

Use the **Description** field to provide details about this task. **Note:** The state of the task will change to **Complete** after the employee completes the task.

</td></tr><tr><td>

Checklist

</td><td>

In the **Checklist** section, add the checklist items. For detailed information, see [Create a checklist](https://www.servicenow.com/docs/access?context=t_CreateAChecklist&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

</td></tr><tr><td>

Collect Employee Input

</td><td>

In the **Employee form** field, select the employee form that the user will fill out. **Note:** Employee forms can be built using the survey designer. See [Create an employee form](../task/ut-create-employee-form.md) for more information.

</td></tr><tr><td>

URL

</td><td>

In the **URL** field, specify a URL that will be displayed in the task that is assigned to the user.In the **Short description** field, provide more details about the URL.

</td></tr><tr><td colspan="2">

To know more about the function of each type, see [Universal Task types](../concept/universal-task-types.md)

</td></tr><tr><td>

Employee form

</td><td colspan="2">

Mandatory employee form. **Note:** This field appears only if the Collect Employee Input task is selected in the **Type** field.

</td></tr><tr><td>

Survey instance

</td><td colspan="2">

Link to the completed employee form. **Note:** This field appears only if the Collect Employee Input task is selected in **Type** field, and the value of the **State** field is complete.

</td></tr><tr><td>

Template

</td><td colspan="2">

Task template to auto-fill the task form.

</td></tr><tr><td rowspan="5">

State

</td><td colspan="2">

State of the Universal Task. The available state settings are:-   New
-   Work In Progress
-   Complete
-   Cancelled

</td></tr><tr><td>

New

</td><td>

Default state when the task is a draft. Tasks at this state are only visible to the agent

</td></tr><tr><td>

Work in Progress

</td><td>

Task is assigned to and visible to the employee.

</td></tr><tr><td>

Complete

</td><td>

Task has been completed by the employee.

</td></tr><tr><td>

Cancelled

</td><td>

Task has been cancelled before completion.

</td></tr><tr><td rowspan="5">

Priority

</td><td colspan="2">

Value that identifies how quickly the service desk should address the request. The available options are:-   Critical
-   High
-   Moderate
-   Low

</td></tr><tr><td>

Critical

</td><td>

Highest priority for urgent or time-sensitive tasks.

</td></tr><tr><td>

High

</td><td>

Tasks that are important but not urgent.

</td></tr><tr><td>

Moderate

</td><td>

Tasks that should be completed at some point.

</td></tr><tr><td>

Low

</td><td>

Optional tasks.

</td></tr><tr><td>

Assignment group

</td><td colspan="2">

Group assigned to the Universal Task. This field is available for the **Mark When Complete** and **Checklist** task types. Other tasks types require a mandatory update of the **Assigned to** field with the **Assignment group**.**Note:** Email notifications are sent only for the two task types.

</td></tr><tr><td>

Assigned to

</td><td colspan="2">

Employee assigned to the Universal Task.

</td></tr><tr><td>

Due date

</td><td colspan="2">

Expected date for the employee to complete the task.

</td></tr><tr><td>

Watch list

</td><td colspan="2">

Users to receive notifications when there is any change in the task status.

</td></tr><tr><td>

Short description

</td><td colspan="2">

Brief description of the request

</td></tr><tr><td>

Description

</td><td colspan="2">

Detailed description of the request

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td colspan="2">

More information about the change. The information in this field is visible to the customer.

</td></tr><tr><td>

Work notes

</td><td colspan="2">

Information about how to resolve the Universal Task or steps taken to resolve it, if applicable. This note is for internal use. The work notes information is not visible to customers.

</td></tr></tbody>
</table>**Parent Topic:**[Universal Task reference](../concept/universal-task-reference.md)

