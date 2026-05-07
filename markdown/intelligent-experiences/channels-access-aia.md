---
title: Select channels and status for an AI agent
description: In the guided setup for an AI agent, activate the AI agent to use in an assistant in Now Assist for Virtual Agent, and set the processing messages.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Select channels and status for an AI agent

In the guided setup for an AI agent, activate the AI agent to use in an assistant in Now Assist for Virtual Agent, and set the processing messages.

## Before you begin

Role required: sn\_aia.admin

## About this task

The final step of the AI agent guided setup includes options for where you can invoke the agentic workflow as well as set the processing message. You must select which assistants for Now Assist in Virtual Agent you want to be able to invoke the AI agent. Your processing messages appear when the AI agent is running and when the AI agent's task is completed.

## Procedure

1.  Select whether you want users to use Now Assist in Virtual Agent to invoke the AI agent.

    If enabled, you must select which chat assistants have access to the AI agent. You can edit assistants using Assistant Designer.

2.  Set the processing and completion messages for your AI agent.

    You can set a processing message, completion message, or both. If you don't want to use a specific type of message, unselect the toggle next to the message field.

    You can also use Now Assist to generate the messages for you by selecting **Generate messages**. You can change the messages after they're generated.

    ![Select channels and access page](../image/select-aia-channels.png)

3.  Activate the AI agent.

    Select the **This AI agent is active** toggle to activate the AI agent only when you want users to be able to use it. If you want to test your AI agent first, wait until after you have tested it before activating it. You can return to the guided setup later.

    If you don't see this option, you may need to scroll.

    ![Select channels and access page.](../image/aia-channels-activation.png)

    **Note:** If you have installed the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) on your ServiceNow AI Agent Studio instance, then agent learning and voice agents won't work if the assistant is in Premium Chat mode.

4.  Select **Save and test**.


## Result

You have completed the guided setup for creating an AI agent. Your new AI agent can be edited at any time using AI Agent Studio.

## What to do next

Move to the **Testing** playground to [test an AI agent execution](test-ai-agent.md) using example utterances or to [test user access](test-aia-access.md).

