---
title: Autonomous Engineer in Build Agent
description: Autonomous Engineer is an agentic worker in Build Agent that takes your requirements and generates an implementation plan. It then builds all work items in parallel, without requiring you to construct each artifact manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/vc-autonomous-engineer.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Autonomous Engineer, Build Agent, agentic development, implementation plan, vibe coding, parallel execution, work items, agent packs]
breadcrumb: [Build Agent overview, Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Autonomous Engineer in Build Agent

Autonomous Engineer is an agentic worker in Build Agent that takes your requirements and generates an implementation plan. It then builds all work items in parallel, without requiring you to construct each artifact manually.

When an application is large or complex, building it artifact-by-artifact through conversational prompts can be slow. Autonomous Engineer addresses this by taking your requirements as input and driving the full implementation lifecycle end to end, from requirements intake through parallel execution of work items.

**Note:** You must install the Autonomous Engineer app from the ServiceNow Store. Check your entitlements to see whether you can use Autonomous Engineer.

Autonomous Engineer is available in ServiceNow Studio and covers custom applications. For full product documentation, see [Autonomous Engineer in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-autonomous-engineer.md).

## Autonomous Engineer process

Autonomous Engineer follows two sequential phases. You retain control throughout both phases and must review and approve the plan before any artifacts are built.

-   **Planning phase**

    Provide your requirements as a natural language description or a file upload, such as a CSV of user stories. Autonomous Engineer interviews you to resolve ambiguous details. It then queries your instance to identify existing tables, roles, fields, and catalog items so it does not duplicate what is already there. The output is a plan with work items structured in an Agile user story format, including acceptance criteria and test criteria, sequenced using a dependency graph. Review and edit each work item before approving the plan.

-   **Execution phase**

    After you approve the plan, Autonomous Engineer generates a background agent for each work item and builds all work items in parallel. Each agent builds the required artifacts, generates Automated Test Framework \(ATF\) tests, and runs those tests. Failed tests trigger automatic root cause analysis and retry cycles. When all work items are complete, Autonomous Engineer generates an update set for deployment.


## Agent packs

Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge during implementation. For more information, see [Agent packs for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

## Autonomous Engineer compared to standard Build Agent development

Standard Build Agent development is conversational and turn-by-turn: you prompt, review, and iterate on one artifact or change at a time. Autonomous Engineer shifts that model by working from a plan. It builds multiple work items in parallel in the background, so you interact primarily at the planning and review stages rather than guiding every step.

Use standard Build Agent development when you're building incrementally, exploring ideas, or making targeted changes. Use Autonomous Engineer when you have well-defined requirements for a larger implementation and need to reduce the number of manual prompting steps.

**Parent Topic:**[Agentic ServiceNow AI Platform development with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vc-build-agent-landing.md)

