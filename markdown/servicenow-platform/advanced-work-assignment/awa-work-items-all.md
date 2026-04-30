---
title: Check work items and AWA events
description: View a list of work items and AWA events.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Check work items and AWA events

View a list of work items and AWA events.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to **Advanced Work Assignment** &gt; **Work Item** &gt; **All**.

    A list of the work items appears.

2.  Select the preview button \(![Preview button](../../../product/configuration-management/image/preview-button.png)\) for the work item you want to view.

3.  On the Work Item dialog box, select **Open Record**.

<table id="table_lhv_3sb_3nb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Exceeded Queue Target Wait Time

</td><td>

Indicator that the interaction has waited longer than the target wait time of the queue.

</td></tr><tr><td>

Queue

</td><td>

Queue assigned to the task.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the task.

</td></tr><tr><td>

Document ID

</td><td>

Document ID assigned to the task.

</td></tr><tr><td>

State

</td><td>

Status of the task:

-   Accepted
-   Canceled
-   Pending Accept
-   Queued


</td></tr><tr><td>

Active

</td><td>

Indicator of whether the task is still being worked on \(active\) or is complete.

</td></tr><tr><td>

Canceled reason

</td><td>

Reason the task was canceled: -   Disqualified from service channel
-   Manually assigned
-   Time out
-   Transfer was canceled or rejected
**Note:** Work items may be canceled if all agents remain at full capacity for the entire interaction.

</td></tr><tr><td>

Is Dismissed

</td><td>

Indicator of whether the task was dismissed.

</td></tr><tr><td>

Rejected

</td><td>

Task that was rejected by the agent.

</td></tr><tr><td>

Timed Out

</td><td>

Task that has exceeded the timeout specified in the assignment rule.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to the task.

</td></tr><tr><td>

Document table

</td><td>

Document table assigned to the task.

</td></tr><tr><td>

Previous Work Item

</td><td>

Reference to a previous work item for the same Document ID.

</td></tr><tr><td>

State changed on

</td><td>

Date that the task state was most recently changed.

</td></tr><tr><td>

Allocated by

</td><td>

User who assigned the work item.

</td></tr><tr><td>

Display Name

</td><td>

Task name.

</td></tr><tr><td>

Offered on

</td><td>

Date the task was first offered to an agent.

</td></tr><tr><td>

Work Item Size

</td><td>

Amount of an agent's capacity used when this task is assigned to the agent.

</td></tr><tr><td>

Wait time

</td><td>

Length of time the task waited in the queue before being assigned.

</td></tr><tr><td>

Assignment rule

</td><td>

Rule that assigns cases that meet the matching rule criteria to a customer service agent.

</td></tr><tr><td>

Offer Count

</td><td>

Number of times the work item was offered to agents.

</td></tr></tbody>
</table>4.  Scroll to the bottom of the Work Item form to view the list of the AWA Events.

5.  Select the preview button ![Preview button](../../../product/configuration-management/image/preview-button.png) for the AWA event you want to view.

6.  On the AWA Event dialog box, select **Open Record**.

<table id="table_yk2_lmc_3nb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Caused By

</td><td>

User who triggered the AWA event.

</td></tr><tr><td>

Record ID

</td><td>

Interaction record ID.

</td></tr><tr><td>

Type

</td><td>

Type of AWA event:-   Assignment
-   Manual Assignment
-   Routing
-   Acceptance
-   Rejection
-   Cancellation


</td></tr><tr><td>

Name

</td><td>

Name of the corresponding interaction.

</td></tr><tr><td>

Channel

</td><td>

Service channel used for the AWA event.

</td></tr><tr><td>

Record table

</td><td>

Table name of document being logged.

</td></tr><tr><td>

Record Details

</td><td>

Details of the work item record.

</td></tr><tr><td>

Timestamp

</td><td>

Date and time the AWA event occurred.

</td></tr><tr><td>

Event Details

</td><td>

Details about the AWA event: -   Routing event - details of the queue that was selected.
-   Assignment event - details about which agent was selected and which eligibility pools were considered. These details include a listing of all candidate agents that were considered from each pool and a summary of which agents were filtered from consideration.
-   Rejection events - details about the user who rejected the item and the reason.
-   Manual assignments - details about the manager making the assignment, the previous and new agents, and the previous work item \(if there is one\).
-   Cancellation events - no additional details.


</td></tr><tr><td>

Summary

</td><td>

Event summary.

</td></tr></tbody>
</table>    The AWA Event form appears.


**Parent Topic:**[Using Advanced Work Assignment](../concept/using-awa.md)

**Related topics**  


[Check for an agent's presence and capacity](awa-agent-presence.md)

[Check unassigned interactions](awa-unassigned-interactions.md)

[Check unassigned task work items](awa-unassigned-task-work-items.md)

[Agent initiated SMS conversation](../concept/agent-initiated-sms-store-app.md)

[Compose an SMS conversation](compose-sms-store-app.md)

