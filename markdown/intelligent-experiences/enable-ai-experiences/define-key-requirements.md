---
title: Define key requirements for an agentic workflow
description: In the guided setup for an agentic workflow, write a clear description of what the agentic workflow is, add AI agents, and select unsupported AI model providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/define-key-requirements.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Define key requirements for an agentic workflow

In the guided setup for an agentic workflow, write a clear description of what the agentic workflow is, add AI agents, and select unsupported AI model providers.

## Before you begin

Role required: sn\_aia.admin

## About this task

The first step of the guided setup includes defining the fundamentals of the agentic workflow. The description and list of steps fields are used by the large language model \(LLM\) to achieve its objectives. Descriptions and list of steps should be clear and well-defined. For guidelines for writing these fields, see [Writing effectively for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/gg-creating-aia.md). For an example agentic workflow, see an [example agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/example-aw.md).

You also assign the AI agents that the agentic workflow has access to in this step. The AI agents should be clearly defined and referred to in your list of steps so that the LLM knows how to use them. You can use existing AI agents installed with Now Assist applications or create your own. See [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/configure-next-best-action-agent.md) for the steps to create your own custom AI agents.

## Procedure

1.  Enter a name for the workflow.

2.  Craft a workflow description.

3.  Craft a list of steps.

    You can also use an old version of a list of steps. Select **View versions** for a full list of previous versions of the field. See [Version control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/version-control.md) for more information.

    \[Omitted image "def-key-reqs-1.png"\] Alt text: Name, description, and list of steps for Generate Resolution Plans

4.  Add AI agents to perform the tasks described in the list of steps.

    You can use Now Assist to generate a list of AI agents for you.

5.  Determine unsupported model providers.

    You may find that some models use your AI agent better than others. If you want to avoid users from having a less optimal experience with a certain model, you can mark a model as unsupported. If an administrator changes the instance-level settings to an unsupported model, your AI agent isn't available to users.

    \[Omitted image "def-key-reqs-2.png"\] Alt text: Add AI agents and determine unsupported models for Generate Resolution Plans


## Result

You have written instructions for the LLM to determine how to use the agentic workflow, assigned AI agents, and determined LLM provider support.

## What to do next

Select **Save and continue** to move to the next step, [Define security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

