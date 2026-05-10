---
title: Order routing based on priority using Advanced Work Assignment
description: AWA can be used to automatically route customer orders based on priority to specific agent categories.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Calculating the order priority, Configuring order priority and routing, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Order routing based on priority using Advanced Work Assignment

AWA can be used to automatically route customer orders based on priority to specific agent categories.

Use AWA to automatically assign work items \(order tasks\) to your agents based on their availability, capacity, and skills. AWA pushes work to qualified agents using work item queues, routing conditions, and assignment criteria. Agents can view their assignments in their Agent Workspace inbox. The following diagram shows how AWA routes different types of orders to different fulfillment agents.

**Note:** All fulfillment agents must have the AWA agent \(awa\_agent\) role.

![Infographic displaying the routing orders process using AWA. For the image description, refer to the text that follows.](../../tmt-order-mgt/image/order-mgt-awa.png)

The following configurations are required for AWA:

-   Service channel: It is a means of assigning a specific type and scope of work to agents. The Order Service Channel is available with the base system for order tasks. The Order Service Channel is in a disabled state by default and must be manually activated.
-   Agent presence state: Availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox. The default presence states are Available, Away, and Offline. After the Order Service Channel is enabled, the Available presence state value shows the Order Service channel the customer has to move the order service channel to the selected list to receive the work.
-   Queue: A queue stores a specific type of work item for a service channel. AWA admins can create queues that focus on certain types of support in the channel, such as VIP customers or critical cases. AWA routes work items to queues based on specific conditions or requirements that you define, such as customer status, or region. Groups assigned to each queue handle the incoming work items. Once work items are placed in a queue, AWA can then assign items to available agents based on assignment rules and agent availability and capacity. Demo queues that can be used as a reference are available with the base system.
-   Assignment rule: Criteria that determines how work items are pushed to the appropriate agent in a qualified assignment group. A demo assignment rule that can be used as a reference is available with the base system.
-   Agent capacity: The maximum number of work items on a particular service channel that an agent may actively work on at one time.
-   Agent availability: States that indicate agent presence and whether the agent is available for work or is busy or offline. AWA uses the agent availability state to determine if an agent is able to receive work.
-   Inbox layout: A configuration tied to a service channel that defines which fields of a record representing a work item are shown in agent inboxes. A layout defines what the agent sees in Agent Workspace. The Default Order Layout is available with the base system and can be used as a reference to create a new layout.

For more details, see [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md)

