---
title: Build Agent tools
description: Build Agent tools support application development tasks such as semantic search, schema inspection, code search, planning, UI validation, database querying, app navigation, and script execution. Each tool extends what Build Agent can do during a build session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-tools.html
release: zurich
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent tools

Build Agent tools support application development tasks such as semantic search, schema inspection, code search, planning, UI validation, database querying, app navigation, and script execution. Each tool extends what Build Agent can do during a build session.

## Code search tool

The code search tool searches workspace files by exact text or regex patterns. Use the code search tool to find references to a field, script, or function across your app, and to understand the impact of a change before making it.

## Open app tool

For applications that were not developed using the ServiceNow IDE, ServiceNow Studio, or the ServiceNow SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the open app tool to locate the application you want. Alternatively, you can search for an application directly within the Build Agent, and it will automatically use the open app tool. The open app tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.

## Planning tool

Build Agent includes a planning tool that creates a detailed, step-by-step plan for your application development. You can refine the plan iteratively by prompting for changes and providing feedback until you reach a final version.

## Rollback script tool

The rollback script tool reverts a previous run script tool operation on demand. After Build Agent runs a script, it returns a rollback context you can use to undo that run. Use the rollback script tool when a script run produces an unexpected result and you want to restore your instance to its previous state.

Only scripts run by Build Agent in the current session can be reverted using this tool. For details on security and governance around the rollback script tool, see [Build Agent governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-governance.md).

**Note:** To use the rollback script tool, you must be on Zurich Patch 5 or later.

## Run query tool

Build Agent can use the run query tool to query a specific table within your instance and return the top five records or derive specific insights.

## Run script tool

The run script tool generates and runs a server-side script on your instance during a build session. Use the run script tool when you need Build Agent to perform an operation that goes beyond querying a table. For example, to retrieve data that requires custom logic, or to create something dynamically when no other tool covers the task.

Before the script runs, Build Agent shows you the generated script, its stated intent, and the application scope it will run in. You must approve the operation before it executes. The script runs in the scope of the app you're building by default. For details on security and governance around the run script tool, see [Build Agent governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/build-agent-governance.md).

**Note:** To use the run script tool, you must be on Zurich Patch 5 or later.

## Semantic metadata search tool

The semantic metadata search tool is part of Build Agent's tool registry. Semantic search enables you to describe what you're looking for without providing the exact file name or keyword. For example, you can search for `files related to incident process management`, and the tool finds relevant results based on semantic understanding, not just keyword matching. Indexing keeps results current as your instance evolves.

Build Agent uses semantic search in two ways:

-   **Implicit search**

    Build Agent determines when to use the semantic search tool based on your development task. When you describe what you need to accomplish, Build Agent searches for existing files and applications that match your intent, then presents the results in a plan for your approval. This helps prevent duplicate content creation.

-   **Explicit search**

    You can directly request a search by asking Build Agent to find something on your instance. Use explicit search when you want to locate specific files, applications, or knowledge without making changes.


**Note:** You must have Zurich Patch 9 and later to use the semantic search tool.

## Table schema inspector tool

The table schema inspector tool returns every field on a table, including field names, types, mandatory flags, and reference targets. Use the table schema inspector tool to understand a table's structure before adding fields or writing logic against it, and to verify the schema of base system tables.

## UI validation tool

Build Agent detects Build Agent detects UI components created during the build process, then analyzes and validates the UI using the UI validation tool. The tool automatically uses skills available in the Playwright MCP and executes them on the Automated Test Framework \(ATF\) Cloud Runner infrastructure.

You can specifically prompt UI validation by asking Build Agent to `validate the UI built using the ATF cloud runner tooling`.The UI validation tool is available for Build Agent in both ServiceNow Studio and the ServiceNow IDE, starting with Zurich Patch 10 to use it in ServiceNow Studio.

**Note:** The ATF test generator and Cloud Runner app must be installed on the instance to use the UI validation tool.

## Web search tool

Two Build Agent tools support external search.

-   Use the web search tool to find information on the public web.
-   Use the web fetch tool to retrieve content from a URL that you supply.

**Note:**

-   You must have Zurich Patch 11 and above to use the web search tool.
-   The web search tool must be enabled in the Build Agent settings. For more information, see [Configure web search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-configure-settings.md).

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

