---
title: Create an AI agent
description: Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents while executing the agentic workflows.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 3
keywords: [Agentic AI, ACLs in AI agents]
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Create an AI agent

Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents while executing the agentic workflows.

## Before you begin

Role required: sn\_aia.admin

## About this task

In the ServiceNow agentic ecosystem, an AI agent is a set of large language model \(LLM\) instructions and tools that can perform specific tasks.

An AI agent can collaborate with other agents to achieve better results by using fewer LLM calls. AI agents can also reach out to the user if they need any help or information.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  From the **Add** drop-down menu, select one of the following agent creation options:**Chat** or **External**.

    1.  **Chat**: Select the Chat option to create AI agents in the AI Agent Studio to connect with internal AI agents within the ServiceNow AI Platform to execute agentic workflows.

        The following instructions are for Chat AI agents. See the following links for guides to create other types of AI agents.

    2.  **Voice**: Select the Voice option to create an AI voice agent.

        See [Deploy AI agents for voice](../reference/deploy-ai-agents-for-voice.md) for more information on setting up and creating AI voice agents.

    3.  **External**: Select the External option to create external AI agents in the AI Agent Studio to connect the ServiceNow AI Platform with the third-party agentic AI providers.

        For more information about creating external AI agents in the AI Agent Studio, see [Create an external AI agent](../concept/create-external-aia.md).

3.  [Define the AI agent's specialty](define-specialty.md).

4.  [Define the AI agent security controls](define-sec-controls-aia.md).

5.  [Add a trigger to automatically invoke your AI agent if a specified event occurs.](add-trigger-aia.md).

    If you want your AI agent to be used only in chats, you don’t need to add a trigger.

6.  [Determine the chat assistants to access your AI agent, set the processing messages, and activate your AI agent.](channels-access-aia.md).

7.  Select **Save and test** to complete the configuration steps or review a previous step by selecting **Back**.

    Selecting Save and test leads you to the AI agent testing page, where you can test the AI agent that you created. For more information, see [Manually test the execution of an AI agent](test-ai-agent.md).

    To test the AI agent, you must have the sn\_aia.admin role and any roles the ACLs configured for the AI agent and its tools require, if applicable.


## Result

You can see the AI agent that you created in the **Manage agentic workflows and AI agents** page.

If you selected **Users with specific roles** for your ACL, you can change roles at any point. Return to the guided setup and double-click the pills to make changes. All other security changes must be done on the ACL \[sys\_security\_acl\] table by a user with elevated permissions.

