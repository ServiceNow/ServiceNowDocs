---
title: Work item queues
description: In Advanced Work Assignment, queues store a specific type of work item for a service channel.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Work items, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Work item queues

In Advanced Work Assignment, queues store a specific type of work item for a service channel.

AWA administrators can create or modify queues based on customer need. As part of creating or modifying a queue, the awa\_admin identifies some information about the queue, including the service channel to which the queue belongs and which agent groups handle the incoming work items.

The awa\_admin can select a schedule that defines when the queue is available and identify a time limit within which an agent should accept a work item in the queue. If the selected service channel is **Chat**, the awa\_admin creates the chat messages that are displayed to users.

Routing conditions identify the work items that are routed to a queue. Create routing conditions in one of two ways:

-   Simple: use a condition builder to select routing conditions. The fields available for selection are based on the selected service channel.
-   Advanced: use a JavaScript script to identify routing conditions.

The awa\_admin can also create a queue without routing conditions so that work items are not routed to that queue automatically. Customers can manually assign work items to the queue or assign work items using assignment tools such as matching rules or Workflow Studio.

When a case in a queue is assigned manually, the case is removed from the queue. The state of the work item is set to **Canceled** and the cancellation reason is set to **Manually assigned**.

**Note:** New work items may not be assigned if they are routed to queues containing more than 10,000 work items in the queued state.

## Configure routing rules that use chat context variables

You can specify queue routing rules that use chat context variables in the condition builder. For details on creating chat context variables, see [Configure context variables for storing chat-related information](https://www.servicenow.com/docs/access?context=ac-configure-context-variables&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US). These variables can store contextual information that can be used in routing conditions to control where chat work items are routed.

For example, you can define chat context variables to store user responses from [pre-chat surveys](https://www.servicenow.com/docs/access?context=create-chat-surveys&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) that you create. If you store these responses in chat context variables, such as a user's department or a product name, you can specify the context variables in queue routing conditions to direct where the live chat is routed. When you specify a routing condition using the condition builder, you can dot walk to the Context fields. In the fields menu, select **Show Related Fields** and open the fields menu again to select **Context → Interaction Context fields**.

![Show Context related table fields in the Work item routing condition builder](../image/awa-dotwalking-context-variables.png)You can then select from the available chat context variables in the condition builder. For example, choosing **csp\_category** becomes **Context.csp\_category**.

## Assign pools of agents eligible to work on a queue

Assign one or more agent groups to a queue using the **Eligibility Assignment** related list. These groups are eligible to receive work items from the queue, which allows work to get prioritized to eligible agents.

Select an agent assignment rule and any eligibility time constraints for each group. The eligibility time constraints are used to determine when the next pool of agents is eligible for assignment. For example, you can assign one group to handle work items immediately and a second group to handle the overflow from the first group after work items sit in the queue for a specified amount of time.

**Note:** If no groups are assigned to a queue, work items can be routed to the queue but Advanced Work Assignment does not assign them.

## Create a sort order for a queue

Use the Work Item Sort Order related list to create one or more sort conditions for work items in a queue. For each sort condition, specify a field from the selected service channel table and the direction to sort, either ascending or descending. Items in the queue are sorted and assigned to agents based on these conditions.

-   **[Create a work item queue](../task/awa-create-queue.md)**  
Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.
-   **[Define agent pools eligible for assignment](../task/awa-specify-assignment-eligibility.md)**  
Specify pools of agents eligible to receive overflow work assignments for a queue. An eligible assignment pool can consist of one or more groups of agents available to work on items in the queue. This feature enables Advanced Work Assignment to find a qualified agent from a wider pool of agents.
-   **[Set work item sort order](../task/awa-set-work-sort-order.md)**  
Specify the order in which work items in a queue are sorted.
-   **[Create and manage queue triggers](../task/awa-create-queue-triggers.md)**  
Create and manage queue triggers to set off multiple actions during customer wait times for a particular queue.
-   **[External routing overview](../concept/awa-external-routing-overview.md)**  
External Routing involves routing to external queue based on the service channel and queue conditions, and then the assignment is completed by the third-party system.

**Parent Topic:**[Work items](../concept/awa-work-items.md)

