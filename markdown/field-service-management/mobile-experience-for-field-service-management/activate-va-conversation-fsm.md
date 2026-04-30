---
title: Activate required Virtual Agent conversation topics for Field Service Management
description: Activate Virtual Agent for Field Service Management to start chatting with the virtual agent.
locale: en-US
release: yokohama
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Virtual Agent Conversations, Setting up Field Service Mobile Agent, Configuring Field Service Management, Field Service Management]
---

# Activate required Virtual Agent conversation topics for Field Service Management

Activate Virtual Agent for Field Service Management to start chatting with the virtual agent.

## Before you begin

Role required: admin, virtual\_agent\_admin

As the administrator or Virtual Agent admin, enable chatbot conversations by enabling the following plugins:

-   Glide Virtual Agent plugin \(com.glide.cs.chatbot\).
-   Field Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\).

## About this task

The base system provides the following predefined virtual agent topics \(chatbot conversations\). To enable chatbot conversations, you must publish these topics:

-   **My Upcoming Tasks**

    Field service agents can search for upcoming work order tasks. The agent can check and update the status of existing tasks.

-   **Show Nearby Tasks**

    Field service agents can search for work order tasks that are a short distance away from the agent's current location. The agents can assign themselves to those tasks.

-   **Debrief Tasks**

    Field service agents can get information about the work order tasks that are in progress. The agents can take appropriate actions, such as entering time spent working on the task, logging incidentals, closing tasks, and creating follow-on tasks.

    You can configure the**sn\_fsm\_va.days\_in\_past\_to\_debrief\_task** system property to get information about the work in progress tasks for n number of previous days. For more information see, [Install Field Service Virtual Agent Conversations](activate-virtual-agent-fsm.md).


**Note:** If you want to customize the predefined topics provided in the base system, duplicate the topic and then modify it. For more information, see [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer** &gt; **Topics**.

2.  Click one of the required topics to open it.

3.  To use the topic, click **Publish**.

4.  Repeat this procedure for the other required topics, as many times as needed.


