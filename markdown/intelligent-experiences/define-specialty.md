---
title: Define the specialty of an AI agent
description: In the guided setup for an AI agent, write a clear description defining your agent and its role. You can also configure supported LLMs, enable third-party access, and manage long-term memory.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 4
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Define the specialty of an AI agent

In the guided setup for an AI agent, write a clear description defining your agent and its role. You can also configure supported LLMs, enable third-party access, and manage long-term memory.

## Before you begin

Role required: sn\_aia.admin

## About this task

The first step of the guided setup enables you to define the fundamentals of the AI agent. The description, AI agent role, and list of steps fields are used by the LLM to understand how to use the AI agent, by itself or as part of an agentic workflow. Descriptions, AI agent roles, and list of steps should be clear and well-defined. For guidelines for writing these fields, see [Writing effectively for agentic AI](../concept/gg-creating-aia.md). For an example AI agent, see [Example AI agent](../concept/example-aia.md).

![AI Agent Guided Setup showcasing the different stages of configuring an AI agent.](../image/create-aia-new.png)

**Note:** If you have the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) installed on your ServiceNow instance, then the AI-native experience may differ from the standard experience. If you plan to use an AI agent in the AI-native mode, make sure to test so it works as expected.

## Procedure

1.  Enter a name for the AI agent.

2.  Craft an AI agent description.

    The description should clarify the purpose of the AI agent, including its inputs, outputs, and context.

3.  Craft the AI agent role.

    The difference between the description and the agent role is that the agent role provides more detail about the function that the AI agent serves within a greater context. The greater context may be as part of an agentic workflow, or it could be the specific function it serves in another type of work process.



4.  Craft a list of steps.

    You can also use an old version of a list of steps. Select **View versions** for a full list of previous versions of the field. See [Version control](../concept/version-control.md) for more information.

5.  Determine unsupported model providers.

    You may find that some models use your AI agent better than others. If you want to avoid users from having a less optimal experience with a certain model, you can mark a model as unsupported. If an administrator changes the instance-level settings to an unsupported model, your AI agent won't be available to users.

6.  Determine if the AI agent can be accessed by third parties.

    Make your AI agent discoverable by turning on the **Allow third-party to access this AI agent** toggle button that enables you to use your ServiceNow AI agent on other platforms. You can still use it on your ServiceNow instances as well.

    See [ServiceNow agents as secondary agents](../concept/secondary-agent.md) for more information about configuring agents to use on other AI platforms.

7.  Configure long-term memory options.

    Long-term memory for AI agents enables agents to access data outside of the specific conversation or trigger that executes it. For example, you can select the **Device and Software** category to give the AI agent access to user information about the kinds of hardware devices and software that are available to the invoking user. The AI agent can remember this information in later conversations.

    -   For more information about creating LTM categories, see [Create long-term memory category](create-ltm-category.md).
    -   For more information about selecting the categories to map them to you AI agent, see [Map long-term memory category](map-ltm-aia.md).
8.  Configure AI agent learning.

    You can enable the AI agent to learn from past interactions with the user. For example, if the user encounters a similar issue, enabling this feature could help the AI agent understand what didn't work previously, so it can recommend other options.

    **Note:** When the agent learning capability is inactive at the AI Agent Studio level, the option to enable at the AI agent level is also inactive. To enable agent learning at the AI Agent Studio level, see [Set up long-term memory](long-term-memory-aia.md).


## Result

You have defined the basics of your AI agent.

## What to do next

Select **Save and continue** to move to the next step, [Add tools and information](../concept/add-tool-aia.md).

