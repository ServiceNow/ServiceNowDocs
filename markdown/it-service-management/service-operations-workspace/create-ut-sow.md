---
title: Create a universal task for a universal request in Service Operations Workspace
description: Create a universal task for a request and assign it to the employee or create multiple tasks for a request by using Universal Task.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Universal Task in Service Operations Workspace, Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a universal task for a universal request in Service Operations Workspace

Create a universal task for a request and assign it to the employee or create multiple tasks for a request by using Universal Task.

## Before you begin

Role required: admin

## Procedure

1.  Open the ticket that you want to create a universal task for.

2.  Click the UI action for creating a universal task.

3.  On the form, fill in the fields.

<table id="table_adv_fm3_xnb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td colspan="2">

Unique number that is generated for the Universal Task.

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

</td></tr><tr><td>

Type

</td><td colspan="2">

Type of task being assigned.

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

</td></tr><tr><td>

State

</td><td colspan="2">

State of the Universal Task.

</td></tr><tr><td>

Priority

</td><td colspan="2">

Value that identifies how quickly the service desk should address the request.

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
</table>4.  Select one of the following.

    |Option|Description|
    |------|-----------|
    |**__Ready for work__**|Task is created. The state of the task changes to Work in Progress, and the employee is notified about the task.|
    |**__Submit__**|Task is created. The state of the task remains New, and no notification is sent to the employee.|


**Parent Topic:**[Using Universal Task in Service Operations Workspace](../concept/using-ut-sow.md)

