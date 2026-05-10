---
title: Exploring AI Desktop Actions
description: Create desktop actions with AI Desktop Actions to automate repetitive tasks on your desktop and web environment using AI agents and agentic workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-02"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [AI Desktop Actions, Enable AI experiences]
---

# Exploring AI Desktop Actions

Create desktop actions with AI Desktop Actions to automate repetitive tasks on your desktop and web environment using AI agents and agentic workflows.

## AI Desktop Actions overview

AI Desktop Actions is a no-code solution that helps you automate repetitive tasks in legacy desktop and web-based applications lacking APIs or backend integrations. AI Desktop Actions leverages AI agents created in the ServiceNow AI Platform to interact with desktop and web applications, perform UI-based tasks, and automate end-to-end workflows.

Desktop actions are tools used by AI agents—they are not AI agents themselves. Think of it this way:

-   **AI Agent**: The orchestrator that receives user requests and coordinates task execution
-   **Desktop Action Tool**: The capability the AI agent uses to interact with desktop or web applications

## Defined path desktop actions for desktop and web-based tasks

You can use AI Desktop Actions to execute predefined automation sequences on your desktop. Defined path actions provide consistent, repeatable workflows for common desktop tasks. AI Desktop Actions is a client application that is installed on the Windows operating system. The app offers two workspaces, the Design workspace, where you create and configure desktop automations, and the Execution workspace, where those automations run. The Design workspace enables you to automate multi-step processes by recording or manually capturing a fixed sequence of steps. Execution workspace enables AI agents to execute desktop actions in an isolated desktop session.

The Design workspace lets you build multi-step desktop actions by recording or manually capturing steps. The Execution workspace runs desktop actions in an isolated desktop session and is launched automatically when you test a desktop action or trigger an automation from the Now Assist panel. You do not open the Execution workspace manually. For more information, see [Defined path desktop actions for desktop and web-based tasks](desktop-actions.md).

## Adaptive path desktop actions for web-based tasks

You can automate web-based tasks that involve adaptive steps using desktop actions. You create desktop actions in AI Agent Studio as part of a tool configuration for an AI agent. When a user triggers an AI agent from the Now Assist panel, the AI agent uses the desktop action tool to open a separate browser tab and performs the task. Screenshots of each step appear in the **Web view** tab of the Now Assist panel enahnced chat so you can monitor progress. For example, opening the application, selecting fields, and completing a workflow. The AI agent checks the state of the page and adjusts the sequence based on the user's goal. Because the steps are adjusted dynamically, results may vary. Review the output for accuracy before accepting it. For more information, see [Adaptive path desktop actions for web-based tasks](web-agents-overview.md).

## How it fits into ServiceNow workflows

AI Desktop Actions integrates with AI Agent Studio, enabling you to publish, manage, and incorporate desktop actions into your broader ServiceNow workflows. This integration lets you automate both cloud and desktop applications, giving your AI agents broader capabilities within ServiceNow.

## Impersonating users

You can trigger AI agents from the Now Assist panel while impersonating another user, provided the impersonated user has the required roles. The sn\_aia.admin role is required to use AI Agent Studio, and the now\_assist\_panel\_user role is required to trigger AI agents that execute desktop actions in the Execution workspace. For more information, see [Impersonating users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_ImpersonateAUser.md).

## What to explore next

To learn more about configuring and using AI Desktop Actions, see:

-   [Configure AI Desktop Actions](../task/configure-agentic-desktop.md)
-   [Defined path desktop actions in AI Desktop Actions](desktop-actions-designer-workspace-ad.md)
-   [Creating AI agents for AI Desktop Actions](create-ai-agents-ad.md)
-   [Examples of creating desktop actions](examples-of-agentic-desktop-automation.md)
-   [Examples of executing desktop actions using AI agents](use-agentic-desktop.md)
-   [Components installed with AI Desktop Actions](../reference/components-installed-with-agentic-desktop.md)
-   [System requirements and limitations in AI Desktop Actions](../reference/sys-req-limitations-ad.md)

