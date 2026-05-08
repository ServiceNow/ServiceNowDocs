---
title: Move from Connect Support to Advanced Work Assignment and Agent Chat
description: Move from ServiceNow Connect Support to Agent Chat \(live chat\), which is the messaging system that agents use in Agent Workspace to interact with customers. Moving from Connect Support also involves using Advanced Work Assignment \(AWA\) to create the chat queues for routing chat work items to agents.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Get started, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Move from Connect Support to Advanced Work Assignment and Agent Chat

Move from ServiceNow® Connect Support to Agent Chat \(live chat\), which is the messaging system that agents use in Agent Workspace to interact with customers. Moving from Connect Support also involves using Advanced Work Assignment \(AWA\) to create the chat queues for routing chat work items to agents.

## Before you begin

Role required: admin

**Important:**

As of Utah, Connect Support is deprecated. For similar capabilities, please move to Advanced Work Assignment and Agent Chat.

## About this task

Moving to modern applications such as Advanced Work Assignment and Agent Chat offers features and benefits that are not available in Connect Support. These new capabilities include:

-   [Automatic assignment of chats and work items to agents](../concept/awa-assignment.md) based on criteria that you define, such as agent availability, capacity, skills, [Agent Affinity](../concept/awa-agent-affinity-concept.md), and variable [work item sizing](awa-modify-work-item-size.md).
-   Automatic [queue overflow handling](awa-specify-assignment-eligibility.md)
-   [Chat timeout reassignment](../../workspace/task/reassign-rejected-timed-out-work-items.md)
-   Native [Chat surveys](../../conversational-interfaces/concept/ci-conversational-chat-surveys.md)
-   Supervisor features, such as [Agent Whisper](../../conversational-interfaces/concept/ci-agent-whisper.md), that enable managers to join ongoing public customer chats with agents or send private messages to agents.
-   Agent features, such as workspace [inbox controls](../concept/agent-experience.md) for viewing, accepting, or rejecting incoming chats.

If you are currently using Connect Support APIs, see AWA Routing API for information on AWA APIs.

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home**.

2.  Activate the Advanced Work Assignment and Agent Chat plugins if they are not currently active.

3.  If needed, review your existing Connect Support chat queues and determine whether you want to create a similar set of queues for the Chat service channel in AWA.

    **Note:** You cannot use your Connect Support chat queues in AWA. Chat queues for Connect Support are stored in the Chat Queue \[chat\_queue\] table. Chat queues for AWA are stored in the AWA Queue \[awa\_queue\] table.

4.  In the AWA Home page, [configure the Chat service channel](awa-create-service-channel.md), [create the associated chat queues](awa-create-queue.md), and establish [agent work assignments](../concept/awa-assignment.md).

5.  In [Agent Chat settings](../../conversational-interfaces/task/ac-configure-agent-chat.md), access the Chat Setup form to specify Agent Workspace as the fulfiller interface for live chat and enable other live chat features.

6.  Activate the [chat client on your end user Service Portal](../../conversational-interfaces/task/ac-configure-bot-portal.md).


Troubleshooting suggestions include these common problems and solutions:

Problem: While using AWA, the chat remains in routing and is not offered to an available agent.

Solution: This problem may happen if AWA attempts to route the chat to a Connect Support queue. In this case, the interaction remains assigned to the Virtual Agent user and no awa\_work\_item record is created. A common cause of this problem is the Chat Setup entry for the chat’s application still being set to **Connect**.

Problem: When trying to route to a live agent, the requester is incorrectly told that no live agents are available.

Solution: This problem may be caused by one of these situations:

-   Queue conditions that depend on checking interaction fields or context were created on the interaction too late for routing.
-   Chat service channel is not associated with the Available presence state. A common cause of this problem is deactivating and reactivating the Chat channel.

Debugging suggestions include these questions to consider:

Here are a few questions to ask and places to look if agents are not receiving chats:

-   Does an awa\_work\_item record exist for the interaction? If it does not, is the **Assigned to** field for the interaction empty or is it set to Virtual Agent? If the **Assigned to** field is set to Virtual Agent, it is probably trying to use Connect Support.
-   In the Chat setup, are the fulfillers set appropriately for each application?
-   In the interaction\_json\_blob referenced by the **interaction.context\_document** field, is the *Liveagent\_application* variable set to the expected value?

