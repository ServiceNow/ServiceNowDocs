---
title: Define the expected behavior an agentic workflow
description: In the guided setup for an agentic workflow, write a clear description defining your agentic workflow and the instructions it should perform to orchestrate AI agents and accomplish complex tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/define-aw-new.html
release: australia
topic_type: task
last_updated: "2026-06-06"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, AI Agent Studio, Enable AI experiences]
---

# Define the expected behavior an agentic workflow

In the guided setup for an agentic workflow, write a clear description defining your agentic workflow and the instructions it should perform to orchestrate AI agents and accomplish complex tasks.

## Before you begin

You must either create an agentic workflow or edit an existing one to get to this step in the guided setup. To learn how to get started creating an agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-aw-new.md). Otherwise, navigate to the AI Agent Studio and select the agentic workflow you want to define to enter the guided setup.

These fields may be blank or be filled in for you as a first draft as part of the new AI Agent Studio setup process.

Role required: sn\_aia.admin

## About this task

The first step of the guided setup enables you to define the fundamentals of the agentic workflow. The description and instructions fields are used by the AI agent Orchestrator to understand how to use the agentic workflow and coordinate its AI agents. Descriptions and instructions should be clear and well-defined. For guidelines for writing these fields, see [Writing effectively for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-creating-aia.md). For an example agentic workflow, see [Example agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/example-aw.md).

## Procedure

1.  Verify or create the name and description of the agentic workflow for the LLM that summarize the main intention of the agentic workflow.

    If the name and description aren't clear or correct, the Orchestrator won't know how to use the agentic workflow in context.

    \[Omitted image "aw-setup-exp-beh-1.png"\] Alt text: Agentic workflow setup expected behavior section showing name and description for LLM discovery

2.  Review and refine the **How-to instructions**.

    The instructions are the most important element of the agentic workflow. They tell the Orchestrator what the workflow accomplishes and how it will coordinate AI agents to perform complex tasks.

    You can create different versions of the agentic workflow instructions. After [testing an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) or [evaluating an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md), you can adjust the instructions and compare their performance. See [Version control for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/version-control.md) to learn more.

    \[Omitted image "ai-agent-setup-exp-beh-2.png"\] Alt text: AI agent setup expected behavior section showing how-to instructions with version control.


## Result

The fundamentals of your agentic workflow are defined so that the AI agent Orchestrator can use it.

## What to do next

Scroll down to the next section of the guided setup, **AI Agents**, to [add AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-aia-aw-new.md) to your agentic workflow.

