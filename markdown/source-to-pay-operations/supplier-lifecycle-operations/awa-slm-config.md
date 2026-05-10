---
title: Setting up Advanced Work Assignment for Supplier Lifecycle Operations
description: Plan and configure your implementation of Advanced Work Assignment for Supplier Lifecycle Operations.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Work Assignment for Supplier Lifecycle Operations, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Setting up Advanced Work Assignment for Supplier Lifecycle Operations

Plan and configure your implementation of Advanced Work Assignment for Supplier Lifecycle Operations.

Setting up [Advanced Work Assignment for Supplier Lifecycle Operations](slo-glossary.md#) involves configuring the following components:

-   Service channels: A means of providing customer service. Advanced Work Assignment offers base system channels for chats, cases, incidents, and walk-up centers. For each channel, you can set attributes such as agent capacity and utilization conditions to control the work handled in the channel.
-   Work item: A single piece of work handled by an agent from start to completion.
-   Work item queue: A queue that stores a specific type of work item for a service channel.
-   Assignment groups: Agents belong to specific groups organized by the type of work assigned to them.
-   Assignment rules: Criteria that determine how work items are pushed to the appropriate agent within a qualified assignment group.
-   Agent capacity: The maximum number of work items on a particular service channel that an agent may actively work on at one time. If you want to set a maximum capacity for an agent across all service channels, define the maximum universal capacity for that agent.
-   Agent availability: States that indicate agent presence and whether the agent is available for work or is busy or offline. Advanced Work Assignment uses the agent availability state to determine if an agent is able to receive work.
-   Inbox layout: A configuration tied to a service channel that defines which fields of a record representing a work item are shown in agent inboxes. A layout defines what the agent sees in the Source-to-Pay Workspace.

For more information, see [Exploring Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md).

-   **[Configure Advanced Work Assignment for Supplier Lifecycle Operations](../task/setup-awa-slm.md)**  
Configure various components, such as service channels, work item queues, and assignment rules that determine how a chat interaction should be routed to an agent.
-   **[Configure the Supplier Collaboration Queue](../task/configure-scp-queue.md)**  
Configure the Supplier Collaboration Queue chat queue to ensure that the chat requests are routed and assigned to specific agents that belong to a defined group.
-   **[Configure Agent Chat for Source-to-Pay Workspace](../task/configure-agent-chat-slm.md)**  
Use Agent Chat Settings to configure Agent Chat for Source-to-Pay Workspace.

**Parent Topic:**[Advanced Work Assignment for Supplier Lifecycle Operations](supplier-awa.md)

**Related topics**  


[Source-to-Pay Workspace agent inbox](agent-inbox-ws.md)

[Activate Agent Chat and load demo data](../task/load-demo-agent-chat.md)

[Using Advanced Work Assignment for Supplier Lifecycle Operations](use-awa-slm.md)

[Configure Advanced Work Assignment for Supplier Lifecycle Operations](../task/setup-awa-slm.md)

[Configure the Supplier Collaboration Queue](../task/configure-scp-queue.md)

[Configure Agent Chat for Source-to-Pay Workspace](../task/configure-agent-chat-slm.md)

