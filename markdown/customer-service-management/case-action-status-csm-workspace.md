---
title: Case action status
description: The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Case action status

The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.

![The Action status column on the Case list displays color-coded indicators and messages for cases that are blocked or need attention.](../image/case-action-status-csm-config-workspace.png "Action status column on the Case list")

## Action status column

The case action status feature provides visual indicators in the **Action status** column on the My Cases and My Open lists to highlight case status. In addition to the colored indicators, the **Action status** column also displays a brief status message.

<table id="table_u1t_cqp_nhc"><thead><tr><th>

Indicator

</th><th>

Status message

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blue

</td><td>

Needs attention

</td><td>

A blue indicator highlights cases that need attention, such as cases that have been updated by customers or internal users and are waiting for input or review.

</td></tr><tr><td>

Red

</td><td>

-   Blocked internally
-   Blocked by customer
-   Blocked internally and by customer

</td><td>

A red indicator highlights cases that are blocked, such as cases that have open related task records or are waiting for customer feedback.

</td></tr></tbody>
</table>## Actionable case flows

The case action status feature uses actionable case flows to automatically determine the action status for customer service cases. These flows create and resolve blocking tasks for different case-related actions and update the action status indicators. Certain agent actions trigger these case flows, which in turn create and resolve the blocking tasks. Customer service agents and managers can also manually set the action status for cases by enabling the **Needs Attention** field on the Case form.

For more information, see the following topics:

-   [Actionable case flows](../reference/case-action-status-triggers.md)
-   [Configure actionable case flows](../task/configure-case-action-status-flows.md)

## Blocking tasks

A blocking task is something that prevents an agent from making progress toward case resolution. For example, a case might have one or more open related case task records or be waiting for customer feedback.

Certain agent actions trigger case flows that create and resolve blocking tasks for customer service cases. These tasks determine the case action status. Additionally, there are actions that resolve these blocking tasks, such as the customer responding to an agent’s question or an internal user resolving a problem task. For more information, see [Blocking tasks](../reference/case-action-status-blocking-tasks.md).

## Blocked by related list

The case action status feature adds the **Blocked by** related list to the workspace view of the Case form. Blocking tasks for a case appear in this list. When the system adds a blocking task to a case, it also adds one of the following blocking reasons:

-   Need information from the customer
-   Need task resolution
-   Need PRB workaround
-   Other

**Note:** When a problem is associated with a case, the blocking reason is set to **Needs task resolution**. The agent can update this reason to **Need PRB workaround** if necessary.

When a blocking task is resolved:

-   The **Unblocked By** field displays the user who performed the unblocking action.
-   The **Unblocked On** field displays the date that the blocking task was resolved.
-   The **Needs Attention** field for the case is enabled.

## Notifications

Agents can receive notifications on their preferred channel when a blocking task for an assigned case is resolved. Agents can also receive notifications when the **Needs Attention** field for an assigned case is enabled.

**Note:** Notifications are not sent to the user who updated the record.

Users with the admin role can configure notification triggers by navigating to **Agent Workspace** &gt; **Notification Triggers** &gt; **Case Action Status Trigger**.

**Related topics**  


[Configure case action status](../task/configure-case-action-status.md)

[Administering case action status](customer-service-case-action-status.md)

