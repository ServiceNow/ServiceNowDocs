---
title: Define the expected behavior of an AI agent
description: In the guided setup for an AI agent, write a clear description defining your AI agent, its role, and the instructions it should perform to accomplish tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/define-aia-new.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 3
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Define the expected behavior of an AI agent

In the guided setup for an AI agent, write a clear description defining your AI agent, its role, and the instructions it should perform to accomplish tasks.

## Before you begin

You must either create an AI agent or edit an existing one to get to this step in the guided step. To learn how to get started creating an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-aia-new.md). Otherwise, navigate to the AI Agent Studio and select the AI agent you want to define to enter the guided setup.

The name, description, modality, AI agent role, and instructions are all required. If the agent was drafted in a conversation, or created from an opportunity, these fields are pre-filled as a first draft. Treat pre-filled content as generated text to be reviewed, not as confirmed configuration.

Role required: sn\_aia.admin

## About this task

The first step of the guided setup enables you to define the fundamentals of the AI agent. The description, AI agent role, and instructions fields are used by the AI agent Orchestrator to understand how to use the AI agent, by itself or as part of an agentic workflow. Descriptions, AI agent roles, and instructions should be clear and well-defined. For guidelines for writing these fields, see [Writing effectively for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-creating-aia.md). For an example AI agent, see [Example AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/example-aia.md).

## Procedure

1.  Verify the name and description summarize the main intention of the AI agent.

    If the name and description aren't clear or correct, the Orchestrator won't know how to wield the AI agent in context.

2.  Check that the modality of the AI agent is correct.

    The **Chat** modality allows users to invoke the AI agent in Virtual Agent or as part of an agentic workflow in the ServiceNow Otto panel.

    An agent has one modality. Chat and Voice cannot both be applied to the same agent. If you need both channels, build one agent per modality. Selecting **Voice** also requires that a voice assistant already exists in Assistant Designer.

    See [Create an AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a-voice-enabled-ai-agent.md) for more information about creating AI agents with the **Voice** modality.

    \[Omitted image "ai-agent-setup-exp-beh-1.png"\] Alt text: AI agent setup definitions section showing name, description, and modality.

3.  Review and refine instructions.

    The instructions are the most important element of the AI agent. While the name and description guide the AI agent Orchestrator to know when to invoke an AI agent, the instructions tell the Orchestrator what it does and how it will do tasks.

    You can create different versions of the AI agent instructions. After [testing an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) or [evaluating an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md), you can adjust the instructions and compare their performance. See [Version control for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/version-control.md) to learn more.

4.  Confirm the AI agent's expertise.

    The difference between the description and the agent role is that the agent role provides more detail about the function that the AI agent serves within a greater context. The greater context may be as part of an agentic workflow, or it could be the specific function it serves in another type of work process.

    \[Omitted image "ai-agent-setup-exp-beh-2.png"\] Alt text: AI agent setup definitions section how-to instructions with version control and AI agent's expertise.


## Result

The fundamentals of your AI agent are defined so that the AI agent Orchestrator can use it.

## What to do next

Scroll down to the next section of the guided setup, **Tools**, to [add tools and information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia-new.md) your AI agent can use.

