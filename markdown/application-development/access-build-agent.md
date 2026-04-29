---
title: Accessing Build Agent in ServiceNow Studio and the ServiceNow IDE
description: Build Agent is available in ServiceNow Studio \(UI-first, declarative workflows\) and the ServiceNow IDE \(code-first, autonomous full-stack development\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 3
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Accessing Build Agent in ServiceNow Studio and the ServiceNow IDE

Build Agent is available in ServiceNow Studio \(UI-first, declarative workflows\) and the ServiceNow IDE \(code-first, autonomous full-stack development\).

## Opening Build Agent

When you open ServiceNow Studio or the ServiceNow IDE, the Build Agent should appear by default. If it doesn't appear, If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser.

**Note:**

-   Currently, only admins have permissions to use Build Agent.
-   You must have Now Assist for Creator installed to access Build Agent. For more information, see [Install Build Agent](../tasks/install-build-agent.md).

![If Build Agent isn't open, open it from the status bar in the corner of your browser.](../../servicenow-studio/image/sn-studio-access-build-agent.png "Open Build Agent")

## Build Agent chat panel

Use the Build Agent chat panel to create or update an app or app file. Make a selection to begin the chat, or enter a prompt.

![Begin a conversation by selecting an option to create or update an app or app file.](../../servicenow-studio/image/sn-studio-ba-new-chat.png "New chat panel")

Continue your conversation in the chat panel until you're happy with the results.

<table id="table_x2g_4c2_m3c"><thead><tr><th>

Function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New chat icon ![](../../servicenow-studio/image/sn-studio-ba-new-chat-icon.png)

</td><td>

Open a new chat in the Build Agent chat panel.Begin a new chat when you want to start working on a new application or need a fresh start for updates.

</td></tr><tr><td>

Chats icon ![](../../servicenow-studio/image/sn-studio-ba-chats-icon.png)

</td><td>

See a list of all your chats with Build Agent.

</td></tr><tr><td>

Checkpoints icon ![](../../servicenow-studio/image/sn-studio-ba-checkpoint-icon.png)

</td><td>

See a list of all the checkpoints within your current chat with Build Agent.Checkpoints show all the progress points in your application. You can revert to any of these checkpoints during the course of developing your app.

</td></tr></tbody>
</table>## Key differences between ServiceNow Studio and the ServiceNow IDE

|Area|ServiceNow Studio|ServiceNow IDE|
|----|-----------------|--------------|
|Primary style|UI-first, declarative, metadata-centric|Code-first, conversational, full-stack|
|Typical users|Low-code builders, admins|Pro-code developers|
|Interaction model|Guided steps with suggestions, diffs, and summaries; selectable modes \(guided, batch, one-shot\)|Chat-driven autonomous generation; user approves edits, then build and deploy|
|Scope of automation|Create or update platform metadata \(tables, flows, experiences\) with dependency awareness|Generate and edit entire scoped or global apps \(UI and backend\), explain or repair code, run queries, create documentation|
|Change control|Strong guardrails; preview via ServiceNow Studio diff surfaces|Approval gates before writing; build and deploy workflow in the ServiceNow IDE|
|Best fit|Iterative configuration, edits, low-code delivery|Greenfield app creation, deep refactors, debugging, multi-artifact edits|
|Dependencies|Uses the ServiceNow Studio agentic experience layer and metadata explorers|Relies on the ServiceNow IDE workspace, file and metadata explorers, and build pipeline|

**Note:** You can do conversational checkpoints with Build Agent and roll back to the last conversation checkpoint in both ServiceNow Studio and the ServiceNow IDE.

Build Agent is available in both ServiceNow Studio and the ServiceNow IDE, but each environment emphasizes a different development style. ServiceNow Studio provides a guided, UI-first experience that focuses on metadata creation and controlled, iterative changes. The ServiceNow IDE provides a code-first experience with an autonomous agent capable of generating and modifying full-stack applications through conversational prompts.

Choose the environment based on your skill set and the type of work:

-   ServiceNow Studio: Low-code builders and admins who prefer declarative, metadata-driven workflows with previews, diffs, and guardrails.
-   ServiceNow IDE: Pro-code developers who need conversational, code-centric generation, advanced customization, and end-to-end build and deploy steps.

## Notes and limitations

Keep the following in mind when using Build Agent:

-   Build Agent generates metadata supported by ServiceNow Fluent. Verify artifact compatibility before approval.
-   Feature availability and UI details might differ between monthly releases. Confirm behavior against your instance version.

For more information on limitations, see [Build Agent limitations](build-agent-limitations.md).

**Parent Topic:**[Use Build Agent](../tasks/use-build-agent.md)

