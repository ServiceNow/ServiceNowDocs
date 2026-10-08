---
title: Extend ServiceNow Cowork
description: Extend Cowork with skills, scheduled task, Model Context Protocol \(MCP\) servers, and sub-agents so the agent can handle more of your work. Each option adds new instructions, tools, or specialized agents, and you control what the agent can access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/extending-cowork.html
release: zurich
topic_type: concept
last_updated: "2026-09-27"
reading_time_minutes: 3
keywords: [Extending ServiceNow Cowork, Extending Cowork]
breadcrumb: [Use, ServiceNow Cowork, Enable AI experiences]
---

# Extend ServiceNow Cowork

Extend Cowork with skills, scheduled task, Model Context Protocol \(MCP\) servers, and sub-agents so the agent can handle more of your work. Each option adds new instructions, tools, or specialized agents, and you control what the agent can access.

-   **Skills and custom skills**

    Skills give Cowork instructions for specific kinds of work, such as creating documents, summarizing data, or planning your time. Each skill is a folder of instructions, so you can version it, review it, and share it with a teammate.

    ServiceNow provides default skills, and you can add custom skills for workflows that the defaults don't cover. Some skills run automatically when a request matches their description, so the right skill loads when the work calls for it and you don't need to memorize commands. Others run as slash commands that you enter in a chat. Some skills require a connector, such as Microsoft 365 or ServiceNow. In Settings &gt; Skills, you can filter skills by source, invocation type, and connector.

    Go to **Settings** &gt; **Skills** to filter skills by source, invocation type, and connector.

    A custom skill captures how you do a task, including the steps, format, and sources, so the next run takes one prompt instead of detailed instructions. You can turn a task you already do well into a custom skill and share it with your team. Cowork includes a default skill that creates custom skills for you from a description of the task. When no skill fits a request, Cowork can build one and save it for next time. i

-   **MCP servers**

    MCP servers add tools and data from other services, such as Sentry, SerpApi, and Postman. You can add servers from the available list or add your own. Each server uses the authentication method that its service requires, such as an API key or OAuth.

-   **Sub-Agents**

    Sub-Agents are specialized agents that the main agent hands work to. Each sub-agent has its own instructions and uses only the skills and MCP servers that you grant it. ServiceNow provides built in sub-agents for tasks such as research, ServiceNow analysis, and code review, and you can create custom sub-agents for your own specialized tasks.Cowork provides built in sub-agents, including:

    -   default: Plans the work and keeps context across tools.
    -   sn-analyst: Analyzes incidents, changes, and operations with deep platform expertise.
    -   comms-scheduler: Drafts email and schedules meetings using context from memory.
    -   explorer: Gives fast, read only answers across files, ServiceNow data, and documentation.

Skills tell Cowork how to do the work, MCP servers and connectors give it access to the services it needs, and sub-agents divide larger work into focused tasks. For example, a custom sub-agent for weekly reporting can use a status summary skill and the tools from an MCP server, while the main agent coordinates the overall task.

Extending Cowork doesn't change your safeguards. Cowork still asks for approval before sensitive actions, and commands run in the agent sandbox. Local MCP servers are the exception. They run on the device outside the agent sandbox and can act without asking for approval, so administrators can turn them off. For more information, see [Turn off local MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/turn-off-local-mcp-servers.md). To limit access, grant each sub-agent only the skills and MCP servers it needs.

-   **[Create a custom skill in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-custom-skill.md)**  
Create a skill for Cowork to do a specific task, customizing it to fit your needs. After running the same type of task a few times, turn it into a skill so future runs require just one prompt instead of detailed instructions.
-   **[Create a sub-agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-sub-agent.md)**  
Create a custom sub-agent to hand off a specialized task, such as code review or security analysis, to a reusable agent with focused instructions and limited access. A narrow scope helps produce consistent results, limiting the sub-agent to only the skills and MCP servers it requires.
-   **[View and edit a sub-agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/view-edit-subagent.md)**  
Review a sub-agent's system prompt to understand how it behaves, and edit it when its results don't match what you need or its scope needs to change.
-   **[Connect ServiceNow Cowork to MCP servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-servers.md)**  
Connect MCP servers so Cowork can use tools and data from other services, such as GitHub, Sentry, SerpApi, and Postman. Each server you connect adds capabilities to the agent, and you control which servers each sub-agent can use.

**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-using.md)

