---
title: Autonomous Engineer in Build Agent
description: Autonomous Engineer is an agentic worker in Build Agent that takes your requirements and generates an implementation plan. It then builds all work items in parallel, without requiring you to construct each artifact manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/vc-autonomous-engineer.html
release: australia
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 4
keywords: [Autonomous Engineer, Build Agent, agentic development, implementation plan, vibe coding, parallel execution, work items, agent packs]
breadcrumb: [Build Agent overview, Develop, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Autonomous Engineer in Build Agent

Autonomous Engineer is an agentic worker in Build Agent that takes your requirements and generates an implementation plan. It then builds all work items in parallel, without requiring you to construct each artifact manually.

When an application is large or complex, building it artifact-by-artifact through conversational prompts can be slow. Autonomous Engineer addresses this by taking your requirements as input and driving the full implementation lifecycle end to end, from requirements intake through parallel execution of work items.

**Note:** You must install the Autonomous Engineer app from the ServiceNow Store. Check your entitlements to see whether you can use Autonomous Engineer.

Autonomous Engineer is available in ServiceNow Studio and supports custom applications. For full product documentation, see [Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer.md). To start using Autonomous Engineer, see [Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-using-autonomous-engineer.md).

## Autonomous Engineer process

Autonomous Engineer follows two sequential phases. You retain control throughout both phases and must review and approve the plan before any artifacts are built.

-   **Planning phase**

    Provide your requirements as a natural language description or a file upload, such as a CSV of user stories. Autonomous Engineer interviews you to resolve ambiguous details. It then queries your instance to identify existing tables, roles, fields, and catalog items so it does not duplicate what is already there. The output is a plan with work items structured in an Agile user story format, including acceptance criteria and test criteria, sequenced using a dependency graph. Review and edit each work item before approving the plan.

-   **Execution phase**

    After you approve the plan, Autonomous Engineer generates a background agent for each work item and builds all work items in parallel. Each agent builds the required artifacts, generates Automated Test Framework \(ATF\) tests, and runs those tests. Failed tests trigger automatic root cause analysis and retry cycles. When all work items are complete, Autonomous Engineer generates an update set for deployment.


## Agent packs

Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge during implementation. For more information, see [Agent packs for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

## Autonomous Engineer compared to standard Build Agent development

Standard Build Agent development is conversational and turn-by-turn: you prompt, review, and iterate on one artifact or change at a time. Autonomous Engineer shifts that model by working from a plan. It builds multiple work items in parallel in the background, so you interact primarily at the planning and review stages rather than guiding every step.

Use standard Build Agent development when you're building incrementally, exploring ideas, or making targeted changes. Use Autonomous Engineer when you have well-defined requirements for a larger implementation and need to reduce the number of manual prompting steps.

## More information about Autonomous Engineer

-   **Autonomous Engineer and Build Agent**

    Differences between the two products and what they share. See [Autonomous Engineer and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-build-agent-relationship.md).

-   **Plan dashboard**

    Work item status, artifacts, and execution progress for a plan. See [Using the dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-plan-dashboard.md).

-   **Plans**

    Create, open, and manage plans from the **Plans** view in the Build Agent panel. See [Plans in Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-plans.md).

-   **Playbook authoring**

    Autonomous Engineer and Build Agent can author Playbook Designer artifacts. See [Playbook authoring with Build Agent and Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-playbooks.md).

-   **MCP connections**

    Connections that give Autonomous Engineer access to external tools and resources, using the same supported servers as Build Agent. See [MCP connections and Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-mcp-connections.md).

-   **Limitations**

    Limitations that apply to Build Agent also apply to Autonomous Engineer. See [Autonomous Engineer limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-limitations.md).


**Parent Topic:**[Agentic ServiceNow AI Platform development with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vc-build-agent-landing.md)

