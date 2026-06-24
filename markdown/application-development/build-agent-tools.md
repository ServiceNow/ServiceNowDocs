---
title: Build Agent tools
description: Build Agent tools support application development tasks such as semantic search, schema inspection, code search, planning, UI validation, database querying, and app navigation. Each tool extends what Build Agent can do during a build session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-tools.html
release: zurich
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Build Agent tools

Build Agent tools support application development tasks such as semantic search, schema inspection, code search, planning, UI validation, database querying, and app navigation. Each tool extends what Build Agent can do during a build session.

## Semantic search tool

The semantic search tool is part of Build Agent's tool registry. Semantic search enables you to describe what you're looking for without providing the exact file name or keyword. For example, you can search for `files related to incident process management`, and the tool finds relevant results based on semantic understanding, not just keyword matching.

Build Agent uses semantic search in two ways:

-   **Implicit search**

    Build Agent determines when to use the semantic search tool based on your development task. When you describe what you want to accomplish, Build Agent searches for existing files and applications that match your intent, then presents the results in a plan for your approval. This helps prevent duplicate content creation.

-   **Explicit search**

    You can directly request a search by asking Build Agent to find something on your instance. Use explicit search when you want to locate specific files, applications, or knowledge without making changes.


**Note:** You must have Zurich Patch 9 and above to use the semantic search tool.

## Table schema inspector tool

The table schema inspector tool returns every field on a table, including field names, types, mandatory flags, and reference targets. Use the table schema inspector tool to understand a table's structure before adding fields or writing logic against it, and to verify the schema of base system tables.

## Code search tool

The code search tool searches workspace files by exact text or regex patterns. Use the code search tool to find references to a field, script, or function across your app, and to understand the impact of a change before making it.

## Planning tool

Build Agent includes a planning tool that creates a detailed, step-by-step plan for your application development. You can refine the plan iteratively by prompting for changes and providing feedback until you reach a final version.

## UI validation tool

Build Agent detects Build Agent detects UI components created during the build process, then analyzes and validates the UI using the UI validation tool. The tool automatically uses skills available in the Playwright MCP and executes them on the Automated Test Framework \(ATF\) Cloud Runner infrastructure.

You can specifically prompt UI validation by asking Build Agent to `validate the UI built using the ATF cloud runner tooling`.The UI validation tool is available for Build Agent in both ServiceNow Studio and the ServiceNow IDE, though you must be on Zurich Patch 10 or higher to use it in ServiceNow Studio.

**Note:**

1.  The ATF test generator and Cloud Runner app must be installed on the instance to use the UI validation tool.
2.  You must have Zurich Patch 9 or higher to use the UI validation tool.

## Run query tool

Build Agent can use the run query tool to query a specific table within your instance and return the top five records or derive specific insights.

## Open app tool

For applications that were not developed using the ServiceNow IDE, ServiceNow Studio, or the ServiceNow SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the open app tool to locate the application you want. Alternatively, you can search for an application directly within the Build Agent, and it will automatically use the open app tool. The open app tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.

**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

