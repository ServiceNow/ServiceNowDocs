---
title: Exploring Advanced Work Assignment
description: Use Advanced Work Assignment \(AWA\) to automatically assign work items to your agents, based on their availability, capacity, and optionally, skills. AWA pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Exploring Advanced Work Assignment

Use Advanced Work Assignment \(AWA\) to automatically assign work items to your agents, based on their availability, capacity, and optionally, skills. AWA pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.

## Overview of how AWA works

Customers use different channels to request service, for example, chats, cases, or incidents. Requests from customers create task or interaction records that store information about these objects, called work items. AWA automatically routes work items to queues that focus on certain types of support using criteria \(such as priority or customer status\) that you provide.

Queues can be defined based on need or type, for example product or critical cases. You also identify the agent groups responsible for work in the queue. AWA then applies assignment rules that you set and uses agent availability, capacity, skills \(if defined\), and shifts \(if defined\) to assign work to the most qualified agent.

AWA has enterprise-grade voice resiliency that ensures call delivery to live agents even without existing interaction creation. This critical capability enables contact-center-as-a-service \(CCaaS\) providers to meet stringent SLAs directly tied to revenue recognition and billing agreements with their customers.

**Note:** Starting with the Quebec release, legacy Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Workflow

See the following diagram to learn more about the Advanced Work Assignment process flow.

![Diagram that shows the main components in Advanced Work Assignment: work items in service channels, routing work items to queues, and assigning work items to agents.](../image/awa-overview-flow.png)

Navigate to [**Advanced Work Assignment** &gt; **Home**](awa-admin-console-home.md) to start exploring AWA features.

## Benefits

Advanced Work Assignment provides the following benefits.

<table id="table_d3b_z3v_4xb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

User

</th></tr></thead><tbody><tr><td>

By automating the assignment of work tasks, AWA eliminates manual efforts involved in distributing workloads. Work items are conveniently pushed to the agent’s inbox, so that the agent can focus on doing the work, rather than looking for work.

</td><td>

[Work assignments](awa-assignment.md)

</td><td>

awa\_admin or admin

</td></tr><tr><td>

AWA helps organizations make the best use of available resources by matching the right skills and expertise with specific tasks. This leads to reduced idle time and better allocation of talent across the organization.

</td><td>

[Configure agent assignment rules](../task/awa-create-assignment-rule.md)

</td><td>

awa\_admin or admin

</td></tr><tr><td>

AWA ensures a fair and balanced distribution of work tasks among resources. It takes into consideration factors like workload, capacity, and availability to avoid overloading certain individuals while underutilizing others.

</td><td>

[Agent Inbox controls](agent-experience.md)

</td><td>

awa\_admin or admin

</td></tr></tbody>
</table>## Advanced Work Assignment components

-   **[Service channels](awa-service-channels.md)**

    A means of providing customer service. AWA offers base system channels for chats, cases, incidents, and walk-up centers. For each channel, you can set attributes such as agent capacity and utilization conditions to control the work handled in the channel.

-   **[Work items](awa-work-items.md)**

    A single piece of work handled by an agent from start to completion. For example, one chat or one case is an object that is routed and assigned to agents.

-   **[Work item queues](../reference/awa-queues.md)**

    A queue stores a specific type of work item for a service channel. AWA admins can create queues that focus on certain types of support within the channel, such as VIP customers or critical cases. AWA routes work items to queues based on specific conditions or requirements that you define, such as customer status, or region. Groups assigned to each queue handle the incoming work items. After work items are placed in a queue, AWA can then assign items to available agents based on assignment rules and agent availability and capacity.

-   **[Assignment groups](../task/awa-groups.md)**

    Agents belong to specific groups organized by the type of work assigned to them. You provide details about an assignment group including the name and description, manager, and group email. You can also set up roles, groups and group members, queues, and agent capacity overrides for agents in an assignment group.

-   **[Assignment rule](../task/awa-create-assignment-rule.md)**

    Criteria that determines how work items are pushed to the appropriate agent within a qualified assignment group.

