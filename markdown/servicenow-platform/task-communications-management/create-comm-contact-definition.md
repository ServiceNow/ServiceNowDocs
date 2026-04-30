---
title: Define a communication contact
description: Define the recipients of a particular plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle. A notification for a task is sent to all individuals specified for that task.
locale: en-US
release: xanadu
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Define a communication plan, Working with Task Communications Management, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a communication contact

Define the recipients of a particular plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle. A notification for a task is sent to all individuals specified for that task.

## Before you begin

Role required: sn\_comm\_management.communication\_plan\_admin or admin

You have defined a communication plan.

## About this task

You can add or remove any particular communication contact manually.

## Procedure

1.  Navigate to **All** &gt; **Task Communications Management** &gt; **Plan Definitions**.

2.  Click the communication plan that you want to define the contacts for.

3.  Click the **Communication Contact Definitions** related list and then click **New**.

4.  On the form, fill in the fields.

<table id="table_ish_5tl_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of contact such as user, group, or recipient list that you want to involve in the plan. The contact type is assigned dynamically at the time of the table execution. For information on recipient lists, refer [Define a recipient list for communication contact](define-recipient-list-comm-contact.md).

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that the user, group, or individuals in the recipient list are expected to handle.

</td></tr><tr><td>

User

</td><td>

Name of the user, group, or recipient list to be added to the contact list.**Note:** You can use the recipient list to specify dynamic criteria for fetching the list of users for a particular communication plan.

</td></tr></tbody>
</table>5.  Click **Submit**.

    A communication contact is defined for the communication plan.


**Parent Topic:**[Define a communication plan](create-comm-plan-definition.md)

**Related topics**  


[Define a communication task](create-comm-task-definition.md)

[Define a communication channel](create-comm-channel-definition.md)

