---
title: Advanced Work Assignment \(AWA\) for HR Service Delivery Agent Workspace overview
description: Use the ServiceNow Advanced Work Assignment \(AWA\) for HR Service Delivery Agent Workspace to automatically assign a work item to agents based on their availability, capacity, and skills.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Setting up HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Advanced Work Assignment \(AWA\) for HR Service Delivery Agent Workspace overview

Use the ServiceNow Advanced Work Assignment \(AWA\) for HR Service Delivery Agent Workspace to automatically assign a work item to agents based on their availability, capacity, and skills.

## Plugins

Activate the Advanced Work Assignment for HRSD \[com.sn\_hr\_awa\] plugin if you have the HR admin role. Activating this plugin also activates:

-   Advanced Work Assignment \[com.glide.awa\]

    When activated, the Advanced Work Assignment for HRSD \[com.sn\_hr\_awa\] plugin supports the AWA routing with historical affinity for chat and cases when the Advanced Work Assignment - Agent Affinity \[com.glide.awa.agent\_affinity\] plugin is activated.

-   Agent Chat \[com.glide.interaction.awa\]
-   Human Resources Scoped App: Core \[com.sn\_hr\_core\]

You can also activate:

-   Skills Management \[com.snc.skills\_management\]
    -   Activated by default when the Human Resources Core \[com.sn\_hr\_core\] plugin is activated.
    -   Only activate when you are using skill determination rules to map a skill to an HR case.
-   Skill Determination \[com.snc.skill\_determination\]

    Activate when using skill determination rules. .

-   Interactions Management \[com.glide.interaction\]
-   Human Resources Scoped App: Virtual Agent Conversations \[com.sn\_hr\_virtual\_agent\]

    Only activate when using Virtual Agent. For more information, see [Virtual Agent for HR Service Delivery](hr-virtual-agent-conversations.md#).


## Chat setup

Ensure the **HR Fulfiller UI** field is set to **Agent Workspace**. For more information, see [Configure Agent Chat for HR Service Delivery Agent Workspace](../task/configure-awa-hr.md).

## HR case

AWA is an alternative to using:

-   HR templates \(based on the HR service\)
-   HR assignment rules
-   HR matching rules

AWA automatically routes HR cases, chats, or interactions based on:

-   Availability
-   Capacity
-   Capacity and Skills

AWA pushes cases to qualified HR agents using work item queues, routing conditions, and assignment criteria that you define. HR agents see their assignments in their inbox. You can set the capacity for an agent, which is the number of work items on a particular service channel that an agent may actively work on. You can set assignment rules to determine how AWA routes work items to a group of agents. If an agent rejects a work item, the item is rerouted to another agent.

For more information, see [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Note:** To use AWA, you must ensure your:

-   HR templates do not identify assignment groups or skills.
-   Deactivate your existing HR Assignment Rules and HR Matching Rules.

Agent Inbox:

Using AWA you can automatically assign an HR case and have it appear in an agent's inbox.

For more information, see [Agent Inbox controls](https://www.servicenow.com/docs/access?context=agent-experience&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). The inbox layouts determine what appears on work item cards in an agent's inbox. For more information, see [Inbox layout](https://www.servicenow.com/docs/access?context=awa-inbox-layout&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Skill Determination Rules

Use Skill Determination Rules as an alternative way to map skills to an HR case.

The base system provides a skill determination rule for each COE and is inactive by default.

There is also a skill determination rule for interactions:

Skill determination rules for Interactions \[Human Resources\]. Defines what skills are required in chat and when creating an interaction. The script defines the mappings. By default, this skill determination rule is inactive.

## Service channels

Service channels help assign specific types of chats or HR cases to the correct agents. For more information, see [Service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

There are two service channels provided with the base system:

-   Chat
-   HR Case

Each service channel has eight \(8\) queues.

-   Each queue corresponds to a COE and HR table.
-   HR cases route to a corresponding queue.
-   Each queue defines an assignment group.
-   AWA logic reviews the assignment group and routes to the appropriate agent.

AWA uses service channels to organize incoming requests from chats, cases, and incidents. AWA routes these work items to specific queues. For more information about AWA, see Agent Workspace Advanced Work Assignment \(AWA\).

## Business rules

There are three \(3\) business rules. Activate only one:

-   Skill determination for HR Cases

    Use this business rule when you are using skill determination rules to map a skill to an HR case.

-   Copy skills to task\_m2m\_skill table

    Use this business rule when you are using HR templates to map a skill to an HR case.

    **Note:** These business rules make entries in the Task Skill \[task\_m2m\_skill\] table. AWA uses this table to determine final mapping between a task and a skill.

-   Skill determination for Interaction\[HR\]
    -   Only activate this business rule when using chat assignment by skill.
    -   Works with the Skill determination rules for interactions \[Human Resources\] to populate the Interaction Skill \[interaction\_m2m\_skill\] table.
    -   AWA uses this table to check the mapping between interaction and skill.
    -   Interaction records are automatically created when an employee initiates a chat.

## AWA Assignment Rules

The base system provides two \(2\) AWA assignment rules. For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   Capacity based assignment for HR work items assignment rule

    Considers agents with the greatest availability for handling the work.

-   Capacity and skill-based assignment for HR work items assignment rule
    -   Considers agents with the greatest availability and their assigned skills for handling the work. Assigned skills can optionally be made mandatory.
    -   When skills are considered mandatory, only considers routing work items to agents that have the skills.

        **Note:** When agents with the correct skills are not available or their capacity is full, it does not route to other agents but will wait until one is available.


## Workspace Agent Chat

Workspace Agent Chat is the real-time messaging system you use in HR Service Delivery Agent Workspace.

Similar to HR case, there is a service channel for chat with eight \(8\) queues.

## Virtual Agent

When Virtual Agent is active, the chat window shows Virtual Agent topics. Under the Chat service channel under AWA, there is a script that maps the additional Virtual Agent topics to the queue.

When Virtual Agent is not active, the chat window shows the Employee Service Center \(ESC\) pre-chat categories. Under the Chat service channel under AWA, there is a script that maps the additional Virtual Agent topics to the queue.

**Note:** You can distinguish the queues by the ESC pre-chat categories and Virtual Agent topics.

For more information, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

If you are migrating from Connect Support, use AWA to create the chat queues for routing chat work items to agents and the Chat Setup form to configure Agent Chat. For more information, see [Migrate from Connect Support to Advanced Work Assignment and Agent Chat](https://www.servicenow.com/docs/access?context=migrate-from-connect-support&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

For more information on Workspace Agent Chat, see Workspace Agent Chat.

