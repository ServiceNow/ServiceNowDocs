---
title: Agent chat harness
description: The Agent Chat Harness is the conversational AI interface built into Lux Lab. It uses the Agent Communication Protocol \(ACP\) to connect external AI agents to your project context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/agent-chat-harness.html
release: zurich
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 5
keywords: [Agent chat harness, Chat panel context, Agent Communication Protocol, Opening the chat panel, Chat input toolbar, Switching agents, Custom providers \(beta\), Attaching context with @, Quick-start actions, Agent responses, Conversation history and sessions, MCP manager, General guidelines for working with agents]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Agent chat harness

The Agent Chat Harness is the conversational AI interface built into Lux Lab. It uses the Agent Communication Protocol \(ACP\) to connect external AI agents to your project context.

ACP is a structured layer between your project and the agent, and it gives agents the context to interpret your code, your instance, and your intent.

## Chat panel context

The Agent Chat Harness is a persistent chat panel embedded in the app, and it gives you direct conversational access to AI agents with context on the following:

-   Your open files and project structure
-   Your connected ServiceNow instance
-   Your conversation and session history
-   Git state and source control context

## Agent Communication Protocol

ACP is the communication layer between Lux Lab and external AI agents. It defines how Lux Lab packages context from your project and sends it to the agent. It also defines how Lux Lab surfaces the agent's responses and proposed actions in the app.

## Supported agents

Lux Lab supports connecting to the ACP-compatible agents in the following table.

|Agent|Notes|
|-----|-----|
|Claude Agent|Supported; set as default|
|Devin|Supported|
|Codex|Supported; requires your own API key|

**Important:** Lux Lab doesn't provide subscriptions or API keys for any agent. You must have your own active subscription or API key for the agent you use. Your own account with the respective provider governs agent usage and costs. Install and configure agents at your own discretion. Lux Lab only facilitates the connection.

## Opening the chat panel

You can open the chat panel in the following ways:

-   Select the **Agent Chat** icon \(speech bubble\) in the Activity Bar.
-   Press Cmd+Shift+B \(macOS\) / Ctrl+Shift+B \(Windows\).

By default, the panel opens on the right side of the app.

## Chat input toolbar

The bottom of the chat panel contains the message input and a toolbar with the controls in the following table.

|Control|Description|
|-------|-----------|
|**+**|Attaches context, for example images, files, code snippets, or plan board items|
|**&lt;&gt; Code ▾**|Switches the code context attached to the message|
|**Default \(recommended\) ▾**|Model and agent selector for switching between configured agents|
|Gear icon \(⚙️\)|Agent-specific settings, for example effort level, display when the active agent supports them|
|Microphone icon \(🎤\)|Voice input|
|Send icon \(**↑**\)|Sends the message|

## Switching agents

Select the model selector \(**Default \(recommended\) ▾**\) in the input toolbar to open the agent switcher, which lists the following options:

-   **Claude Agent**: Default, displays a check mark when active
-   **Devin**: Expand to configure
-   **Codex**: Requires an API key \(displays key icon\)
-   **Manage models &amp; agents**: Opens the full agent management settings

Select any agent to switch to it for the current conversation. When the agent supports them, agent-specific settings such as effort level may appear next to the model selector.

## Connecting a custom endpoint

Select **Add Custom Model** \(top right\) to open the connection dialog for any other OpenAI-compatible endpoint, including self-hosted or local servers such as Ollama. The dialog exposes the generic OpenAI-compatible fields in the following table.

|Field|Description|
|-----|-----------|
|**Provider name**|Label shown in the model selector for this provider|
|**Base URL**|Endpoint's OpenAI-compatible base URL, ending in `/v1`|
|**Model id**|Exact model identifier as reported by the endpoint|
|**Display name**|\(Optional\) Friendlier name shown in the model list|
|**API key**|\(Optional\) Key required by most hosted endpoints; local servers may ignore the value but still require the field to be non-empty|
|**Context**|\(Optional\) Model's context window size|

Select **Test connection** to verify the endpoint responds before saving, then select **Add model**.

## Attaching context with @

Enter `@` in the message input to open the context picker, which has the options in the following table.

|Option|Description|
|------|-----------|
|**Web**|Includes web search results as context|
|**Agents**|References or switches to a specific agent|
|**Skills**|Invokes an available skill to guide the agent|
|**Files**|Attaches a specific file from your project|
|**Git**|Includes Git state, for example the diff and commit history, as context|

Navigate the picker with ↑ / ↓, press Enter to select, and press Esc to cancel.

## Quick-start actions

When you open a new conversation with no prior messages, the chat panel shows quick-start action buttons for example **Create a widget** and **Create a page**. These buttons pre-fill a partial prompt in the input. You then complete the prompt with the specific details of what you want to build before sending.

## Agent responses

Agent responses stream into the conversation in real-time and can include plain text, code blocks, proposed file changes, and terminal commands.

## Plain text

Explanations and analysis appear as formatted markdown.

## Code blocks

Inline code snippets with syntax highlighting. Select **Copy** to copy the snippet, or **Insert at Cursor** to insert it directly into the active editor.

## Proposed file changes \(diffs\)

When the agent proposes editing a file, Lux Lab shows a diff preview inline with the actions in the following table.

|Button|Action|
|------|------|
|**View Full Diff**|Opens a side-by-side diff in the editor|
|**Apply**|Applies the change to the file immediately|
|**Reject**|Dismisses the proposed change|

You can undo any applied change with Cmd+Z / Ctrl+Z.

## Terminal commands

The agent may propose running a terminal command. A **Run** button appears next to the command. You can also copy the command and run it manually.

## Conversation history and sessions

Lux Lab stores each conversation as part of the project, with the following results:

-   Conversation history persists when you reopen the project.
-   Multiple agents can reference the shared conversation history as context.
-   You can start a new conversation from the chat panel header.
-   Past conversations are accessible from the conversation history list in the chat panel.

The chat panel also shows consumption details: how much of the agent's context window or quota your current session is using.

## MCP manager

The three-dot menu \(`…`\) in the chat panel header opens the Model Context Protocol \(MCP\) manager. In the manager, you can view and manage all configured MCP servers that extend the agent's capabilities.

## General guidelines for working with agents

The following general guidelines apply when you work with agents in the chat panel:

-   **Be specific.** Instead of "fix my code," try "the error on line 42 of NavBar.js says X — how do I fix it?"
-   **Use @ context.** Attach the relevant file or Git diff rather than pasting large code blocks.
-   **Review diffs carefully.** Apply agent-proposed changes one at a time and verify before continuing.
-   **Manage your quota.** Keep track of consumption details, because each agent has its own usage limits based on your subscription.

