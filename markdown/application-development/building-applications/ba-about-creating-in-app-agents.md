---
title: Agentic workflows, agents, and skills
description: Build Agent can generate agentic workflows, agents, and skills scoped to your custom app. Turn business requirements into configured AI artifacts without building from scratch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/ba-about-creating-in-app-agents.html
release: australia
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Agentic workflows, agents, and skills

Build Agent can generate agentic workflows, agents, and skills scoped to your custom app. Turn business requirements into configured AI artifacts without building from scratch.

You must install Now Assist for App Engine to create agentic workflows, agents, and skills. For more information, see [Installing Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-app-engine/install-now-assist-for-app-engine.md).

Verify that you have access to ServiceNow Studio or the ServiceNow IDE.

**Note:** Your entitlements determine whether you have access to agentic workflows, agents, and skills in Build Agent.

Skills must be published before they can be used as a tool by another skill.

Build Agent supports the following tool creation:

-   Skills:
    -   \*FlowAction
    -   Now Assist Skill
    -   Script - Inline
    -   Script - Explicit
    -   \*SubFlow
    -   WebSearch
-   Agents:
    -   Catalog item: For more information, see .
    -   Conversational topic: For more information, see .
    -   Flow action: For more information, see .
    -   Now Assist Skill: For more information, see .
    -   Record operations: For more information, see .
    -   Script: For more information, see .
    -   \*\*Search retrieval: For more information, see .
    -   Subflow: For more information, see .
    -   WebSearch: For more information, see .

**Note:**

1.  \*You can use only FlowActions and Subflows that are already part of your app scope. Build Agent reuses existing FlowActions and Subflows instead of creating new ones.
2.  \*\*When you create an agent that requires knowledge retrieval, Build Agent can configure a search retrieval tool scoped to your use case. The tool queries your existing search profiles to identify the best match, retrieves the associated search sources and return fields, and checks whether semantic search indexes are available.

    **Note:** You must be on Australia Patch 3 or higher to use the search retrieval tool.


The agentic capability turns business requirements into fully configured agents, skills, and agentic workflows for custom applications. It evaluates existing app context, such as tables, roles, business rules, and metadata, and applies a four-phase pattern to generate artifacts scoped to your application's data model, roles, and ACLs:

-   **Assess**

    Evaluates data model readiness for AI.

-   **Analyze**

    Identifies use cases from existing tables, roles, and flows.

-   **Design**

    Proposes an architecture with a recommended quick-win.

-   **Build**

    Generates agents and skills scoped to the application's data model, roles, and ACLs.


In-App agents can work with any custom scoped application. Applications with real data, established roles, and defined automation produce more targeted, domain-specific artifacts. Applications with no data or configuration produce agents that aren't scoped to a specific data model.

**Note:** Generated agents are automatically registered in AI Control Tower for centralized governance, and artifacts deploy through standard update sets.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/use-build-agent.md)

