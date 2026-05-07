---
title: Creating AI agents for AI Desktop Actions
description: Create an AI agent in AI Agent Studio to mimic human-like intelligence while executing desktop actions for repetitive tasks in web and desktop environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-02"
reading_time_minutes: 4
keywords: [use]
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Creating AI agents for AI Desktop Actions

Create an AI agent in AI Agent Studio to mimic human-like intelligence while executing desktop actions for repetitive tasks in web and desktop environment.

## Overview of AI agents for AI Desktop Actions

In the ServiceNow agentic ecosystem, an AI agent is a set of large language model \(LLM\) instructions and tools that can perform specific tasks. The Now Assist AI agents can perform specific tasks and functions, often using natural language instead of traditional code. For more information, see [Create an AI agent](../../../administer/now-assist-ai-agents/task/configure-next-best-action-agent.md).

AI agents process instructions, generate execution plans, and run desktop actions autonomously and semi-autonomously across legacy systems, thick client applications, and web applications lacking APIs or backend integrations. AI agents can interpret your goal and map them to one or more desktop actions via metadata \(capabilities, inputs, and outputs\).

Use AI agents to do the following tasks for your organization:

-   Generate a dynamic execution plan for desktop or web-based tasks
-   Coordinate with other AI agents to complete subtasks
-   Process human input during task execution when required
-   Collaborate with users to resolve issues that require human judgment

For adaptive desktop actions, an AI agent named **Web Automation Agent** and agentic workflow named **Web Automation** are provided by default when you install AI Desktop Actions.

1.  [Define the specialty of an AI agent](../../../administer/now-assist-ai-agents/task/define-specialty.md)

    Write a clear name and description of the AI agent, define role, and list of steps this AI agent must complete, define supported LLMs, enable third-party access, and manage long-term memory. The LLM analyzes the specific wording that you use to understand the specialty of this AI agent.

2.  Add a desktop action to an AI agent.

    Add a desktop action as a tool to the AI agent to enable desktop and web automations. Tools provide your AI agents with the capabilities necessary to complete their tasks. Providing your AI agents with the appropriate tools help with the robustness and quality of their performance. An AI agent selects a tool based on the tool’s name and description, which must be clearly written.

    -   [Add a desktop action to an AI agent](../../../administer/now-assist-ai-agents/task/add-desktop-action-ai-agent.md)
    -   [Add an adaptive desktop action tool to an AI agent for web-based tasks](create-web-actions.md)
3.  [Define security controls for an AI agent](../../../administer/now-assist-ai-agents/task/define-sec-controls-aia.md)

    Define security controls for who can access the AI agent and what data the AI agent has access to. The Define security controls step is divided into two parts:

    -   **Define user access**: Creates an ACL that determines which users can discover or invoke the AI agent.
    -   **Define data access**: Defines the data that the AI agent has access to once it’s invoked.
    Trigger conditions are not supported for AI agents that execute desktop actions. You must manually trigger these agents from the system where the AI Desktop Actions application is installed.

4.  [Select channels and status for an AI agent](../../../administer/now-assist-ai-agents/task/channels-access-aia.md)

    Activate the AI agent to use in an assistant in Now Assist for Virtual Agent and set the processing message. This AI agent can engage with users who initiate an interaction when it’s available for use in channels. Select channels where you want this AI agent to be available to engage with users.


**Related topics**  


[Defined desktop actions for desktop and web-based tasks](desktop-actions.md)

[Adaptive desktop actions for web-based tasks](web-agents-overview.md)

[Defined path desktop actions in AI Desktop Actions](desktop-actions-designer-workspace-ad.md)