-   **[Agent capacity](../task/awa-agent-presence.md)**

    The maximum number of work items on a particular service channel that an agent may actively work on at one time. If you want to set a maximum capacity for an agent across all service channels, define the maximum universal capacity for that agent. For information on configuring the maximum universal capacity, see [Configure an agent's maximum universal capacity](../task/awa-universal-capacity.md). Messaging Interactions in an On Hold state aren’t calculated as part of an agent's capacity.

-   **[Agent availability](../task/awa-agent-presence.md)**

    States that indicate agent presence and whether the agent is available for work or is busy or offline. AWA uses the agent availability state to determine if an agent is able to receive work.

-   **[Inbox layout](../task/awa-modify-inbox-layout.md)**

    A configuration tied to a service channel that defines which fields of a record representing a work item are shown in agent inboxes. A layout defines what the agent sees in Agent Workspace.


## Reassigning messaging conversations

If you want messaging conversations to be automatically reassigned if the current Assigned To agent on the conversation isn’t available, set the **glide.messaging.reassign.enabled** system property to `true`. The system property only affects messaging conversations and the Assigned To agent is considered not available if the AWA Inbox status isn’t set to "Available."

-   **[Advanced Work Assignment home page](awa-admin-console-home.md)**  
Explore, implement, and maintain ServiceNow® Advanced Work Assignment using a home-page experience. Discover AWA, install relevant plugins, and configure settings for AWA through the Advanced Work Assignment home page available to admins.
-   **[Service channels](awa-service-channels.md)**  
Provide customer support by automatically routing incoming work to agents through service channels.
-   **[Service channel capacity and utilization](awa-service-channel-capacity.md)**  
In Advanced Work Assignment, capacity is the number of work items automatically assigned to agents supporting a service channel. Utilization is the condition that identifies the work item states supported in the channel.
-   **[Conversational SMS service channel](conversation-sms-service-channel-store-app.md)**  
Using the Conversational SMS service channel app on the ServiceNow Store, workspace agents can provide support for long-running SMS conversations and conversations that use multiple service channels.
-   **[Work items](awa-work-items.md)**  
View Advanced Work Assignment work items using the Work Items menu options.
-   **[Work assignments](awa-assignment.md)**  
After routing work items to the appropriate queues and corresponding agent groups, Advanced Work Assignment \(AWA\) pushes work to the most qualified agent using the assignment criteria that you specify. Assignment criteria revolve around the type of assignment rule \(most capacity or last assigned\) and whether skills are defined.
-   **[External routing overview](awa-external-routing-overview.md)**  
External Routing involves routing to external queue based on the service channel and queue conditions, and then the assignment is completed by the third-party system.
-   **[Inbox layout](awa-inbox-layout.md)**  
The inbox layout determines the information shown on work item cards displayed in an agent's inbox.
-   **[Agent Inbox controls](agent-experience.md)**  
Control certain elements of the agent experience in Agent Workspace. Define the agent presence \(availability\) states and the work item rejection reasons used by agents to decline work assignments in their Agent Workspace inbox.
-   **[Advanced Work Assignment Inbox Sentiment display](awa-inbox-sentiment-display.md)**  
Surface the sentiment in AWA Inbox for agents to get the visibility of requester sentiment \( if available\) during live agent handoff or agent transfer for all channels.
-   **[Wrap up overview](wrap-up-overview.md)**  
When agents close an interaction, the wrap up feature enables them to enter closing details and wrap up codes for future reference.
-   **[Management](management.md)**  
Configure Advanced Work Assignment properties using the Management menu options.
-   **[AWA group queue priorities](awa-group-queue-priorities.md)**  
Use the group queue priority feature to set a queue or work item preference for a given group of agents. For a given group or agent with limited capacity, this feature controls which queues should be preferred if matching work items are found in both.

**Parent Topic:**[Advanced Work Assignment](awa-application-landing-page.md)

