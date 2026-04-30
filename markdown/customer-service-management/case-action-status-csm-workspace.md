---
title: Case action status
description: Customer service agents can use the case action status feature in CSM Configurable Workspace to easily identify cases that need attention.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-05-14"
reading_time_minutes: 2
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case action status

Customer service agents can use the case action status feature in CSM Configurable Workspace to easily identify cases that need attention.

## Action Status column

This feature enables customer service agents to easily identify cases that need attention and quickly prioritize their work. Visual indicators in the **Action Status** column on the My Cases and My Open lists highlight case status:

-   A blue indicator highlights cases that need attention, such as cases that have been updated by customers or internal users and are waiting for input or review.
-   A red indicator highlights cases that are blocked, such as cases that have open related task records or are waiting for customer feedback. Blocked cases can have the following status:
    -   Blocked internally
    -   Blocked by customer
    -   Blocked internally and by customer

![The action status column on the Case list displays color-coded indicators and messages for cases that are blocked or need attention.](../image/case-action-status-csm-config-workspace.png "Action status column on the Case list")

In addition to the colored indicators, the **Action Status** column also displays a brief status message.

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


[Case action status overview](customer-service-case-action-status.md)

