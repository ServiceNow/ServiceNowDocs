---
title: Work assignments
description: After routing work items to the appropriate queues and corresponding agent groups, Advanced Work Assignment \(AWA\) pushes work to the most qualified agent using the assignment criteria that you specify. Assignment criteria revolve around the type of assignment rule \(most capacity or last assigned\) and whether skills are defined.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Work assignments

After routing work items to the appropriate queues and corresponding agent groups, Advanced Work Assignment \(AWA\) pushes work to the most qualified agent using the assignment criteria that you specify. Assignment criteria revolve around the type of assignment rule \(most capacity or last assigned\) and whether skills are defined.

Administrators can choose to push work items to agents based on one of these assignment rules:

-   Most capacity: This option pushes work to agents that have the most capacity \(availability for work\) for a given channel. For example, suppose that two available agents, Agent 1 and Agent 2 have different capacities. Agent 1 has capacity for three chats, but Agent 2 has capacity for two chats and is currently working on one chat. AWA assigns the next work item to Agent 1 with the most capacity.
-   Last assigned: This option pushes work to the agent who has gone the longest without a work assignment in the service channel. If more than one agent has the same spare capacity in a service channel, AWA creates and assigns the next work item to the agent who has gone the longest without work in the service channel.

In addition to selecting the assignment rule, AWA admins can also determine whether:

-   Agents can reject work items.
-   Agents automatically accept chat interactions.
-   A timer is used to set a timeout period \(the length of time that an agent has to reject or accept a work item\).
-   Agent skills are to be considered during assignment.

## Assignment process

When an agent is available, AWA:

-   Checks the queue priority and gets an item from the queue with the highest priority. AWA also reviews items that have timed out or have been rejected by agents.
-   Identifies the eligible assignment pool. The eligibility assignment pool widens the group of agents who are eligible to work on an item.
-   Determines the available agents based on their presence state, the assignment rule selected \(most capacity or last assigned\), and also skills, if defined. Agents have spare capacity when they decline, transfer, or complete a work item. For example, after an agent transfers a chat, the agent has additional capacity.
-   Pushes the item to the inbox of the most qualified agent \(the timer begins\).
-   Accepts work items automatically when **Enable auto-assign work items** is selected. Agents are unable to manually **Accept** or **Reject** work items.

## Skill-based work assignment

In AWA, you can enable skill-based assignment and if needed, evaluate skill levels and make skill assignment mandatory \(required\). The basic process for setting up skills involves the following steps:

1.  Identify agents that have specific skills \(for example, a foreign language or expertise in a certain area such as network routers\), and then assign the skills to those agents using the Skills Management feature.
2.  Make the agents members of the assignment groups for the work item queues involving those skills.
3.  Create an assignment rule in AWA that enables skill handling for the specific skills.

    If you chose to select the **Evaluate skill level** option while creating the assignment rule, AWA also reviews agents' skill levels prior to assigning the work item to the most qualified agent. If multiple agents have the same number of matching skills, agents with more skills at the sufficient skill level are prioritized over agents with fewer skills at the sufficient level. For example, a chat comes through listing three skills at a high skill level. Agent A and Agent B both have the three skills. Agent A has three skills with the following skill levels: two high and one low. Agent B has three skills with the following skill levels: one high and two low. In this example, Agent A would be the first assignee of the work item because they have more skills with the sufficient skill level than Agent B. Agent B would only be assigned this work item if Agent A rejected the work.

    AWA also prioritizes the number of matching skills over the number of skills with the sufficient skill level. For example, a chat comes through listing two skills and their sufficient skill levels: Both the English skill and the Databases skill are associated with an advanced skill level. Agent 1 has both skills but only at the beginner skill level. Agent 2 has only the English skill at the sufficient advanced skill level but doesn’t have the Databases skill. In this example, the chat is routed to Agent 1 because this agent has both skills even though they aren’t at the sufficient skill level.

    If you also chose to select the **Enforce mandatory skills** option while creating the assignment rule, AWA only assigns the work item to agents that have the mandatory skills at the sufficient skill level. For example, a work item with two high-level associated mandatory skills and one optional skill is ready for assignment. Agent C has all three skills but only one of the mandatory skills at the sufficient high skill level. Agent D has only the two mandatory skills, but both skills are at the sufficient high skill level. In this example, Agent D would be the only applicable work item assignee because they are the only agent with both mandatory skills at a high enough level.

4.  Create the work item queue with a routing condition that includes the specific skill, and include the appropriate group in the eligible assignment pool.
5.  Create a scripted business rule that includes the skill in the table associated with the relevant service channel \(for example, the Case table\).

During work assignment, AWA routes and assigns work items to the Agent Workspace inbox of the most qualified agent based on the agents skills and if applicable, skill level and mandatory skill settings.

-   **[Configure agent assignment rules](../task/awa-create-assignment-rule.md)**  
Set the Advanced Work Assignment criteria for assigning work items to agents. Choose the assignment rule that considers the agent with the most capacity or the agent who has gone the longest without work. Establish the settings for the auto-assign handling, reject handling, and skill handling related lists.

**Parent Topic:**[Configuring Advanced Work Assignment](../task/installing-awa.md)

**Related topics**  


[Advanced Work Assignment home page](awa-admin-console-home.md)

[Get started with Advanced Work Assignment](../task/implement-awa.md)

[Install Conversational SMS service channel](../task/install-conversational-sms.md)

[Activate Agent Affinity](../task/awa-activate-agent-affinity.md)

[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)

[Service channels](awa-service-channels.md)

[Work items](awa-work-items.md)

[Using Agent Affinity](awa-agent-affinity-concept.md)

[Agent Inbox controls](agent-experience.md)

[Advanced Work Assignment Inbox Sentiment display](awa-inbox-sentiment-display.md)

[Management](management.md)

[AWA group queue priorities](awa-group-queue-priorities.md)

[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)

[Enable logging for Advanced Work Assignment](../task/awa-activate-logging.md)

