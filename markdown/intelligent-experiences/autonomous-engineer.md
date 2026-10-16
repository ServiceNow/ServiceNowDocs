---
title: Autonomous Engineer
description: This AI agent helps with implementing ServiceNow applications. The agent accepts requirements, generates a plan with structured work items, and builds all work items in parallel using background AI agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/autonomous-engineer.html
release: brazil
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 2
breadcrumb: [AI Workflow Factory AI agents, AI Workflow Factory, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Autonomous Engineer

This AI agent helps with implementing ServiceNow applications. The agent accepts requirements, generates a plan with structured work items, and builds all work items in parallel using background AI agents.

**Important:** Autonomous Engineer uses a different framework than other ServiceNow® AI agents. Review the following workflow and configuration settings for Autonomous Engineer. For more information, see .

## Build Agent dependency

Autonomous Engineer uses Build Agent, a separate AI agent part of ServiceNow Otto for Creator, as its execution layer. When you install Autonomous Engineer, Build Agent is installed as a dependency.

Because Autonomous Engineer is powered by Build Agent, both products use the same settings. For more information about these settings, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/build-agent.md).

## Workflow

Autonomous Engineer accepts requirements, generates a structured plan for the user to approve, and builds all work items in parallel using background AI agents.

1.  Accept requirements from a natural language prompt or an uploaded file, such as a CSV of user stories.
2.  Search the instance for existing artifacts, such as tables, roles, fields, and catalog items, to avoid duplicating them.
3.  Interview the user to resolve ambiguous or incomplete details, and then generate a brief for approval.
4.  Generate a plan of work items in Agile user story format, with acceptance criteria and test criteria. Group the work items into logical sections and sequence them using a dependency graph.
5.  List any steps that require manual action, such as activating plugins, in a pre-flight verification section.
6.  Pause for user review and approval of the plan and its work items.
7.  Once approved, load the applicable agent pack, and generate a background agent for each work item.
8.  Build all work items in parallel, running each work item only after the work items it depends on are complete.
9.  For each work item, build the required metadata, and then run Test Agent to generate and run Automated Test Framework \(ATF\) tests.
10. If tests fail, identify the root cause and retry the work item. Detect stuck or unresponsive agents and retry their work items automatically.
11. Display the status of each work item on the plan dashboard, and highlight the work items that need attention in the dashboard and chat panel.
12. Pause each completed work item for user validation.
13. Generate an update set for the plan when all work items are complete.

## Configuration

|Configuration area|Description|
|------------------|-----------|
|Plugins|The Autonomous Engineer plugin is `sn_autonomous_eng`. When you install Autonomous Engineer, the Build Agent plugin is installed as a dependency.|
|Access|Autonomous Engineer is accessible via the Build Agent chat panel in ServiceNow Studio.|
|Agent packs|Autonomous Engineer uses agent packs to understand ServiceNow products. You can install different agent packs depending on the implementation you're completing. For more information, see .|

**Parent Topic:**[AI Workflow Factory AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-workflow-factory-prime-ai-agents.md)

