---
title: Agent packs for Autonomous Engineer
description: Agent packs bundle the domain knowledge, tools, and skills that Autonomous Engineer uses to plan and implement custom applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-auto-eng-agent-packs.html
release: brazil
topic_type: concept
last_updated: "2026-11-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, agent packs, Autonomous Engineer, Build Agent, implementation, ServiceNow products, ATF tests, run server side step, ATF list steps]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Agent packs for Autonomous Engineer

Agent packs bundle the domain knowledge, tools, and skills that Autonomous Engineer uses to plan and implement custom applications.

When you use Autonomous Engineer to build a custom application, Autonomous Engineer loads agent packs to understand the platform. An agent pack bundles the domain knowledge, tools, and skills that background agents require to generate accurate artifacts during plan execution.

Agent packs are active during Autonomous Engineer execution.

**Note:** You must install the Autonomous Engineer app from the ServiceNow Store. Check your entitlements to see whether you can use Autonomous Engineer.

## How agent packs work

All agent packs share a common base that provides the core capabilities available to every background agent during Autonomous Engineer execution. Each agent pack extends this base with its own knowledge. For example, the Platform development pack adds knowledge of platform metadata. Autonomous Engineer activates the right agent pack when it needs it, and an active pack is available to every background agent working on a work item. You don't install agent packs. They ship as part of each release.

Each agent pack also includes Automated Test Framework \(ATF\) Test Agent capabilities for the work it covers. When a background agent completes a work item, it uses Test Agent in the agent pack to generate tests. The tests validate the work item against the acceptance criteria in your plan.

For details on Test Agent use in Autonomous Engineer, see [Test what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md).

For details on using agent packs to implement applications, see [Use Autonomous Engineer to implement an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-autonomous-engineer.md).

## Agent packs and custom applications

Agent packs are available in the Brazil EA \(Patch 0\) release:

-   The Planning pack, which parses requirements, interviews you to resolve unclear details, applies best practices, and generates a structured plan of work items.
-   The Platform development pack, which gives Autonomous Engineer knowledge of platform metadata, the building blocks that custom applications and customizations use. The ServiceNow AI Platform knowledge helps generated work items and artifacts align with standard platform conventions.

During planning, Autonomous Engineer asks follow-up questions to gather requirements and suggests recommendations based on best practices before it generates the plan.

Autonomous Engineer plans custom work with platform knowledge from the Platform development pack.

If your implementation spans a ServiceNow product and custom application development, Autonomous Engineer applies the Platform development pack to work items for custom artifacts.

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-autonomous-engineer.md)

