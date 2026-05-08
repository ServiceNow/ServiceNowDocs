---
title: Create a work item queue
description: Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a work item queue

Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.

## Before you begin

Role required: awa\_admin or admin

## About this task

Depending on the service channel, additional configuration options are available. For example, in the chat channel you define the standard messages displayed during a chat session with a user.

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Choose a situation.

    -   To create a queue, select **New**.
    -   To change a queue, select the queue record to be updated.
3.  On the form, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the queue. A default queue may be available for the service channel you activated through the plugins related to AWA.

</td></tr><tr><td>

Number

</td><td>

Base number for the table. For more information, see Record numbering.

</td></tr><tr><td>

Service channel

</td><td>

Channel to which the queue belongs. For the chat channel, define the standard messages displayed to chat users in the Chat Messages section.

</td></tr><tr><td>

Active

</td><td>

Option indicating whether the queue is enabled.

</td></tr><tr><td>

Application

</td><td>

Type of scoped application.

</td></tr><tr><td>

Schedule

</td><td>

Support schedule that defines when the queue is available.

</td></tr><tr><td>

Order

</td><td>

During routing, the order in which AWA considers the routing condition for this work item queue, in comparison to other queues.

</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the queue.

</td></tr><tr><td class="sub-head" colspan="2">

Routing Condition

</td></tr><tr><td>

Define condition here

</td><td>

Option that indicates a routing condition is to be applied to the queue. If checked, define the **Condition mode** and **Work item routing condition**.

</td></tr><tr><td>

Condition mode

</td><td>

Type of condition for routing work items in the queue. -   Simple: Specify a routing condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

Work item routing condition

</td><td>

Condition that applies to routing work items to this queue.

 Use the condition builder to select routing conditions. The fields available for selection are based on the selected service channel. For the chat service channel, you can specify chat context variables in the condition builder by dot-walking to related context fields.

 For example, if you defined chat context variables that store pre-chat routing information, you can dot-walk to those chat context variables in the condition builder. You can use the variables in routing conditions to specify where chats are routed.

</td></tr><tr><td>

Script

</td><td>

JavaScript condition statement that specifies the work items to be routed to the queue. The condition must evaluate to true. This field appears only when **Advanced** is selected from Condition mode.

</td></tr><tr><td>

Initial agent response

</td><td>

Message that users see when an agent accepts a chat. For example: `Thank you for contacting support. I am looking into your question now and will be with you shortly.`

</td></tr><tr><td>

Max wait time message

</td><td>

Message that users see when a chat ends because the Max Wait Time has elapsed.This field is required if the **Max Wait Time** is greater than 0.

</td></tr><tr><td>

Target wait time

</td><td>

Estimated time \(Days or Hours, minutes, seconds\) allotted for an agent to accept an item in the queue.

</td></tr><tr><td>

Max Wait Time

</td><td>

Maximum amount of time that all available agents have to accept or reject a chat request. After time runs out, the requester receives the value in either the **Max wait time message** field or the **No Agents Available Message** field defined in [Agent Chat settings](../../conversational-interfaces/task/ac-configure-agent-chat.md).**Note:** The **Max Wait Time** field is available after you associate the queue to the chat service channel.

</td></tr></tbody>
</table>4.  Select **Submit** for a new queue or **Update** to change the queue.

    The queue is added to or updated in the Queues \[awa\_queue\_list\] table.


## What to do next

-   Define the [**Assignment Eligibility**](awa-specify-assignment-eligibility.md).
-   Optionally, define the [**Work Item Sort Order**](awa-set-work-sort-order.md).
-   Optionally, define the [**Queue Triggers**](awa-create-queue-triggers.md).
-   Optionally, define the [**Set Agent Affinity rules**](awa-set-agent-affinity-for-queue.md).

