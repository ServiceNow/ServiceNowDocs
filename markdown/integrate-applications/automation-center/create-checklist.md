---
title: Create a checklist
description: Create a checklist to track the items for an automation request. A checklist is a list of tasks that you must track before publishing an automation request.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with golive checklists, Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Create a checklist

Create a checklist to track the items for an automation request. A checklist is a list of tasks that you must track before publishing an automation request.

## Before you begin

Role required: sn\_ac.automation\_admin

**Note:** The option to create a checklist is available only when the automation request is in the In progress state. For information about moving an automation request to the In progress state, see [Move an automation request to the In progress state](move-automationrequest-to-inprogress.md).

After the automation request is moved to the following states, the option to create a checklist isn’t available:

-   Defer
-   Publish
-   Reject

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  Select the list icon \(![List icon.](../images/autocenter-list-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

4.  Open the automation request for which you want to create a checklist.

    Ensure that the automation request is in the In progress state.

5.  Select the Golive Checklist icon \(![golive checklist icon](../images/icon-golive.png)\) from the side panel.

6.  Select **Create new** from the **Add checklist** list if you want to create a checklist.

    The Details form is displayed. A checklist is a list of tasks.

    You can create a template by yourself or use an available template. The available templates are listed in the drop-down.

7.  Fill details in the Details form.

<table id="choicetable_qpb_b1t_zfc"><thead><tr><th align="left" id="d281237e165">

Field

</th><th align="left" id="d281237e168">

Description

</th></tr></thead><tbody><tr><td id="d281237e174">

**Name**

</td><td>

Provide a name for the checklist.This is a mandatory field.

</td></tr><tr><td id="d281237e185">

**Description**

</td><td>

Provide a description.

</td></tr><tr><td id="d281237e194">

**State**

</td><td>

Provide a state.When a checklist is first created, the state is New. If you’re updating an existing checklist, you can change the state manually.

</td></tr><tr><td id="d281237e205">

**Assignment group**

</td><td>

Select an appropriate assignment group from the list.

</td></tr><tr><td id="d281237e215">

**Assigned to**

</td><td>

Select a user who you want to view and review the checklist.**Note:** The user must have the sn\_ac.automation\_technical\_user role. Based on your choice in the **Assignment group** field, this filed is populated.

</td></tr><tr><td id="d281237e229">

**Due date**

</td><td>

Specify a due date in the provided format.

</td></tr></tbody>
</table>8.  Select **Save**.

    On top of the task that you created, there’s an arrow. Select the arrow to go to the main checklist window.

    ![Moving from task window to checklist window](../images/golive-check.png)

    You can also select the available checklist that is provided with the product. For information, see [Working with golive checklists](../concept/working-golive.md).

9.  Select the + icon if you want to add more tasks to the checklist.

    ![Add task button](../images/golive-addtask.png)

    The Details form is displayed. Fill in the details.


**Parent Topic:**[Working with golive checklists](../concept/working-golive.md)

