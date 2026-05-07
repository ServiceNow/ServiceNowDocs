---
title: Build Agent tools
description: Development tools integrate with Build Agent to automate application building tasks. The tools provide semantic search capabilities, development planning assistance, automated UI validation fixes, database querying, and application navigation support.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Build Agent tools

Development tools integrate with Build Agent to automate application building tasks. The tools provide semantic search capabilities, development planning assistance, automated UI validation fixes, database querying, and application navigation support.

## Semantic search tool

The semantic search tool is part of Build Agent's tool registry. Semantic search enables you to describe what you're looking for without providing the exact file name or keyword. For example, you can search for `files related to incident process management`, and the tool finds relevant results based on semantic understanding, not just keyword matching.

Build Agent uses semantic search in two ways:

-   **Implicit search**

    Build Agent automatically decides when to use the semantic search tool based on your development task. When you describe what you want to accomplish, Build Agent searches for existing files and applications that match your intent, then presents the results in a plan for your approval. This helps prevent duplicate content creation.

-   **Explicit search**

    You can directly request a search by asking Build Agent to find something on your instance. It’s useful when you want to locate specific files, applications, or knowledge without making changes.


## Planning tool

Build Agent includes a planning tool that creates a detailed, step-by-step plan for your application development. You can refine the plan iteratively by prompting for changes and providing feedback until you reach a final version. The tool emphasizes user control, enabling you to use prompts to request changes to the plan. Overall, it facilitates collaborative planning before proceeding with implementation.

## UI validation tool

Build Agent intelligently recognizes if there are UI components that it created as part of the build process, and analyzes and validates the UI using UI validation tool. The tool automatically uses skills available in the Playwright MCP and executes them on the Automated Test Framework \(ATF\) Cloud Runner infrastructure.

You can specifically prompt UI validation by asking Build Agent to `validate the UI built using the ATF cloud runner tooling`.

**Note:** The ATF test generator and Cloud Runner apps must be installed on the instance to use the UI validation tool.

## Run Query tool

Build Agent can use the Run Query tool to query a specific table within your instance and return the top five records or derive specific insights.

## Open App tool

For applications that were not developed using the ServiceNow IDE, ServiceNow Studio, or the ServiceNow SDK, you must convert them into Fluent format to enable development within the Build Agent. You can prompt the Build Agent to use the Open App tool to locate the application you want. Alternatively, you can search for an application directly within the Build Agent, and it will automatically use the Open App tool. The Open App tool can find an application, convert it to Fluent format, and then add the converted app to your workspace.

**Parent Topic:**[Exploring Build Agent](exploring-build-agent.md)

