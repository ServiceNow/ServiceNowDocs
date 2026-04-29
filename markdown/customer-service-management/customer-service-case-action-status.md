---
title: Administering case action status
description: The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Customer Service Management]
---

# Administering case action status

The case action status feature displays the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention.

The case action status feature provides visual indicators in the **Action status** column on the My Cases and My Open lists to highlight case status. In addition to the colored indicators, the **Action status** column also displays a brief status message.

![The Action status column on the Case list displays color-coded indicators and messages for cases that are blocked or need attention.](../image/case-action-status-csm-config-workspace.png "Action status column on the Case list")

## Actionable case flows

The case action status feature uses [actionable case flows](../reference/case-action-status-triggers.md) to automatically determine the action status for customer service cases. These flows create and resolve blocking tasks for different case-related actions and automatically update the action status indicators. Certain agent actions trigger these case flows, which in turn create and resolve the blocking tasks.

Customer service agents and managers can also manually set the action status for cases by enabling the **Needs Attention** field on the Case form.

## Blocking tasks

A [blocking task](../reference/case-action-status-blocking-tasks.md) is something that prevents an agent from making progress toward case resolution. For example, a case might have one or more open related case task records or be waiting for customer feedback.

Certain agent actions trigger case flows that create and resolve blocking tasks for customer service cases. These tasks determine the case action status. Additionally, there are actions that resolve these blocking tasks, such as the customer responding to an agent’s question or an internal user resolving a problem task. For more information, see .

-   **[Actionable case flows](../reference/case-action-status-triggers.md)**  
Actionable case flows contain predefined user actions that automatically create and resolve blocking tasks for customer service cases.
-   **[Blocking tasks](../reference/case-action-status-blocking-tasks.md)**  
Certain agent actions trigger case flows which create and resolve the blocking tasks for customer service cases. These tasks determine the case action status.
-   **[Case action status analytics](../reference/case-action-status-dashboard.md)**  
The Customer Service Manager dashboard displays the percentage of the case backlog that is waiting for an agent response, customer input, or a response for other users.
-   **[Case action status logging](../reference/case-action-status-logging.md)**  
Logging for the case action status feature uses a metric definition to view information about blocking tasks associated with customer service cases.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Case action status](case-action-status-csm-workspace.md)

[Configure case action status](../task/configure-case-action-status.md)

[Activate Case Action Status](../task/activate-case-action-status.md)

