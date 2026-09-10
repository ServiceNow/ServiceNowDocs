---
title: Creating AI agents and adding desktop action tool
description: Create an AI agent and add desktop action tool in AI Agent Studio to mimic human-like intelligence while executing desktop actions for repetitive tasks in web and desktop environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-ai-agents-ad.html
release: australia
topic_type: concept
last_updated: "2025-11-02"
reading_time_minutes: 4
keywords: [use]
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Creating AI agents and adding desktop action tool

Create an AI agent and add desktop action tool in AI Agent Studio to mimic human-like intelligence while executing desktop actions for repetitive tasks in web and desktop environment.

## AI agent and agentic workflow for AI Desktop Actions

In the ServiceNow agentic ecosystem, an AI agent is a set of large language model \(LLM\) instructions and tools that can perform specific tasks. The AI agents can perform specific tasks and functions, often using natural language instead of traditional code. For more information creating AI agents, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-aia-new.md).

AI agents process instructions, generate execution plans, and run desktop actions autonomously and semi-autonomously across legacy systems, thick client applications, and web applications lacking APIs or backend integrations. AI agents can interpret your goal and map them to one or more desktop actions via metadata \(capabilities, inputs, and outputs\).

Use AI agents to do the following tasks for your organization:

-   Generate a dynamic execution plan for desktop or web-based tasks
-   Coordinate with other AI agents to complete subtasks
-   Process human input during task execution when required
-   Collaborate with users to resolve issues that require human judgment

Trigger conditions aren't supported for AI agents that execute desktop actions. You must manually trigger these agents from the system where the AI Desktop Actions application is installed.

For adaptive desktop actions, an AI agent named **Web Automation Agent** and agentic workflow named **Web Automation** are provided by default when you install AI Desktop Actions. You can create a different agentic workflow referencing this AI agent or AI agent that you created. For more information about creating agentic workflows, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-aw-new.md).

## Desktop action tool for an AI agent

Desktop actions are tools that AI agents use to interact with web and desktop applications. An AI agent uses a desktop action to automate tasks in desktop-based or web-based applications on the end user's system. You can create a desktop action or add an existing one as a tool to your AI agent. For more information about adding desktop action tools, see [Add a desktop action tool to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-desktop-action-new.md).

There are two types of desktop actions.

-   **Defined desktop action**

    Created in the AI Desktop Actions client application on the Windows machine, then added as a tool to an AI agent.

-   **Adaptive desktop action**

    Configured in AI Agent Studio during AI agent tool configuration. There are two ways the adaptive desktop actions run:

    -   **Desktop applications**: AI agents run these desktop actions in the AI Desktop Actions client application on the macOS machine. For more information, see [Adaptive desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md).

        **Warning:** This is a beta feature in this release. Functionality, behavior, and execution logic may change in subsequent releases. Test these desktop actions thoroughly in a test environment before deploying to production. Report issues or feedback through your support channels.

    -   **Web based applications**: AI agents run these desktop actions in the Google Chrome browser through a browser extension. For more information, see [Adaptive desktop actions for web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/web-agents-overview.md).

## Testing an AI agent or agentic workflow

Test an AI agent or agentic workflow that uses adaptive desktop actions in AI Agent Studio to evaluate its performance. For more information, see [Manually test an agentic AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md).

**Related topics**  


[Defined desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions.md)

[Adaptive desktop actions for web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/web-agents-overview.md)

[Defined desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)

[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

