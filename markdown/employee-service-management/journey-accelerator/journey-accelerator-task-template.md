---
title: Journey Accelerator task template fields
description: To make a task template, fill in the Journey Accelerator task template fields.
locale: en-US
release: australia
product: Journey Accelerator
classification: journey-accelerator
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Journey Accelerator task template fields

To make a task template, fill in the Journey Accelerator task template fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Descriptive name for the activity that is associated with the task.

</td></tr><tr><td>

**Table**

</td><td>

Table that is used to track tasks and fields. Select the Journey Accelerator Task \[sn\_ja\_task\] table to enable access to the template fields.

</td></tr><tr><td>

**Template**

</td><td>

Template fields that appear only when a table is selected. Template fields are tracked in the Journey Accelerator Task \[sn\_ja\_task\] table.

 The following settings apply to the overall properties of the task:

-   **Mandatory**: Set to **true** to make the task required. Set to **false** to make the task optional.
-   **Type**
    -   **Regular**: Standard to-do task template.
    -   **Calendar**: Schedulable task. Creates to-do task linked to Microsoft Office 365 calendar event.

</td></tr><tr><td>

**Active**

</td><td>

Option that enables the task template when selected. Only active tasks are available for managers to use.

</td></tr><tr><td>

**Task short description**

</td><td>

Brief description of the task. This text appears to users from the Journey Accelerator plan. This field appears in the **Short description** field when you are managing tasks in stages.

</td></tr><tr><td>

**Task description**

</td><td>

Detailed description of the task.

</td></tr><tr><td>

**Parent plan table**

</td><td>

Higher-level table that associates an entry in the Journey Accelerator Task \[sn\_ja\_task\] with the table that tracks plans, Journey Accelerator Plan \[sn\_ja\_plan\]. Selecting the Journey Accelerator enables access to the plan-related fields.

</td></tr><tr><td>

**Assign to source**

</td><td>

User who is assigned the task:-   Employee
-   Manager
-   Mentor

**Note:** Initially, only the first mentor is assigned with to-do tasks in the list with multiple entries. Managers can reassign the to-do tasks to other mentors after the plan is created.


</td></tr><tr><td>

**Relative due date trigger**

</td><td>

Condition that is used to trigger when a task is assigned based on the publish date of the plan. This condition is evaluated with **Date offset type** and **Date offset type**.-   **Created**
-   **End on**
-   **Start on**
-   **Updated**

 **Note:** Only use the **Start on** condition. **Start on** is selected by default.

</td></tr><tr><td>

**Date offset type**

</td><td>

Condition that is used to trigger when a task is assigned. This condition is evaluated with **Relative due date trigger** and **Number of offset days**.-   **On**
-   **After**

 **Note:** The **After** condition is the default selection. We recommend that you use only the After condition.

</td></tr><tr><td>

**Number of offset days**

</td><td>

Condition that is used to trigger when a task is assigned. This condition is evaluated with **Relative due date trigger** and **Date offset type**.-   **Days**
-   **Hours**

 **Note:** Only specify days, and keep hours set at 0 \(zero\).

For example: If the `Relative Due Date Trigger = Start On`, `Date Offset type = After`, and `Number of offset days = 5 days`, the task is configured to trigger 5 days after the publish date of the plan.

</td></tr></tbody>
</table>**Parent Topic:**[Journey Accelerator reference](ja-reference.md)

