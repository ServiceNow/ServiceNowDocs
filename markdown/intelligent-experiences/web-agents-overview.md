---
title: Adaptive desktop actions for web-based tasks
description: Desktop actions for adaptive paths enable AI agents to automate repetitive tasks across web applications and websites without preconfigured APIs, scripts, or other back-end logic. Desktop actions enable AI agents to access and interact with a website or web application through the browser extension just as you would—clicking, typing, and scrolling—to execute actions on your behalf.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-09-05"
reading_time_minutes: 5
keywords: [explore, AI Agents, Agentic AI]
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# Adaptive desktop actions for web-based tasks

Desktop actions for adaptive paths enable AI agents to automate repetitive tasks across web applications and websites without preconfigured APIs, scripts, or other back-end logic. Desktop actions enable AI agents to access and interact with a website or web application through the browser extension just as you would—clicking, typing, and scrolling—to execute actions on your behalf.

## Adaptive desktop actions overview

Desktop actions are tools that AI agents use to interact with web applications through a browser extension. When you configure an AI agent and select desktop action as a tool, you define whether the AI agent follows a defined path \(fixed steps designed in AI Desktop Actions\) or an adaptive path \(high-level goal described in the tool configuration\). Unlike defined path desktop actions that follow preconfigured workflows, adaptive path desktop actions enable AI agents to dynamically plan and execute tasks based on high-level instructions.

These AI agents access the browser through the browser extension and do not use preconfigured APIs, scripts, or other back-end logic. They function as interactive, visible assistants that process UI states and determine subsequent actions through UI actions. Simply tell an AI agent what you need, from updating user roles to scheduling maintenance, and it handles the work for you. The AI agent performs these tasks in a separate browser tab without requiring manual intervention. It performs tasks in a similar way to humans interacting with the UI: analyzing the screen state, identifying UI elements, and selecting the next action based on the configured instructions. You can also take control to complete the task manually.

## How adaptive desktop actions work

1.  Request initiation: The user describes a task in the Now Assist panel. For example, "Update all open incidents assigned to the Network team to include priority level in the short description".
2.  Agent activation: The AI agent is triggered and analyzes the request.
3.  Tool selection: The AI agent identifies that it needs to use the desktop action tool configured for adaptive paths.
4.  Plan generation: The AI agent creates a step-by-step plan based on the high-level instructions in the tool configuration.
5.  User confirmation: The plan is presented to the user for approval in the Now Assist panel.
6.  Execution: Once confirmed, the AI agent opens a separate browser tab and performs the task.
7.  Visual feedback: Screenshots of each step appear in the **Web view** tab of the Now Assist panel so you can monitor progress.

## LLM provider

Adaptive desktop actions use AWS Anthropic Sonnet model provider.

## Users

Adaptive path desktop actions are designed for all users who perform tasks across enterprise applications and want to automate repetitive work:

|User|Description|
|----|-----------|
|Administrators|Manage permissions, roles, and agentic workflows|
|Developers|Build and configure AI agents with desktop action tools|
|Fulfillers|Automate routine fulfillment tasks across multiple systems|
|Requestors|Manage browser extensions and submit requests that trigger AI agents to automate web workflows|

## Configuring adaptive desktop actions

1.  Create or edit an AI agent and an agentic workflow.
2.  At the tool selection step, choose **Desktop Action**.
3.  For adaptive paths, describe the high-level goal in the tool configuration \(no design work in AI Desktop Actions is required.\)
4.  Configure permissions and browser extension settings

**Note:** End-users must download and install a Google Chrome browser extension locally, and configure it to connect to a target ServiceNow instance. For more information, see [Install the Google Chrome extension for adaptive desktop actions](../task/na-ai-wa-install-browser-extension.md).

On the ServiceNow instance, an admin must configure at least one agentic workflow that involves an AI agent. For more information, see [Create an agentic workflow for automating web tasks](../task/na-ai-wa-configure-workflow.md).

## Operating desktop actions

You access desktop actions through the Now Assist panel that has enhanced chat enabled. The AI agent provides updates on its progress in the chat interface. As the agent works, you receive:

-   Real-time status updates in the chat
-   Periodic screenshots of the web pages the agent navigates
-   Notifications when external websites require login credentials

When an external website requires login, you're prompted in the chat. Switch to the external website tab, provide your credentials, then switch back to the Now Assist panel. The agent will continue once authentication is complete.

**Note:** When you close the chat, you have the option to delete the chat log including all screenshots containing sensitive information.

## Limitations

Desktop actions operate as browser extensions with the following limitations:

-   Can only access content within the browser
-   Cannot interact with desktop applications or local files \(except for downloading files\)
-   Cannot upload data from the local file system

For tasks requiring local file access, consider using defined path desktop actions or alternative automation tools.

## Third-party website access

When you use ServiceNow desktop actions to visit, access, log into, or otherwise interact with \(collectively, “Access”\) websites, applications, or other digital properties owned or operated by a third party \(“Third Party Services”\), that Access is a direct interaction between you and the Third Party Services. You are responsible for adhering to any applicable terms and conditions, including all policies or statements governing the use of personal data, of the third party.

**Important:**

ServiceNow AI Desktop Actions rely on “computer use,” a beta technology provided by Anthropic. As a result, AI Desktop Actions users are subject to unique risks, including as described in Anthropic's documentation. Notwithstanding anything to the contrary in any customer agreement, or any other agreement governing a customer's use of ServiceNow offerings, ServiceNow AI Desktop Actions are provided “as is” and without representations or warranties of any kind, including any warranty that AI Desktop Actions will be uninterrupted, error free, or free of harmful components, or that any data, including customer data, will be secure or not otherwise lost or damaged.

**Related topics**  


[Configure AI Desktop Actions](../task/configure-agentic-desktop.md)

[Creating AI agents for AI Desktop Actions](create-ai-agents-ad.md)

[Examples of executing desktop actions using AI agents](use-agentic-desktop.md)

