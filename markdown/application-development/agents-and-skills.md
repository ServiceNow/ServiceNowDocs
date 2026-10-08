---
title: Agents and skills
description: The Agents and Skills panel is an explorer that surfaces all agents and skills available in your current project and on your system. It gives you a single place to check what is configured and ready to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/agents-and-skills.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Agents and skills, Opening the panel, Panel contents, Skills in the chat]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Agents and skills

The Agents and Skills panel is an explorer that surfaces all agents and skills available in your current project and on your system. It gives you a single place to check what is configured and ready to use.

## Opening the panel

Select the **Agents and Skills** icon in the Activity Bar to open the panel. The panel lists the following items:

-   **Agents**

    All ACP-compatible agents configured on your system, such as Claude, Devin, and Codex

-   **Skills**

    All skills bundled with Lux Lab and any project-specific skills present in your project


## Panel contents

The panel is a read-only explorer. It does not configure or install agents. It reflects the following existing setup:

-   Bundled Lux skills are shown automatically.
-   Project-level skills, if present in your project directory, are listed alongside the bundled ones.
-   Configured agents appear as they're registered through the [Agent chat harness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/agent-chat-harness.md).

To configure agents or install new ones, use **Manage models &amp; agents** from the agent switcher in the chat panel.

## Skills in the chat

You can attach any skill visible in this panel to a chat message with the `@` context picker, by selecting **Skills** from the picker. For details on using context in the chat, see [Agent chat harness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/agent-chat-harness.md).

**Related topics**  


[Agent chat harness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/agent-chat-harness.md)

[Configuring Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configuring-lux-lab.md)

