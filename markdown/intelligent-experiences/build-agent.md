---
title: Build Agent
description: This AI agent enables developers to create, edit, and deploy full-stack ServiceNow applications to update sets that encompass both user interface and back-end components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/build-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Build Agent]
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Build Agent

This AI agent enables developers to create, edit, and deploy full-stack ServiceNow® applications to update sets that encompass both user interface and back-end components.

**Important:** Build Agent uses a different framework than other ServiceNow® AI agents. Review the following workflow and configuration settings for Build Agent. For more information, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent.md).

## Workflow

You describe what to build or change in natural language, and Build Agent proposes, applies, tests, and builds the changes for your review. The workflow is the same in ServiceNow Studio and the ServiceNow IDE.

1.  Based on the user's request, parse the requirements.
2.  Propose the application and files to create or modify.
3.  Display the proposed edits, diffs, and summaries, and pause for user approval.
4.  Once approved, edit the code or metadata, or scaffold a new application.
5.  Repeat until the requested metadata changes are complete.
6.  When prompted, or after asking the user depending on the configuration, create and run Automated Test Framework \(ATF\) tests.
7.  If tests fail, triage the failures and produce a regression test suite for monitoring app health.
8.  Build the application.

## Configuration

<table id="table_tlf_ylx_skc"><thead><tr><th>

Configuration area

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugins

</td><td>

Plugins are required for Build Agent and vary by version.-   For Build Agent \(Trial/Free\): `sn_glider` and `sn_build_agent` plugins.
-   For Build Agent \(Premium\): the `sn_now_creator` plugin, which contains the `sn_build_agent_pro` plugin.

</td></tr><tr><td>

Access

</td><td>

Build Agent is accessible in both ServiceNow Studio and the ServiceNow IDE.

</td></tr><tr><td>

Model context protocol \(MCP\) servers

</td><td>

Build Agent enables access to external tools and resources through standardized communication \(MCP servers\). For more information, see [MCP connections and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/accelerate-design-to-development-with-figma-mcp-server.md) and [Connect Build Agent to a supported MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-connct-mcp-server.md).

</td></tr><tr><td>

Tests

</td><td>

Test settings determine whether Build Agent and Autonomous Engineer generate and run Automated Test Framework \(ATF\) tests in conversations.-   **Sync ATF tests with app**: Generates ATF tests when the agent creates an app, and keeps the tests synced when the app is edited.
-   **Run UI ATF tests**: Runs client-side and server-side UI ATF tests. This setting requires **Sync ATF tests with app** and is off by default because UI test runs are slower.

For more information, see [Configure auto test prompting and UI tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-config-testing.md).

</td></tr><tr><td>

Custom instructions

</td><td>

Custom instructions control how Build Agent behaves during a session.-   Rules are preloaded into every session automatically. Rules enforce consistent behavior, such as naming conventions or organizational standards.
-   Skills are available on demand when a user or the agent invokes them by name. Skills provide task-specific guidance, such as internal guidelines for a particular workflow pattern.

The **Applies To** setting determines which sessions use an instruction: all sessions on the instance, sessions within a specific application scope, or only the sessions of the user who created it. For more information, see [Configure custom skills and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-configure-custom-skills-rules.md).

</td></tr></tbody>
</table>## Access roles

Build Agent uses the following existing roles for access control and feature masking.

-   **sn\_glider.admin**

    Users with this role have the following

    -   Access control lists \(ACLs\) on all Build Agent tables
    -   Read and write access on operational system properties
    -   Role masking for the Build Agent and Build Agent Preprocessor ServiceNow Otto skills
-   **admin**

    Users with this role have read access on protected system properties, such as prompt limits and tier overrides.


**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

