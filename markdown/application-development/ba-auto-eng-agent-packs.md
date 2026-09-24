---
title: Agent packs for Autonomous Engineer
description: Agent packs bundle the domain knowledge, tools, and skills that Autonomous Engineer uses to implement ServiceNow products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-auto-eng-agent-packs.html
release: brazil
topic_type: concept
last_updated: "2026-09-08"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, agent packs, Autonomous Engineer, Build Agent, implementation, ServiceNow products, ATF tests, run server side step, ATF list steps]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Agent packs for Autonomous Engineer

Agent packs bundle the domain knowledge, tools, and skills that Autonomous Engineer uses to implement ServiceNow products.

When you use Autonomous Engineer to implement a ServiceNow product, Autonomous Engineer loads an agent pack to understand that product. An agent pack bundles the domain knowledge, tools, and skills that background agents require to generate accurate, product-specific artifacts during plan execution.

Agent packs are active during Autonomous Engineer execution.

**Note:** You must install the Autonomous Engineer app from the ServiceNow Store. Check your entitlements to see whether you can use Autonomous Engineer.

## How agent packs work

All agent packs share a common base that provides the core capabilities available to every background agent during Autonomous Engineer execution. Product-specific packs extend this base with product-specific knowledge. When you run a plan that involves a ServiceNow product, Autonomous Engineer loads the corresponding agent pack. That agent pack is available to every background agent working on a work item for that product.

Each agent pack also includes Automated Test Framework \(ATF\) Test Agent capabilities for the product it covers. When a background agent completes a work item, it uses Test Agent in the agent pack to generate tests. The tests validate the work item against the acceptance criteria in your plan.

For details on Test Agent use in Autonomous Engineer, see [Test what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md).

For details on using agent packs to implement ServiceNow products and applications, see [Use Autonomous Engineer to implement an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-autonomous-engineer.md).

## Agent packs and custom applications

Agent packs are available in the Brazil EA \(Patch 0\) release:

-   The Planning pack, which parses requirements and interviews you for clarity, applies ServiceNow best practices, and generates a structured plan of work items.
-   The Platform development pack, which provides domain knowledge for implementing custom applications on your instance. The Platform development pack gives Autonomous Engineer awareness of platform tables, roles, and configuration patterns specific to custom app development. The awareness helps generated work items and artifacts align with standard platform conventions.

Agent packs are specific to ServiceNow products. Autonomous Engineer applies instance awareness and your requirements to generate the plan without product-specific domain knowledge.

If your implementation spans a ServiceNow product and custom application development, Autonomous Engineer will apply the appropriate agent packs. The agent pack applies only to work items that target the product. Work items for custom artifacts are handled by the base implementation capabilities.

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-autonomous-engineer.md)

