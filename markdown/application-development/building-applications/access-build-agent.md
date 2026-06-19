---
title: Accessing Build Agent in ServiceNow Studio and the ServiceNow IDE
description: Build Agent is available in ServiceNow Studio \(UI-first, declarative workflows\) and the ServiceNow IDE \(code-first, autonomous full-stack development\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/access-build-agent.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 5
keywords: [Build Agent, ServiceNow Studio, ServiceNow IDE, access, development, AI agent, chat panel, Personal Development Instance, PDI, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Accessing Build Agent in ServiceNow Studio and the ServiceNow IDE

Build Agent is available in ServiceNow Studio \(UI-first, declarative workflows\) and the ServiceNow IDE \(code-first, autonomous full-stack development\).

You can watch a short video on how to access Build Agent in ServiceNow Studio.

Access Build Agent 

## Build Agent and PDIs

You can access Build Agent on a Personal Development Instance \(PDI\). Developers using PDIs get 25 prompts per instance per 30-day cycle.

PDIs are updated to match the latest Build Agent for a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments. For more information on PDIs, see [Personal developer instance guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/personal_developer_instance_guide.md).

## Build Agent environments

You can use Build Agent in both ServiceNow Studio and the ServiceNow IDE. Your choice depends on your role and workflow.

|Usage|ServiceNow Studio|ServiceNow IDE|
|-----|-----------------|--------------|
|Generally best for|ServiceNow AI Platform developers, app owners, admins, citizen developers, and business analysts|Developers who prefer using an IDE on platform, TypeScript, and ServiceNow Fluent workflows|
|Code approach|Metadata-driven \(tables, fields, business rules, scripts\); embedded Build Agent|ServiceNow Fluent DSL \(`.now.ts` files\), TypeScript, React|
|Deployment|System Update Sets; ServiceNow Studio package and install|ServiceNow SDK build, deploy, and install|
|UI creation|Forms, lists, workspaces \(Next Experience\), and catalog items|React UI pages and custom interfaces|
|Source control|System Update Sets; source control via linked repositories|Git built-in with branching|
|Local dev option|No; runs on the instance|Yes, VS Code with `@servicenow/now-sdk`|

## Opening Build Agent

When you open ServiceNow Studio or the ServiceNow IDE, the Build Agent should appear by default. If it doesn't appear, If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser. You can also select the Sparkle icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the application banner.

**Note:**

-   Currently, only admins have permissions to use Build Agent.
-   You must have the correct plugins installed to access Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/install-build-agent.md).

\[Omitted image "sn-studio-access-build-agent.png"\] Alt text: If Build Agent isn't open, open it from the status bar in the corner of your browser.

## Build Agent chat panel

Use the Build Agent chat panel to create or update an app or app file. Make a selection to begin the chat, or enter a prompt.

\[Omitted image "sn-studio-ba-new-chat.png"\] Alt text: Begin a conversation by selecting an option to create or update an app or app file.

Continue your conversation in the chat panel until you're happy with the results.

<table id="table_x2g_4c2_m3c"><thead><tr><th>

Function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New chat icon \[Omitted image "sn-studio-ba-new-chat-icon.png"\] Alt text:

</td><td>

Open a new chat in the Build Agent chat panel.Begin a new chat when you want to start working on a new application or need a fresh start for updates.

</td></tr><tr><td>

Chats icon \[Omitted image "sn-studio-ba-chats-icon.png"\] Alt text:

</td><td>

See a list of all your chats with Build Agent.

</td></tr><tr><td>

Checkpoints icon \[Omitted image "sn-studio-ba-checkpoint-icon.png"\] Alt text:

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

For more information on limitations, see [Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-limitations.md).

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/use-build-agent.md)

