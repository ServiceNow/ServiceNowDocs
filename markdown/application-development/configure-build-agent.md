---
title: Build Agent configuration
description: Build Agent connects your instance to AI-powered design workflows. Set up the required application and MCP server connections to start using it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/configure-build-agent.html
release: zurich
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent configuration

Build Agent connects your instance to AI-powered design workflows. Set up the required application and MCP server connections to start using it.

**Note:** To access all of the tools and features in the Zurich release, you must have the latest Family patches and the ServiceNow Otto for Creator ServiceNow Store update for Zurich Patch 8 \(April 2026\) installed.

Configuring Build Agent involves several sequential steps:

-   Installing the ServiceNow Otto for Creator application from the ServiceNow Store \(Check your entitlements to determine whether you have access to this application.\)
-   Activating the required plugins for your version
-   Establishing MCP server connections
-   Enabling additional settings, such as for tests and custom instructions

Complete these steps to verify that all dependencies and integrations are in place before using Build Agent.

-   **[Install Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/install-build-agent.md)**  
For the Premium version of Build Agent, install the ServiceNow Otto for Creator application from the ServiceNow Store.
-   **[Build Agent plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-plugins.md)**  
The plugins for Build Agent depend on whether you're using the free/trial version or premium version.
-   **[Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-connct-mcp-server.md)**  
Connect a supported MCP server to Build Agent to access external tools and resources in the chat panel when building and editing apps.
-   **[Configure custom skills and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-configure-custom-skills-rules.md)**  
Create and manage custom skills and rules, or instructions to control how Build Agent behaves during a session. Rules are preloaded into every session automatically. Skills are available on demand when you or the agent invokes them by name.
-   **[Configure auto test prompting and UI tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-config-testing.md)**  
Configure test settings to enable automatic test prompting and execution of UI tests in Build Agent.
-   **[Configure web search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-configure-settings.md)**  
Enable the web search tool so that Build Agent can search the public web and retrieve relevant information when responding to queries.

**Parent Topic:**[Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent.md)

