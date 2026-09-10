---
title: Accessing Build Agent in ServiceNow Studio
description: Build Agent is available in ServiceNow Studio for UI-first, declarative workflows. You can also use Build Agent the ServiceNow IDE within ServiceNow Studio for code-first, autonomous full-stack development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/access-build-agent.html
release: zurich
topic_type: concept
last_updated: "2026-09-02"
reading_time_minutes: 5
keywords: [Build Agent, ServiceNow Studio, ServiceNow IDE, access, development, AI agent, chat panel, Personal Development Instance, PDI, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Accessing Build Agent in ServiceNow Studio

Build Agent is available in ServiceNow Studio for UI-first, declarative workflows. You can also use Build Agent the ServiceNow IDE within ServiceNow Studio for code-first, autonomous full-stack development.

## Opening Build Agent

When you open ServiceNow Studio, the central chat area on the home page is where you chat with Build Agent to start a new conversation.

\[Omitted image "ba-sns-full-page-chat.png"\] Alt text: ServiceNow Studio home screen with a Build Agent prompt input area, Recents panel, Recent chats panel, and Plans panel listing example plans with statuses.

To open an existing conversation, select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel. The Build Agent panel then opens on the left.

\[Omitted image "ba-sns-panel-left.png"\] Alt text: Home screen in ServiceNow Studio with the Build Agent panel open. For a description of the interface panels, refer to the surrounding text.

**Note:**

-   Currently, only admins have permissions to use Build Agent.
-   You must have the correct plugins installed to access Build Agent. For more information, see [Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/install-build-agent.md).

You can start a Build Agent session with an active working set already loaded by right-clicking an artifact in the ServiceNow AI Platform, which displays a list of related metadata that you can edit. Then select the **Configure** option, which opens the record in ServiceNow Studio. From there, you can start a new Build Agent conversation about what you want to do with the metadata.

## Build Agent environments

You can use Build Agent in both ServiceNow Studio, which contains the ServiceNow IDE if you want to create apps in source code.

Your choice on where to access Build Agent depends on your role and workflow.

|Usage|ServiceNow Studio|ServiceNow IDE|
|-----|-----------------|--------------|
|Generally best for|ServiceNow AI Platform developers, app owners, admins, citizen developers, and business analysts|Developers who prefer using an IDE on platform, TypeScript, and ServiceNow Fluent workflows|
|Code approach|Metadata-driven \(tables, fields, business rules, scripts\); embedded Build Agent|ServiceNow Fluent DSL \(`.now.ts` files\), TypeScript, React|
|Deployment|System Update Sets; ServiceNow Studio package and install|ServiceNow SDK build, deploy, and install|
|UI creation|Forms, lists, workspaces \(Next Experience\), and catalog items|React UI pages and custom interfaces|
|Source control|System Update Sets; source control via linked repositories|Git built-in with branching|
|Local dev option|No; runs on the instance|Yes, VS Code with `@servicenow/now-sdk`|

## Key differences between ServiceNow Studio and the ServiceNow IDE

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

## Handing off ServiceNow Otto conversations to Build Agent

You can continue a ServiceNow Otto conversation from another product in Build Agent without repeating your intent. When ServiceNow Otto detects that you want to build or modify an application, it creates a handoff record. ServiceNow Studio then uses that handoff record to open Build Agent with your conversation context already loaded.

The handoff record stores a versioned summary of the conversation and a reference to the full transcript. ServiceNow Studio reads the handoff record and opens Build Agent with the summary pre-filled as an editable prompt in the chat panel. When that happens, Build Agent doesn't run automatically. You must review and edit the pre-filled prompt before submitting it. The full ServiceNow Otto transcript is attached to the session so you can reference details from the original conversation that the summary doesn't include.

**Note:** To use conversation handoff:

-   You must have access to both ServiceNow Otto® and Build Agent.
-   You must be working in ServiceNow Studio.

## Build Agent and sandboxes

Use Build Agent in an isolated development environment with Developer Sandboxes. Sandboxes provide parallel development for distributed developers, with isolated metadata and Git integration. For more information, see [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/sandboxes-landing.md).

## Build Agent and PDIs

You can access Build Agent on a Personal Development Instance \(PDI\). Developers using PDIs get 25 prompts per instance per 30-day cycle.

PDIs are updated to match the latest Build Agent for a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments. For more information on PDIs, see [Personal developer instance guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/personal_developer_instance_guide.md).

## Notes and limitations

Keep the following in mind when using Build Agent:

-   Build Agent generates metadata supported by ServiceNow Fluent. Verify artifact compatibility before approval.
-   Feature availability and UI details might differ between monthly releases. Confirm behavior against your instance version.

For more information on limitations, see [Build Agent limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-limitations.md).

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

