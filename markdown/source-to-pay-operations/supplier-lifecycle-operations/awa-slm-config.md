---
title: Setting up Advanced Work Assignment for Supplier Lifecycle Operations
description: Plan and configure your implementation of Advanced Work Assignment for Supplier Lifecycle Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplier-lifecycle-operations/awa-slm-config.html
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced Work Assignment for Supplier Lifecycle Operations, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Setting up Advanced Work Assignment for Supplier Lifecycle Operations

Plan and configure your implementation of Advanced Work Assignment for Supplier Lifecycle Operations.

Setting up [Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/slo-glossary.md) involves configuring the following components:

-   Service channels: A means of providing customer service. Advanced Work Assignment offers base system channels for chats, cases, incidents, and walk-up centers. For each channel, you can set attributes such as agent capacity and utilization conditions to control the work handled in the channel.
-   Work item: A single piece of work handled by an agent from start to completion.
-   Work item queue: A queue that stores a specific type of work item for a service channel.
-   Assignment groups: Agents belong to specific groups organized by the type of work assigned to them.
-   Assignment rules: Criteria that determine how work items are pushed to the appropriate agent within a qualified assignment group.
-   Agent capacity: The maximum number of work items on a particular service channel that an agent may actively work on at one time. If you want to set a maximum capacity for an agent across all service channels, define the maximum universal capacity for that agent.
-   Agent availability: States that indicate agent presence and whether the agent is available for work or is busy or offline. Advanced Work Assignment uses the agent availability state to determine if an agent is able to receive work.
-   Inbox layout: A configuration tied to a service channel that defines which fields of a record representing a work item are shown in agent inboxes. A layout defines what the agent sees in the Source-to-Pay Workspace.

For more information, see [Exploring Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/awa-overview.md).

-   **[Configure Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/setup-awa-slm.md)**  
Configure various components, such as service channels, work item queues, and assignment rules that determine how a chat interaction should be routed to an agent.
-   **[Configure the Supplier Collaboration Queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/configure-scp-queue.md)**  
Configure Supplier Collaboration Queue to route and assign supplier portal chat requests in a defined group via AWA.
-   **[Configure Agent Chat for Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/configure-agent-chat-slm.md)**  
Use Agent Chat Settings to configure Agent Chat for Source-to-Pay Workspace.

**Parent Topic:**[Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/supplier-awa.md)

**Related topics**  


[Source-to-Pay Workspace agent inbox]()

[Activate Agent Chat and load demo data]()

[Using Advanced Work Assignment for Supplier Lifecycle Operations]()

[Configure Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/setup-awa-slm.md)

[Configure the Supplier Collaboration Queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/configure-scp-queue.md)

[Configure Agent Chat for Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/configure-agent-chat-slm.md)

[Using Advanced Work Assignment for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/use-awa-slm.md)

