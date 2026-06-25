---
title: Adaptive desktop actions for web-based tasks
description: Adaptive desktop actions enables AI agents to automate repetitive tasks across web applications through a browser extension. The agent interacts directly with the browser by clicking, typing, and scrolling, without preconfigured APIs, scripts, or back-end logic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/web-agents-overview.html
release: australia
topic_type: concept
last_updated: "2025-09-05"
reading_time_minutes: 3
keywords: [explore, AI Agents, Agentic AI]
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# Adaptive desktop actions for web-based tasks

Adaptive desktop actions enables AI agents to automate repetitive tasks across web applications through a browser extension. The agent interacts directly with the browser by clicking, typing, and scrolling, without preconfigured APIs, scripts, or back-end logic.

## Adaptive desktop actions overview

Desktop actions are tools that AI agents use to interact with web applications through a browser extension.

When you configure an AI agent and select Desktop action as a tool, you choose how it operates:

|Mode|How it works|Use when|
|----|------------|--------|
|Defined path|Follows fixed steps preconfigured in AI Desktop Actions.|The workflow is stable and steps are known in advance.|
|Adaptive path|Works from a high-level goal. Dynamically plans and executes steps based on your instructions.|The workflow varies or steps cannot be fully defined in advance.|

Specify a high-level goal — such as updating user roles or scheduling maintenance — and the agent plans and executes the steps to complete it. You can take manual control at any point.

## How adaptive desktop actions work

\[Omitted image "adaptive-da-working.png"\] Alt text: Stages in which adaptive desktop actions work

## LLM provider

Adaptive desktop actions use AWS Anthropic Sonnet model provider.

## Users

Adaptive desktop actions are available to all users who perform tasks across enterprise applications and automate repetitive work.

|Users|Description|
|-----|-----------|
|Administrators|Manage permissions, roles, and agentic workflows|
|Developers|Build and configure AI agents with desktop action tools|
|Fulfillers|Automate routine fulfillment tasks across multiple systems|
|Requestors|Manage browser extensions and submit requests that trigger AI agents to automate web workflows|

## Operating desktop actions

You access desktop actions through the Now Assist panel that has enhanced chat enabled. The AI agent provides updates on its progress in the chat interface. As the agent works, you receive:

-   Real-time status updates in the chat
-   Periodic screenshots of the web pages the agent navigates
-   Notifications when external websites require login credentials

When an external website requires login, you're prompted in the chat. Switch to the external website tab, provide your credentials, then switch back to the Now Assist panel. The agent continues after authentication is complete.

**Note:** When you close the chat, you have the option to delete the chat log, including all screenshots containing sensitive information. For more information, see [Delete an AI agent chat log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-wa-delete-chat-log.md).

## Limitation

Desktop actions operate as browser extensions with the following limitations:

-   Can only access content within the browser
-   Cannot interact with desktop applications or local files \(except for downloading files\)
-   Cannot upload data from the local file system

For tasks requiring local file access, consider using defined desktop actions. For more information, see [Defined path desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions.md).

## Third-party website access

When you use ServiceNow desktop actions to visit, access, log in to, or otherwise interact with \(collectively, “Access”\) websites, applications, or other digital properties owned or operated by a third party \(“Third Party Services”\), that Access is a direct interaction between you and the Third Party Services. You're responsible for adhering to any applicable terms and conditions, including all policies or statements governing the use of personal data, of the third party.

**Important:**

ServiceNow AI Desktop Actions rely on “computer use,” a beta technology provided by Anthropic. As a result, AI Desktop Actions users are subject to unique risks, including as described in Anthropic's documentation. Notwithstanding anything to the contrary in any customer agreement, or any other agreement governing a customer's use of ServiceNow offerings, ServiceNow AI Desktop Actions are provided “as is” and without representations or warranties of any kind, including any warranty that AI Desktop Actions will be uninterrupted, error free, or free of harmful components, or that any data, including customer data, will be secure or not otherwise lost or damaged.

**Related topics**  


[Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md)

[Creating AI agents for AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-agents-ad.md)

[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

