---
title: Case action status overview
description: Use the case action status feature to indicate the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention and quickly prioritize their work.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-12-16"
reading_time_minutes: 1
breadcrumb: [Administer Customer Service Management, Customer Service Management]
---

# Case action status overview

Use the case action status feature to indicate the status of cases in the Case list. With this feature, customer service agents can easily identify cases that need attention and quickly prioritize their work.

Visual indicators in the **Action Status** column on the Case list highlight case status:

-   A blue indicator highlights cases that need attention, such as cases that have been updated by customers or internal users and are waiting for input or review.
-   A red indicator highlights cases that are blocked, such as cases that have open related task records or are waiting for customer feedback. Blocked cases can have the following status:
    -   Blocked internally
    -   Blocked by customer
    -   Blocked internally and by customer

![The action status column on the Case list displays color-coded indicators and messages for cases that are blocked or need attention.](../image/case-action-status-csm-config-workspace.png "Action status column on the Case list")

In addition to the colored indicators, the **Action Status** column also displays a brief status message.

The case action status feature uses actionable case flows to automatically determine the action status for customer service cases. These flows create and resolve blocking tasks for different case-related actions and update the action status indicators. Certain agent actions trigger these case flows, which in turn create and resolve the blocking tasks.

Customer service agents and managers can also manually set the action status for cases by enabling the **Needs Attention** field on the Case form.

-   **[Actionable case flows](../reference/case-action-status-triggers.md)**  
Actionable case flows contain predefined user actions that automatically create and resolve blocking tasks for customer service cases.
-   **[Blocking tasks](../reference/case-action-status-blocking-tasks.md)**  
Certain agent actions trigger case flows which create and resolve blocking tasks for customer service cases. These tasks determine the case action status.
-   **[Case action status analytics](../reference/case-action-status-dashboard.md)**  
The Customer Service Manager dashboard displays the percentage of the case backlog that is waiting for an agent response, customer input, or a response for other users.
-   **[Case action status logging](../reference/case-action-status-logging.md)**  
Logging for the case action status feature uses a metric definition to view information about blocking tasks associated with customer service cases.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Activate Case Action Status](../task/activate-case-action-status.md)

